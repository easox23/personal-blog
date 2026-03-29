# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start dev server at localhost:4321
npm run build     # Production build to ./dist/
npm run preview   # Preview production build locally
```

## Architecture

This is an **Astro v6** static blog site targeting `https://ealejo.dev`.

### Content layer

Blog posts live in `src/content/posts/` as `.md` or `.mdx` files. The schema is defined in `src/content.config.ts` and requires:

```yaml
title: string
pubDate: date
description: string
author: string
image:
  url: ../../images/blog/<filename>   # relative path to src/images/blog/
  alt: string
tags: [string]
```

Images referenced in frontmatter go in `src/images/blog/` (processed by Astro's image pipeline). Images embedded inline in post body go in `public/img/`.

### Routing

- `/` → `src/pages/index.astro` — lists all posts sorted by date
- `/posts/<slug>` → `src/pages/posts/[...slug].astro` — individual post, uses `BlogLayout.astro`
- `/tags/<tag>` → `src/pages/tags/[tag].astro` — posts filtered by tag
- `/about` → `src/pages/about.astro`

### Layouts

- `BaseLayout.astro` — full-width dark banner (`bg-base-700`) with logo, `Navigation`, and tagline; wraps content in `max-w-5xl`
- `BlogLayout.astro` — extends BaseLayout; constrains post content to `max-w-2xl mx-auto`

### Styling

Tailwind CSS v4 — **no `tailwind.config.js`**. All configuration is in `src/styles/global.css` using `@theme` directives.

Custom color palette uses oklch format under the `base-*` scale (50–950), a forest/teal/sage green theme. Key tokens:
- `base-700` — banner background (`#384b56` dark teal)
- `base-900` — primary text (`#212b31` near-black navy)

Typography plugin (`@tailwindcss/typography`) is used for prose content. The `prose` class gets `max-w-none` to fill its container rather than using the plugin's default `65ch` cap.

Alpine.js is loaded via CDN in `BaseHead.astro` and used for the Categories dropdown and mobile hamburger menu in `Navigation.astro`.

## Workflow rules

- **Do not `git push` unless the user explicitly asks.** Commit locally as needed, but wait for instruction before pushing.
