# Análisis de Referencia Visual — brightstone.ca/about/

*Análisis realizado: 2026-03-16*
*URL: https://brightstone.ca/about/*
*Nota: Los screenshots fueron capturados durante la sesión de navegador. Para referencia visual directa, visitar la URL.*

---

## Estructura de Secciones de la Página

La página About de Brightstone sigue una estructura vertical clara con secciones bien definidas y mucho espacio en blanco entre ellas:

1. **Header / Navegación** — Sticky, fondo transparente que toma el color del fondo de la página (beige claro). Logo a la izquierda, navegación a la derecha.

2. **Hero / Intro** — Animación de carga con un elemento decorativo de estrella/cruz de 4 puntas y líneas cruzadas (color terracotta). Transiciona a una gran imagen full-width de un interior de cocina de lujo.

3. **History** — Etiqueta "HISTORY" en uppercase pequeño a la izquierda. Texto descriptivo a la derecha en tipografía serif grande (~30px). Layout asimétrico con texto ocupando 60% derecho.

4. **Approach** — Etiqueta "APPROACH" en uppercase a la izquierda. Layout de dos columnas: texto con valores/pilares a la izquierda (con ícono de estrella decorativa), imagen de proyecto a la derecha. Cada pilar tiene título en bold + descripción breve.
   - "Discerningly selected." — sobre ubicaciones
   - "Artfully envisioned." — [sobre diseño]

5. **Core Values** — Etiqueta "CORE VALUES" en uppercase. Headline grande a la izquierda: "Every home is built on an unshakeable foundation of *stone*." (la palabra "stone" en color terracotta/itálica). A la derecha, valores listados con letra inicial gigante (gris claro, ~150px) + título en bold + descripción:
   - **S** — Superior quality. "Craft residences that last."
   - **T** — Transparent relationships. "Uphold integrity in all communications."
   - **N** — Nuanced precision. "Embrace full immersion in the details of each project."
   - **E** — Everlasting impact. "Approach each development as an opportunity..."

6. **Imagen full-width** — Foto panorámica de paisaje urbano con parque, árboles y skyline de ciudad. Funciona como separador visual entre secciones.

7. **Leadership** — Etiqueta "LEADERSHIP" en uppercase. Texto introductorio sobre los 45+ años de experiencia colectiva. Cards de líderes en grid de 2 columnas con: foto, nombre, cargo.
   - Noah Shechtman — Director of Development
   - Jonathan Marmer — Director of Operations & Construction

8. **Decorative Divider** — Elementos decorativos de estrella/cruz con líneas (mismos que en el hero), que funcionan como separadores de sección.

9. **CTA / Get in Touch** — Heading gigante "Get in touch." con tipografía sans-serif a ~90px. Icono circular de flecha a la derecha (botón de navegación).

10. **Footer** — Minimalista. Logo a la izquierda, links de navegación centrados (ABOUT, DESIGN, COMMUNITIES, NEWS, CONTACT), PRIVACY y copyright a la derecha. Todo en una sola línea horizontal. Separado del contenido por una línea fina.

---

## Tipografías

### Fuente principal: Degular (sans-serif)
- Se usa para TODO el sitio — tanto headings como body text
- No usa par serif + sans como muchos sitios de lujo; en cambio usa una sola familia con variaciones de tamaño y peso

### Aplicación tipográfica:
| Elemento | Font | Size | Weight | Letter-Spacing | Line-Height | Color |
|----------|------|------|--------|----------------|-------------|-------|
| H1 (headlines grandes) | Degular | 91.2px | 400 (regular) | -1.6px (tight) | 100.8px (1.1) | rgb(61, 57, 53) — marrón oscuro |
| H2 (section labels) | Degular | 16px | 400 | 1.6px (wide) | 25.6px (1.6) | rgb(61, 57, 53) |
| Body (párrafos) | Degular | 22.4px | 400 | normal | 33.6px (1.5) | rgb(61, 57, 53) |
| Nav links | System sans-serif | 16px | 400 | — | — | — |
| Accent text (itálica) | Degular | — | — | — | — | rgb(186, 91, 63) — terracotta |

### Notas tipográficas:
- Los headings usan letter-spacing negativo (tracking cerrado = -1.6px) para mayor impacto visual
- Los labels de sección (HISTORY, APPROACH, etc.) usan letter-spacing positivo amplio (1.6px) + uppercase = efecto de etiqueta/tag
- El body text es relativamente grande (22.4px) para legibilidad premium
- Las letras decorativas de los valores (S, T, N, E) son ~150px en gris muy claro, puramente decorativas

---

## Paleta de Colores

| Color | Hex (aproximado) | Uso |
|-------|-------------------|-----|
| Beige claro (fondo) | #F0EBE3 / rgb(240,235,227) | Fondo principal de toda la página |
| Marrón oscuro (texto) | #3D3935 / rgb(61,57,53) | Todo el texto principal |
| Terracotta/cobre | #BA5B3F / rgb(186,91,63) | Color accent — botón ABOUT activo, texto destacado, elementos decorativos (estrellas), itálicas |
| Gris claro | ~#C0BCB7 | Letras decorativas grandes (S, T, N, E), separadores |
| Blanco | #FFFFFF | No se usa como fondo — el beige es el "blanco" del sitio |
| Negro/casi-negro | ~#2A2724 | Usado mínimamente |

### Notas sobre color:
- El sitio NO usa blanco puro — todo el fondo es beige cálido
- Solo hay UN color de acento (terracotta) contra la base neutra
- La paleta es extremadamente contenida: 2-3 colores reales
- El color terracotta transmite calidez, artesanía, material natural

---

## Espaciado y Layout General

### Espaciado vertical:
- **Entre secciones:** 120-160px de espacio vertical (muy generoso)
- **Dentro de secciones:** 40-60px entre elementos
- **Padding lateral:** ~80-100px en desktop (1440px), contenido centrado con max-width ~1200px

### Layout patterns:
- **Asimétrico 40/60:** Label de sección a la izquierda (40%), contenido principal a la derecha (60%)
- **Full-width images:** Las imágenes rompen el grid y van edge-to-edge
- **Separadores:** Líneas finas horizontales (1px, gris claro) + elementos decorativos de estrella
- **Mucho "air":** El sitio respira. Hay más espacio vacío que contenido visible en cada viewport

### Grid/Container:
- Max-width del contenido: ~1200-1300px centrado
- Las imágenes full-width salen de este container
- Grid de 2 columnas para la sección de liderazgo

---

## Elementos de Diseño Más Destacables

### 1. Elementos decorativos de estrella/cruz
- Motivo visual recurrente: una estrella de 4 puntas con líneas cruzadas (horizontales y verticales) que se extienden
- Color terracotta, trazo fino
- Aparecen como: animación de carga, separadores de sección, elementos decorativos de fondo
- Transmiten: precisión, artesanía, atención al detalle

### 2. Letras iniciales gigantes en los valores
- Cada valor (S, T, N, E) tiene su inicial en ~150px, gris muy claro
- Funciona como elemento gráfico/decorativo, no solo tipográfico
- Crea un juego visual que deletrea "STONE" (el nombre de la empresa)
- Muy inteligente como recurso de branding integrado al diseño

### 3. Uso del color terracotta como acento único
- Solo un color de acento en todo el sitio
- Se usa para: el botón activo de navegación (pill shape), texto itálico destacado, elementos decorativos
- Crea una identidad visual inmediata y memorable

### 4. Imágenes full-width como separadores
- Fotografía de interiores de alta calidad (cocina de lujo) en el hero
- Fotografía de paisaje/entorno entre secciones
- Las imágenes NO tienen overlay ni tratamiento — se muestran puras contra el fondo beige

### 5. Navegación pill-shaped
- El item activo de la navegación tiene un fondo terracotta en forma de pill/cápsula con texto blanco
- Los demás items son texto plano en uppercase con letter-spacing amplio
- Es sutil pero efectivo para indicar la página activa

### 6. Footer extremadamente minimalista
- Una sola línea: logo + nav links + copyright
- Sin columnas múltiples, sin newsletter, sin redes sociales visibles
- Separado del contenido por una línea fina

### 7. CTA "Get in touch." como sección completa
- Heading gigante (~90px) que ocupa todo el ancho
- Solo acompañado de un ícono circular de flecha
- Mucho espacio vacío alrededor — le da importancia y urgencia elegante

---

## Resumen para Replicar con Branding de VF Construcciones

Para adaptar este diseño a VF Construcciones, los elementos clave a replicar son:

1. **Fondo beige/crema cálido** en vez de blanco puro (adaptar a los tonos de VF: quizás #F5F3F0)
2. **Una sola tipografía sans-serif** con variaciones de tamaño — o el par serif+sans de VF (Cormorant Garamond + Inter)
3. **Headings gigantes** (~90px) con tracking negativo para impacto
4. **Labels de sección** en uppercase con letter-spacing amplio
5. **Color de acento único** — el turquesa de VF (#4DB8C7) reemplaza al terracotta de Brightstone
6. **Espaciado extremadamente generoso** entre secciones (120-160px)
7. **Imágenes full-width** de sus obras finalizadas como separadores
8. **Layout asimétrico** con labels a la izquierda y contenido a la derecha
9. **Elementos decorativos** propios (quizás líneas que evoquen planos arquitectónicos o la geometría del logo VF)
10. **Footer minimalista** en una sola línea
11. **CTA "Empezá tu proyecto"** como sección gigante independiente
12. **Mucho espacio vacío** — el "aire" transmite premium y confianza

### Diferencias a considerar:
- Brightstone usa **un solo font** (Degular); VF puede usar su **par Cormorant Garamond + Inter** para más diferenciación
- El **negro del logo de VF** reemplaza al marrón oscuro de Brightstone como color base de texto
- El **turquesa de las piletas** de VF como acento en vez del terracotta de Brightstone
- Donde Brightstone muestra paisaje urbano, VF debe mostrar sus **barrios cerrados y entornos verdes**
