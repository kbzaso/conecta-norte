# Conecta Norte — Project Guidelines

## Stack

- **Framework**: Astro (`.astro` components)
- **Styling**: Tailwind CSS v4 via `@tailwindcss/vite` — configured in `src/styles/global.css` using `@theme`
- **Animations**: `tailwind-animations` package (`animate-fade-up`, `animate-float-card`, `animate-float`)
- **Images**: Always use `<Image>` from `astro/components` for optimization
- **Package manager**: pnpm

## Design System

### Color Tokens (use Tailwind utilities, not raw hex)

| Token      | Value     | Usage                          |
|------------|-----------|--------------------------------|
| `north`    | `#2c1d4d` | Primary dark background        |
| `sky`      | `#603bff`  | Brand purple / interactive     |
| `sand`     | `#e8e0ff`  | Light text on dark backgrounds |
| `terra`    | `#e88900`  | Warm accent                    |
| `accent`   | `#ffaa5c`  | Highlight / CTA color          |
| `electric` | `#332df9`  | Deep electric blue             |
| `verde`    | `#8bc4d5`  | Teal / secondary accent        |
| `surface`  | `#f9f9f9`  | Light page background          |

### Typography

- Font: **Montserrat** (set globally on `body`)
- Headings: `font-black` for heavy titles, `italic font-light` for elegant emphasis
- Tracking: `tracking-wide` or `tracking-widest` for uppercase labels
- Body text: `text-[1.1rem] leading-[1.7]`

### Spacing & Layout

- Max content width: `max-w-300` (container class)
- Section padding: `px-8 py-8` mobile, `lg:py-24` desktop
- Use Tailwind's default spacing scale — avoid arbitrary values unless necessary

### Component Patterns

- Sections use `relative overflow-hidden` with `z-10` on content and `absolute` for decorative elements
- Decorative blobs: `absolute rounded-full pointer-events-none` with radial gradients
- Cards: `bg-gradient-to-br from-sky/35 to-north/85 border border-sand/15 rounded-3xl backdrop-blur-md`
- CTAs: `bg-accent text-north font-bold uppercase tracking-[0.05em] rounded-sm`
- Pills/badges: `border border-sky/40 rounded-full` or `bg-north/90 rounded-full`

### Background Images

- Use `<Image>` with `object-cover` + `opacity-*` for background images with opacity control
- Wrap in `<div class="w-full h-full absolute inset-0">` and add `z-10` to overlapping content

### Animations

- Entrance: `animate-fade-up` with `animation-delay:0.Xs` staggered per element
- Floating UI: `animate-float` (hero image), `animate-float-card` (floating cards)
- Hover transitions: `transition-[transform,box-shadow] duration-200 hover:-translate-y-0.5`

## General Rules

- Prefer editing existing components over creating new files
- Keep components focused — one section per `.astro` file
- Use semantic HTML elements (`<section>`, `<h1>`, `<p>`, `<a>`)
- No inline styles — use Tailwind utilities or `<style>` scoped blocks
- Opacity on colors via Tailwind slash syntax: `text-sand/75`, `bg-north/90`
