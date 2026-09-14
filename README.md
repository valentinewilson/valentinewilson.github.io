# valentinewilson.github.io

Personal portfolio + blog, built with [Astro](https://astro.build), Tailwind CSS, and MDX.

## Project structure

```text
/
├── src/
│   ├── components/       # Nav, Footer
│   ├── layouts/          # Layout.astro (shared page shell)
│   ├── content/blog/     # blog posts (.md / .mdx)
│   ├── content.config.ts # blog collection schema
│   └── pages/
│       ├── index.astro   # home
│       ├── projects.astro
│       └── blog/
│           ├── index.astro
│           └── [...slug].astro
└── astro.config.mjs
```

## Commands

| Command             | Action                                      |
| -------------------- | -------------------------------------------- |
| `npm install`         | Install dependencies                          |
| `npm run dev`          | Start local dev server at `localhost:4321`    |
| `npm run build`        | Build production site to `./dist/`            |
| `npm run preview`       | Preview the production build locally           |

## Writing a new blog post

Add a new `.md` or `.mdx` file to `src/content/blog/`:

```md
---
title: "Post Title"
description: "One-sentence summary."
date: 2026-01-01
tags: ["tag-one"]
---

Post content goes here.
```

Set `draft: true` in the frontmatter to keep a post out of the listing and homepage until it's ready.

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and publishes it to GitHub Pages at `https://valentinewilson.github.io`.

**One-time setup after pushing this repo to GitHub:** go to the repo's **Settings → Pages** and set **Source** to **GitHub Actions**.
