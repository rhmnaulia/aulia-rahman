# aulia-rahman

Personal site and blog. Built with Astro 5, Tailwind CSS v4, MDX, and Shiki. Static HTML/CSS only — zero client JavaScript. Charter serif for headings, Geist Sans for body, Geist Mono for code.

No custom domain yet. Spent all my money on running gear.

## Dev

```bash
pnpm install
pnpm dev       # localhost:4321
pnpm build     # static output in dist/
```

## New post

Create an `.mdx` file in `src/content/posts/`:

```mdx
---
title: "Post Title"
description: "Short description for SEO and previews."
date: 2026-02-08
tags: ["topic"]
draft: false
---

Content here. Supports markdown, code blocks, tables, etc.
```

Set `draft: true` to hide a post without deleting it.

## New project

Create an `.mdx` file in `src/content/projects/`:

```mdx
---
title: "Project Name"
description: "What it does."
url: "https://example.com"
repo: "https://github.com/rhmnaulia/example"
stack: ["Astro", "Tailwind"]
---
```

## Deploy

Cloudflare Pages. Every push to `main` triggers a build and deploy automatically.
