# joshuakravitz.com

Personal website built with [Astro](https://astro.build/) using the [AstroPaper](https://github.com/satnaing/astro-paper) theme. Deployed on Netlify.

## Quick Start

```bash
npm install        # install dependencies (first time or after pulling new deps)
npm run dev        # start dev server at localhost:4321
npm run build      # production build to ./dist/
npm run preview    # preview production build locally
```

## Common Tasks

### Add a Blog Post

Create a new `.md` file in `src/data/blog/`:

```markdown
---
author: Joshua Kravitz
pubDatetime: 2026-03-21T12:00:00Z
title: "Your Post Title"
slug: your-post-title
featured: false
draft: false
tags:
  - some-tag
description: "A short description for SEO and post listings."
---

Your post content here. Standard markdown works.
```

- `slug` determines the URL: `/posts/your-post-title/`
- Set `draft: true` to hide a post from the site
- Set `featured: true` to pin it to the Featured section on the homepage
- Tags create automatic tag pages at `/tags/tag-name/`

### Update the Bio

The bio appears in two places:

1. **Homepage hero** -- edit `src/components/Hero.astro` (the paragraph text in the `<div class="space-y-3">` block)
2. **About page** -- edit `src/pages/about.md` (plain markdown)

Keep them in sync, or make the about page a longer version.

### Update Interests / Education

Edit the `interests` and `education` arrays at the top of `src/components/Hero.astro`.

### Add a Project or Publication

Edit `src/pages/projects.astro`. Projects and publications are separate arrays at the top of the file:

```typescript
// Add to the projects array:
{
  title: "Project Name",
  description: "What it does.",
  url: "https://github.com/...",
  tags: ["tag1", "tag2"],
}

// Add to the publications array:
{
  title: "Paper Title",
  year: 2026,
  abstract: "The abstract text.",
  authors: "Author One, Author Two, ...",
  publication: "Journal Name",
  url: "https://doi.org/...",
  tags: ["tag1"],
}
```

### Update Social Links

- **Homepage hero icons** (email, Twitter, Scholar, GitHub, LinkedIn, CV): edit `socialLinks` in `src/components/Hero.astro`
- **Footer/header icons**: edit `SOCIALS` in `src/constants.ts`

### Update Resume

Replace `public/files/resume.pdf` with the new file.

### Update Site Metadata

Edit `src/config.ts` -- title, description, author, timezone, etc.

### Update Navigation

Edit the `<ul id="menu-items">` in `src/components/Header.astro`.

## Deployment

The site auto-deploys via **Netlify** on push to `master`.

- Build command: `npm run build`
- Publish directory: `dist/`
- Config: `netlify.toml`
- Contact form submissions go to the Netlify Forms dashboard

Branch deploys (like `astro-migration`) get preview URLs automatically.

## Key Files

| File | What it controls |
|---|---|
| `src/data/blog/*.md` | Blog posts |
| `src/components/Hero.astro` | Homepage hero (bio, photo, social links, interests, education) |
| `src/pages/about.md` | About page |
| `src/pages/projects.astro` | Projects & publications |
| `src/pages/contact.astro` | Contact form |
| `src/config.ts` | Site title, description, settings |
| `src/constants.ts` | Social links (footer/header) |
| `src/styles/global.css` | Colors, layout width, base styles |
| `src/components/Header.astro` | Navigation menu |
| `public/files/resume.pdf` | Resume PDF |

## Colors & Theming

Light/dark mode colors are in `src/styles/global.css` as CSS variables. The accent color is `#006cac` (light) and `#ff6b01` (dark).

## Built on AstroPaper

Based on [AstroPaper](https://github.com/satnaing/astro-paper) by Sat Naing. Licensed under MIT.
