# Product Requirements Document (PRD): trackr.

**Version:** 1.1.0
**Framework:** Angular 21 (Standalone, Signals, New Control Flow)
**Design System:** Engineering-Focused (Vercel/Linear Style)
**Primary Color Palette:** Slate-900 / Indigo-500

---

## 1. Visión y Nombre
**Nombre:** trackr. (tipografía monoespaciada, peso bold)
**Eslogan:** Track what matters. Ship faster.
**Misión:** SaaS MVP para desarrolladores que permite registrar eventos, marcar progreso y visualizar métricas con una API limpia y sin fricción.

---

## 2. Stack Técnico Estricto
* **Frontend:** Angular 21.
* **Componentes:** 100% Standalone (Sin `NgModule`).
* **Estado:** Angular Signals para toda la reactividad del Dashboard.
* **Control Flow:** `@if`, `@for`, `@switch` obligatorio.
* **Estilos:** Tailwind CSS.
* **Iconos:** Lucide Angular.
* **Fuentes:**
  - Headlines: Serif con carácter editorial (Georgia o similar).
  - UI/Cuerpo: DM Sans o Outfit.
  - Código/Logo: JetBrains Mono o Fira Code.

---

## 3. Arquitectura de Carpetas
```text
src/
├── app/
│   ├── core/                  # Singleton services (State, Auth)
│   │   └── services/          # trackr-logic.service.ts (Signals)
│   ├── features/              # Smart Components (Pages)
│   │   ├── landing/           # Landing Page modularizada
│   │   └── dashboard/         # Panel de métricas y registro
│   ├── shared/                # Dumb Components (UI Kit)
│   │   └── ui/                # Navbar, Footer, Buttons, Cards, Snippets
│   ├── app.config.ts          
│   └── app.routes.ts          
└── styles.css                 # Tailwind + Custom Typography
```

---

## 4. Contenido de la Landing Page (Guía de Copy)

### 01 — Navegación

- **Logo:** trackr.
- **Links:** Features, Docs, Pricing, GitHub.
- **CTA:** Start free → (Fondo #0F172A, borde sutil indigo).

### 02 — Hero Section

- **Headline:** Track what matters. Ship faster.
- **Subheadline:** Registra elementos, marca progreso y visualiza métricas en una API limpia, sin fricción. Para desarrolladores que odian el ruido.
- **Snippet decorativo (ventana de terminal):**

```typescript
import { trackr } from '@trackr/sdk'
trackr.register('user:onboarded', { userId: '42' })
trackr.progress('feature:setup', 60)
```

### 03 — Propuesta de Valor (Features Grid)

- **Register:** Registra cualquier evento (SDK para Node, Python, Go).
- **Track Progress:** Marca el progreso en tiempo real (Hitos y Webhooks).
- **Visualize:** Métricas que hablan solas (Dashboards automáticos).

### 04 — Precios

- **Free ($0):** Side projects, 1K eventos, 7 días retención.
- **Pro ($19):** Equipos pequeños, eventos ilimitados, 30 días retención.
- **Team ($79):** Organizaciones, dashboards ilimitados, SSO, retención 90 días.

### 05 — Open Source & Footer

- **Sección:** "100% open source. 100% tuyo." (Star on GitHub / Self-host guide).
- **Footer:** Links de API Reference, Changelog, Terms. © 2025 trackr.

---

## 5. Especificaciones de UI/UX (Voz del Producto)

- **Tono:** Directo, técnico, sin "fluff". Inglés para términos técnicos, español para el discurso.
- **Colores:**
  - Fondo: `#0F172A` (slate-900)
  - Texto: `#F8FAFC` (slate-50)
  - Acento: `#6366F1` (indigo-500)
- **Dashboard View:** Debe mostrar una tabla de elementos con timestamps, barras de progreso y mini gráficos de líneas en tiempo real.
