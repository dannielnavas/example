# Product Requirements Document (PRD): DevexpSass Frontend MVP

**Version:** 1.0.0
**Target Framework:** Angular 21 (Latest)
**Design System:** Vercel/Geist (Strict Zinc Palette)

---

## 1. Visión del Proyecto
DevexpSass es un SaaS técnico minimalista para registrar elementos, marcar progreso y visualizar métricas. La interfaz debe ser extremadamente limpia, profesional y optimizada para desarrolladores, utilizando el lenguaje visual de Vercel.

## 2. Stack Técnico Estricto
* **Framework:** Angular 21.
* **Componentes:** 100% Standalone Components (Prohibido `NgModule`).
* **Estado:** Angular Signals (`signal`, `computed`, `effect`).
* **Control Flow:** Nueva sintaxis nativa (`@if`, `@for`, `@switch`).
* **Estilos:** Tailwind CSS con paleta Zinc.
* **Iconografía:** Lucide Angular.
* **Detección de Cambios:** `ChangeDetectionStrategy.OnPush` en todos los componentes.

## 3. Arquitectura de Carpetas
La IA debe inicializar el proyecto siguiendo esta estructura modular:

```text
src/
├── app/
│   ├── core/                  # Servicios globales y modelos de datos
│   │   ├── services/          # State management con Signals
│   │   └── models/            # Interfaces de Typescript
│   ├── features/              # Componentes de página (Smart)
│   │   ├── landing/           # Hero, Pricing ($3/$99), Features
│   │   └── dashboard/         # Registro de ítems y métricas
│   ├── shared/                # Componentes reutilizables (Dumb)
│   │   └── ui/                # Button, Card, Input, Badge (Vercel Style)
│   ├── app.config.ts          # Configuración de Providers modernos
│   └── app.routes.ts          # Rutas de la aplicación
├── assets/                    # Fuentes Geist y recursos estáticos
└── styles.css                 # Directivas de Tailwind
```

---

## 4. Requisitos de UI/UX (Estilo Vercel)

| Elemento        | Especificación                                      |
|-----------------|-----------------------------------------------------|
| **Fondo**       | `#000000` (Pure Black)                              |
| **Bordes**      | zinc-800 (1px sólido)                               |
| **Texto**       | Principal zinc-100, Secundario zinc-400             |
| **Cards**       | Fondo transparente o zinc-950, borde sutil, sin sombras pesadas |
| **Interactividad** | Hover en botones con transiciones de 150ms       |

---

## 5. Funcionalidades del MVP

### Landing Page

- Sección **Hero** con gradiente sutil
- **Grid** de features
- **Tabla de precios:**
  - **Plan Mensual:** $3 USD
  - **Plan Lifetime:** $99 USD
