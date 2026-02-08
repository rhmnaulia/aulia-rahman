# aulia-rahman

Personal site. Astro, Tailwind, MDX, Shiki. No client JS.

## Dev

```bash
pnpm install
pnpm dev
pnpm build
```

## New post

Add `.mdx` to `src/content/posts/`:

```mdx
---
title: "Post Title"
description: "Short description."
date: 2026-02-08
tags: ["topic"]
---

Content here.
```

## Deploy

Cloudflare Pages. Pushes to `main` auto-deploy.
