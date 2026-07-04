# Personal Blog

Personal blog built with [Astro](https://astro.build/) using
[Astro Cactus](https://github.com/chrismwilliams/astro-theme-cactus), configured for static
deployment on [Vercel](https://vercel.com/).

## Commands

```bash
pnpm install
pnpm dev
pnpm build
pnpm preview
pnpm check
```

## Vercel

This project is a static Astro site. It does not need the `@astrojs/vercel` adapter unless you
later add server-rendered pages or Vercel-specific services.

`vercel.json` pins the deployment settings:

```json
{
	"installCommand": "pnpm install --frozen-lockfile",
	"buildCommand": "pnpm build",
	"outputDirectory": "dist"
}
```

After importing the repo in Vercel, use the Astro framework preset or leave framework detection
enabled. Vercel will install with pnpm, run the production build, and publish `dist`.

## Site Config

Update site metadata in `src/site.config.ts`:

- `url`: production domain, for sitemap, RSS, canonical URLs, and Open Graph images.
- `title`: site name shown in the header and metadata.
- `author`: footer and feed author.
- `description`: default SEO description.

The current default URL is `https://personal-blog.vercel.app/`. Change it after creating the
actual Vercel project or adding a custom domain.

## Content

Add posts in `content/posts` and notes in `content/notes`.

Posts require frontmatter like:

```md
---
title: "My First Post"
description: "A short description for SEO and previews."
publishDate: "2026-07-03"
tags: ["astro", "blog"]
---
```

Notes require frontmatter like:

```md
---
title: "A Note"
description: "Optional note description."
publishDate: "2026-07-03T00:00:00-04:00"
---
```

## Attribution

This site is based on Astro Cactus by Chris Williams. See `LICENSE` for the original MIT license.
