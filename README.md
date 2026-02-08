# Personal Blog

A minimal personal blog built with Astro, React, Tailwind CSS, and shadcn/ui. Warm aesthetics, clean typography, fast page loads.

## Tech Stack

- **Astro 5** — Static site framework with zero JS by default
- **React** — Interactive islands (theme toggle, tag filter)
- **Tailwind CSS v4** — Utility-first styling
- **shadcn/ui** — Minimal component library (Button, Badge, Card, DropdownMenu)
- **Geist** — Font family for body and code
- **sugar-high** — 1KB syntax highlighter with CSS variable theming
- **Content Collections** — Type-safe markdown/MDX with Zod schemas

## Development

```bash
pnpm install
pnpm dev        # Start dev server at localhost:4321
pnpm build      # Build for production
pnpm preview    # Preview production build
```

## Adding Blog Posts

Create a new `.mdx` file in `src/content/posts/`:

```mdx
---
title: "My New Post"
description: "A short description for previews and SEO."
date: 2025-03-01
tags: ["topic"]
draft: false
---

Your content here. Supports full markdown and MDX.
```

### Frontmatter Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `title` | string | yes | Post title |
| `description` | string | yes | Short description for cards and meta tags |
| `date` | date | yes | Publication date |
| `tags` | string[] | no | Tags for categorization (default: `[]`) |
| `draft` | boolean | no | Set to `true` to hide from production (default: `false`) |

## Customization

### Colors

Edit the CSS variables in `src/styles/global.css` under `:root` (light) and `.dark` (dark) selectors.

### Fonts

Fonts are imported via `@fontsource-variable` packages. Change them in `global.css` under the `@theme` block.

### Syntax Highlighting

Sugar-high colors are defined as `--sh-*` CSS variables in `global.css`. They automatically switch with light/dark mode.

## Deployment

Run `pnpm build` and deploy the `dist/` directory to any static host (Vercel, Netlify, Cloudflare Pages, etc.).

Update the `site` URL in `astro.config.mjs` before deploying — it's used for RSS, sitemap, and canonical URLs.

## Future

- Add a CMS (Tina, Decap, etc.) — content files are already compatible
- Add image optimization with `astro:assets`
- Add search functionality
