# CLAUDE.md — Frontend Website Rules

## Always Do First

- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.

## Reference Images

- If a reference image is provided: match layout, spacing, typography, and color exactly. Swap in placeholder content (images via `https://placehold.co/`, generic copy). Do not improve or add to the design.
- If no reference image: design from scratch with high craft (see guardrails below).
- Screenshot your output, compare against reference, fix mismatches, re-screenshot. Do at least 2 comparison rounds. Stop only when no visible differences remain or user says so.

## Local Server

- **Always serve on localhost** — never screenshot a `file:///` URL.
- Start the dev server: `node serve.mjs` (serves the project root at `http://localhost:3000`)
- `serve.mjs` lives in the project root. Start it in the background before taking any screenshots.
- If the server is already running, do not start a second instance.

## Screenshot Workflow

- Puppeteer is installed at `C:/Users/nateh/AppData/Local/Temp/puppeteer-test/`. Chrome cache is at `C:/Users/nateh/.cache/puppeteer/`.
- **Always screenshot from localhost:** `node screenshot.mjs http://localhost:3000`
- Screenshots are saved automatically to `./temporary screenshots/screenshot-N.png` (auto-incremented, never overwritten).
- Optional label suffix: `node screenshot.mjs http://localhost:3000 label` → saves as `screenshot-N-label.png`
- `screenshot.mjs` lives in the project root. Use it as-is.
- After screenshotting, read the PNG from `temporary screenshots/` with the Read tool — Claude can see and analyze the image directly.
- When comparing, be specific: "heading is 32px but reference shows ~24px", "card gap is 16px but should be 24px"
- Check: spacing/padding, font size/weight/line-height, colors (exact hex), alignment, border-radius, shadows, image sizing

## Output Defaults

- Single `index.html` file, all styles inline, unless user says otherwise
- Tailwind CSS via CDN: `<script src="https://cdn.tailwindcss.com"></script>`
- Placeholder images: `https://placehold.co/WIDTHxHEIGHT`
- Mobile-first responsive

## Brand Assets

- Always check the `brand_assets/` folder before designing. It may contain logos, color guides, style guides, or images.
- If assets exist there, use them. Do not use placeholders where real assets are available.
- If a logo is present, use it. If a color palette is defined, use those exact values — do not invent brand colors.

## Anti-Generic Guardrails

- **Colors:** Never use default Tailwind palette (indigo-500, blue-600, etc.). Pick a custom brand color and derive from it.
- **Shadows:** Never use flat `shadow-md`. Use layered, color-tinted shadows with low opacity.
- **Typography:** Never use the same font for headings and body. Pair a display/serif with a clean sans. Apply tight tracking (`-0.03em`) on large headings, generous line-height (`1.7`) on body.
- **Gradients:** Layer multiple radial gradients. Add grain/texture via SVG noise filter for depth.
- **Animations:** Only animate `transform` and `opacity`. Never `transition-all`. Use spring-style easing.
- **Interactive states:** Every clickable element needs hover, focus-visible, and active states. No exceptions.
- **Images:** Add a gradient overlay (`bg-gradient-to-t from-black/60`) and a color treatment layer with `mix-blend-multiply`.
- **Spacing:** Use intentional, consistent spacing tokens — not random Tailwind steps.
- **Depth:** Surfaces should have a layering system (base → elevated → floating), not all sit at the same z-plane.

## Mobile Responsiveness (mandatory before any deploy)

- Every page MUST be fully tested and optimized for mobile (375px width) before pushing to production.
- Use responsive breakpoints: 375px (mobile), 768px (tablet), 1024px (desktop), 1440px (large desktop).
- Mobile-specific rules:
  - Navigation: collapse to hamburger menu or bottom navigation bar on screens < 768px
  - Typography: reduce heading sizes by 30-40% on mobile. Body text minimum 16px.
  - Spacing: reduce section padding to 60-80px vertical on mobile (from 120-160px on desktop)
  - Cards/grids: stack vertically on mobile, single column
  - Touch targets: all clickable elements must be minimum 44x44px
  - Images: must scale down proportionally, never overflow the viewport
  - 3D/WebGL elements: simplify or reduce on mobile for performance (fewer particles, smaller grids)
  - Horizontal scrolling: NEVER allow horizontal scroll on mobile — if it happens, fix it immediately
- When asked to build any section, always write mobile styles FIRST, then add desktop overrides with min-width media queries.
- Before any push to production, verify the site looks correct at 375px, 768px, and 1440px widths.

## Security Check (mandatory before every push)

- Before any commit or push to GitHub, scan ALL project files for:
  - API keys (any string that looks like a key: `sk-`, `pk-`, `api_`, `key_`, `secret_`, etc.)
  - Hardcoded passwords or credentials
  - Access tokens or authentication tokens
  - Webhook URLs
  - `.env` files not listed in `.gitignore`
  - Any sensitive data (private emails, secrets, database connection strings)
- If you find anything suspicious: DO NOT push. Alert me, explain what you found and where, and wait for my instruction.
- If nothing is found: explicitly confirm "Security check passed — no sensitive information found" before proceeding with the push.
- Ensure a `.gitignore` file exists and excludes at minimum: `.env`, `node_modules/`, `temporary screenshots/`, and any file containing credentials.

## Git Commits
- Always commit as "Fernando Eijo" <fernandoeijo1@gmail.com>
- Do NOT add Co-authored-by trailers to commit messages
- Do NOT use --author flags with any other identity

## Hard Rules

- Do not add sections, features, or content not in the reference
- Do not "improve" a reference design — match it
- Do not stop after one screenshot pass
- Do not use `transition-all`
- Do not use default Tailwind blue/indigo as primary color
