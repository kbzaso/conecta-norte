# Conecta Norte

Landing page institucional para el programa **Conecta Norte** — una iniciativa de vinculación entre estudiantes universitarios y la industria regional del norte de Chile.

## Stack

- **Framework**: [Astro](https://astro.build) v5
- **Estilos**: Tailwind CSS v4 via `@tailwindcss/vite`
- **Animaciones**: `tailwind-animations`
- **Package manager**: pnpm

## Estructura del proyecto

```
/
├── public/
│   ├── favicon.svg
│   └── logo_nav.svg
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── Hero.astro          # Sección principal / hero
│   │   ├── WhatIs.astro        # Qué es Conecta Norte
│   │   ├── Program.astro       # El programa
│   │   ├── StudentRoute.astro  # Ruta del estudiante
│   │   ├── Requirements.astro  # Requisitos de postulación
│   │   ├── Industry.astro      # Aliados / industria
│   │   ├── CTAIndustry.astro   # CTA para empresas
│   │   ├── Form.astro          # Formulario de postulación
│   │   └── Welcome.astro       # Shell: nav + secciones + footer
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css          # Tokens de color y tema (@theme)
└── package.json
```

## Comandos

| Comando        | Acción                                          |
| :------------- | :---------------------------------------------- |
| `pnpm install` | Instala dependencias                            |
| `pnpm dev`     | Servidor de desarrollo en `localhost:4321`      |
| `pnpm build`   | Genera el sitio de producción en `./dist/`      |
| `pnpm preview` | Previsualiza el build antes de desplegar        |

## Design System

Los tokens de color se definen en `src/styles/global.css` con `@theme` y se consumen como utilidades Tailwind:

| Token      | Hex       | Uso                              |
| ---------- | --------- | -------------------------------- |
| `north`    | `#2c1d4d` | Fondo oscuro principal           |
| `sky`      | `#603bff` | Morado de marca / interactivo    |
| `sand`     | `#e8e0ff` | Texto claro sobre fondos oscuros |
| `terra`    | `#e88900` | Acento cálido                    |
| `accent`   | `#ffaa5c` | Destacado / CTAs                 |
| `electric` | `#332df9` | Azul eléctrico profundo          |
| `verde`    | `#8bc4d5` | Verde azulado / acento secundario|
| `surface`  | `#f9f9f9` | Fondo claro de página            |

Tipografía: **Montserrat** (aplicada globalmente en `body`).
