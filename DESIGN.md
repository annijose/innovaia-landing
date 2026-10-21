# INNOVAIA TECH — Design System & Brand Identity Manual

> **Versión:** 2.0 (Edición Navy × Orange)  
> **Dirección Visual:** Neo-Grotesque Swiss Precision & High-Contrast Dark UI  
> **Colores Insignia:** Innovaia Navy (`#14213D`) × Innovaia Orange (`#FF6B35`)  
> **Tipografía Oficial:** **Univers** (`Univers Next` / `Univers LT Std`)

---

## 1. Esencia de Marca y Dualidad Visual (`Navy × Orange`)

La identidad visual de **INNOVAIA TECH** se fundamenta en el equilibrio entre **rigor arquitectónico corporativo** y **energía transformadora de Inteligencia Artificial**:

- **Innovaia Navy (`#14213D`) — Autoridad, Ingeniería y Estabilidad:** Representa la solidez de las arquitecturas empresariales (ERP, Cloud Native, FinTech, Seguridad Bancaria) y más de 18 años de liderazgo técnico.
- **Innovaia Orange (`#FF6B35`) — Innovación, Dinamismo e IA:** Aporta energía cinética, protagonismo visual y direccionalidad hacia la acción (CTAs, indicadores activos, nodos de IA y métricas clave).
- **Obsidian Canvas (`#050811` / `#000000`) — Profundidad Dimensional:** El lienzo oscuro profundo permite que los bloques en `#14213D` y `#FF6B35` proyecten iluminación ambiental (*ambient glow*) y bordes biselados con estética tridimensional moderna.

---

## 2. Sistema de Color (Color Tokens)

### 2.1 Colores Principales de Marca (Core Brand Palette)

| Token | Nombre | HEX | RGB | Rol Principal |
| :--- | :--- | :--- | :--- | :--- |
| `brand-navy` | **Innovaia Navy** | `#14213D` | `rgb(20, 33, 61)` | Color primario de marca, contenedores elevados, tarjetas principales y bloques estructurales. |
| `brand-orange` | **Innovaia Orange** | `#FF6B35` | `rgb(255, 107, 53)` | Acento principal de alta energía, botones primarios (CTA), badges activos, iconos e indicadores clave. |
| `brand-black` | **Obsidian Void** | `#050811` | `rgb(5, 8, 17)` | Fondo base principal de la interfaz (reemplaza el negro plano con un matiz azul nocturno profundo). |
| `pure-white` | **Pure White** | `#FFFFFF` | `rgb(255, 255, 255)` | Titulares principales (`H1`-`H3`), textos sobre botones primarios y contraste máximo. |

---

### 2.2 Escala Tonal y Superficies (Surface & Accent Architecture)

Para construir interfaces oscuras con jerarquía de elevación sin depender de sombras pesadas, el sistema utiliza una progresión tonal derivada de `#14213D` y `#FF6B35`:

| Token Tailwind / CSS | HEX | Uso en Interfaz |
| :--- | :--- | :--- |
| `background` / `absolute-black` | `#050811` | Fondo global del documento (`body`, secciones base). |
| `surface-container-lowest` | `#0A101F` | Secciones alternas (Portafolio, Footer) para separar bloques de contenido. |
| `surface-container-low` | `#101A30` | Contenedor base de tarjetas de servicio, formularios glassmorphic y barras de métricas. |
| `surface-container` | `#14213D` | **Innovaia Navy** — Superficie activa, tarjetas en hover, inputs y chips tecnológicos. |
| `surface-container-high` | `#1D2E52` | Contenedores de iconos, cabeceras flotantes, píldoras destacadas y estados `:focus`. |
| `surface-container-highest` | `#273C69` | Bordes iluminados (*rim light*), divisores activos y estados seleccionados. |
| `primary` / `orange-accent` | `#FF6B35` | **Innovaia Orange** — Botones CTA, enlaces en hover, puntos de atención y acentos principales. |
| `primary-light` / `amber-accent` | `#FF885B` | Estado hover de botones naranjas, degradados de texto y brillos secundarios. |
| `primary-dark` | `#D94E1F` | Estado `:active` / presionado en botones y bordes de alto contraste. |
| `navy-glow` | `#2E5BFF` | Luz ambiental azulada sutil para efectos 3D de respaldo sobre bloques `#14213D`. |
| `on-surface` | `#F1F5F9` | Texto de cuerpo principal con lectura descansada sobre fondos oscuros. |
| `on-surface-variant` | `#94A3B8` | Subtítulos, descripciones de tarjetas y etiquetas de formulario. |
| `outline` | `#64748B` | Texto secundario, placeholders y metadatos. |
| `outline-variant` | `#233559` | Bordes sutiles de tarjetas (`border-outline-variant/40`). |

---

### 2.3 Degradados y Efectos de Iluminación (Gradients & 3D Glows)

Inspirados en la pieza visual `Navy × Orange`, los elementos clave combinan superficies sólidas con luz ambiental difusa:

- **Gradiente Hero / Texto Destacado:**
  ```css
  background: linear-gradient(90deg, #FFFFFF 0%, #FF885B 50%, #FF6B35 100%);
  ```
- **Gradiente de Superficie Navy (Tarjetas Premium):**
  ```css
  background: linear-gradient(145deg, #1A2B4E 0%, #14213D 60%, #0D1629 100%);
  ```
- **Resplandor Naranja (CTA & Hover Glow):**
  ```css
  box-shadow: 0 0 30px rgba(255, 107, 53, 0.40);
  ```
- **Resplandor Dual Navy × Orange (Fondos de Sección):**
  - Orbe Navy: `rgba(20, 33, 61, 0.65)` con `blur(140px)`
  - Orbe Orange: `rgba(255, 107, 53, 0.15)` con `blur(140px)`

---

### 2.4 Accesibilidad y Contraste (WCAG 2.1)

| Combinación | Ratio de Contraste | Nivel WCAG | Uso Aprobado |
| :--- | :--- | :--- | :--- |
| `#FFFFFF` sobre `#14213D` (Innovaia Navy) | **15.4 : 1** | **AAA** | Texto de titulares, cuerpo y etiquetas sobre tarjetas Navy. |
| `#FFFFFF` sobre `#050811` (Obsidian Void) | **19.8 : 1** | **AAA** | Texto general sobre fondo principal. |
| `#FF6B35` sobre `#050811` (Obsidian Void) | **7.2 : 1** | **AAA (Large) / AA** | Acentos, etiquetas, iconos, enlaces y subtítulos destacados. |
| `#FF6B35` sobre `#14213D` (Innovaia Navy) | **5.6 : 1** | **AA** | Chips tecnológicos, iconos y enlaces sobre contenedores Navy. |
| `#050811` sobre `#FF6B35` (Innovaia Orange) | **7.2 : 1** | **AAA** | Texto oscuro de alto impacto sobre botones primarios `#FF6B35`. |

---

## 3. Sistema Tipográfico: **Univers**

### 3.1 Filosofía Tipográfica

**Univers** (creada por Adrian Frutiger en 1957 y actualizada en **Univers Next**) es el referente histórico del diseño neo-grotesco suizo. A diferencia de otras sans-serif, **Univers** fue concebida desde su origen como un sistema tipográfico unificado y modular: sus proporciones racionales, apertura de contrapunzones y neutralidad técnica transmiten precisión ingenieril y modernidad atemporal.

### 3.2 Stack Tipográfico (Web & Corporativo)

Para garantizar fidelidad absoluta tanto en entornos con licencia corporativa instalada como en navegadores web públicos, se define el siguiente stack con fallback geométrico/neo-grotesco en Google Fonts:

```css
--font-sans: 'Univers Next', 'Univers LT Std', 'Univers', 'Plus Jakarta Sans', 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-mono: 'JetBrains Mono', monospace;
```

### 3.3 Equivalencia de Pesos Univers (Sistema Frutiger → CSS)

| Nomenclatura Univers | Peso CSS (`font-weight`) | Aplicación en INNOVAIA |
| :--- | :--- | :--- |
| **Univers 45 Light** | `300` | Textos introductorios extensos o citas ejecutivas. |
| **Univers 55 Roman** | `400` | Cuerpo de texto (`body-lg`, `body-md`, `body-sm`), párrafos descriptivos. |
| **Univers 65 Bold** | `500` / `600` | Subtítulos (`headline-md`, `headline-sm`), navegación (`label-md`), chips y botones. |
| **Univers 75 Black** | `700` / `800` | Titulares de alto impacto (`headline-xl`, `headline-lg`) y métricas clave (`18+`, `99.9%`). |

### 3.4 Escala Tipográfica (Type Scale)

| Token | Tamaño (`font-size`) | Interlineado (`line-height`) | Tracking (`letter-spacing`) | Peso | Uso |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `headline-xl` | `48px` (`56px` desktop) | `56px` (`64px` desktop) | `-0.025em` | `700` (65/75) | Hero H1 y títulos principales de sección. |
| `headline-lg` | `36px` | `44px` | `-0.015em` | `700` (65/75) | Títulos de productos en portafolio y KPIs numéricos. |
| `headline-md` | `24px` | `32px` | `-0.01em` | `600` (65 Bold) | Títulos de tarjetas de servicio (`H3`). |
| `headline-sm` | `20px` | `28px` | `-0.005em` | `600` (65 Bold) | Marca en cabecera y subtítulos destacados. |
| `body-lg` | `16px` | `24px` | `0em` | `400` (55 Roman) | Subtítulos de sección e introducciones. |
| `body-md` | `14px` | `20px` | `0em` | `400` (55 Roman) | Texto descriptivo estándar en tarjetas y formularios. |
| `body-sm` | `12px` | `16px` | `0.005em` | `400` (55 Roman) | Notas al pie, garantías NDA y microcopy. |
| `label-md` | `14px` | `20px` | `0.01em` | `600` (65 Bold) | Botones CTA, enlaces de navegación y títulos de features. |
| `label-sm` | `12px` (`11px` badges) | `16px` | `0.04em` | `600` (65 Bold) | Píldoras superiores, tags tecnológicos y etiquetas de campo. |

---

## 4. Espaciado, Layout y Bordes

### 4.1 Tokens de Espaciado

| Token | Valor | Equivalencia px | Uso |
| :--- | :--- | :--- | :--- |
| `space-xs` | `0.25rem` | `4px` | Separación interna mínima (icono-texto compacto). |
| `space-sm` | `0.5rem` | `8px` | Gaps entre chips, padding interno de píldoras. |
| `space-md` | `1rem` | `16px` |Separación estándar entre elementos relacionados. |
| `space-lg` | `1.5rem` | `24px` | Grid gap entre tarjetas y padding de contenedores medianos. |
| `space-xl` | `3rem` | `48px` | Padding vertical de secciones y separación de bloques mayores. |
| `gutter` | `1.5rem` | `24px` | Margen lateral responsivo de contenedores (`max-w-7xl`). |

### 4.2 Radios de Borde (`borderRadius`)

- `DEFAULT`: `0.25rem` (`4px`) — Botones ejecutivos, inputs y chips técnicos.
- `lg`: `0.5rem` (`8px`) — Contenedores de iconos y sub-tarjetas de características.
- `xl`: `0.75rem` (`12px`) — Tarjetas de servicio y barra de métricas.
- `2xl`: `1rem` (`16px`) — Showcases de portafolio y contenedor principal de formulario.

---

## 5. Especificación de Componentes UI

### 5.1 Botón Primario (High-Energy Orange CTA)
- **Fondo:** `bg-brand-orange` (`#FF6B35`) con transición a `hover:bg-amber-accent` (`#FF885B`).
- **Texto:** `text-pure-white` o `text-absolute-black` en peso `600`/`700` (`Univers 65 Bold`).
- **Sombra:** `shadow-[0_0_30px_rgba(255,107,53,0.4)]`.
- **Interacción:** Elevación sutil `hover:-translate-y-0.5` y aumento de brillo ambiental.

### 5.2 Botón Secundario (Innovaia Navy Surface)
- **Fondo:** `bg-surface-container` (`#14213D`) con borde `border border-outline-variant/60`.
- **Hover:** `hover:bg-surface-container-high` (`#1D2E52`) y `hover:border-brand-orange/50`.
- **Texto:** `text-pure-white` con icono en `#FF6B35`.

### 5.3 Tarjetas de Servicio y Portafolio (Navy Elevated Cards)
- **Superficie Base:** `#101A30` (`bg-surface-container-low`) con transición en hover a `#14213D` (`bg-surface-container`).
- **Borde:** Borde biselado sutil `#233559` (`border-outline-variant/40`), iluminándose en hover con gradiente `from-brand-orange/25`.
- **Chips Tecnológicos:** Fondo `#14213D` (`bg-surface-container`) con texto `#FF6B35` (`text-brand-orange`) o `#FF885B` (`text-amber-accent`).

### 5.4 Inputs y Controles de Formulario
- **Fondo:** `#14213D` (`bg-surface-container`) sobre tarjeta `#101A30`.
- **Focus:** `focus:bg-surface-container-high` (`#1D2E52`) + anillo `focus:ring-1 focus:ring-brand-orange`.
- **Placeholder:** `#64748B` (`placeholder-outline`).

