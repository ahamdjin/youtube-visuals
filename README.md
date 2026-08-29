# YouTube Visuals

A tiny Astro site for creating clean HTML/CSS visuals, comparison cards, diagrams, timelines, and explainer graphics for YouTube videos.

## Stack

- Astro
- Plain CSS
- `astro-icon` + Lucide icons
- Local or official brand logos
- Static output for Vercel

No React, Tailwind, database, CMS, or client-side JavaScript is required.

## Run locally

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

Vercel can import this repository directly and auto-detect Astro.

## Structure

```text
src/
├── components/
│   ├── BrandLogo.astro
│   ├── ComparisonCard.astro
│   └── FeatureRow.astro
├── data/
│   └── visuals.ts
├── layouts/
│   ├── BaseLayout.astro
│   └── VisualLayout.astro
├── pages/
│   ├── index.astro
│   └── visuals/
│       └── managed-vs-vps.astro
└── styles/
    └── global.css
```

## Adding a new visual

1. Create a new page in `src/pages/visuals/`, for example:

```text
src/pages/visuals/hermes-memory.astro
```

2. Use `VisualLayout.astro` and any reusable components.
3. Add the visual to `src/data/visuals.ts` so it appears on the homepage.

Each file automatically becomes a route:

```text
src/pages/visuals/hermes-memory.astro
→ /visuals/hermes-memory
```

## Design rules

- Black and white first
- Large text readable in a YouTube video
- 16:9 visual canvas on desktop
- Minimal borders and spacing
- Real brand logos where useful
- Lucide line icons for generic concepts
- Avoid gradients and unnecessary decoration

## Current visuals

- `/visuals/managed-vs-vps` — Managed Hermes vs VPS Hermes
