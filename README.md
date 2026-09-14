# valentinewilson.github.io

Personal portfolio, built with [Astro](https://astro.build) and Tailwind CSS.

## Project structure

```text
/
├── src/
│   ├── components/       # Nav, Footer
│   ├── layouts/          # Layout.astro (shared page shell)
│   └── pages/
│       ├── index.astro      # home
│       ├── experience.astro
│       └── projects.astro
└── astro.config.mjs
```

## Commands

| Command             | Action                                      |
| -------------------- | -------------------------------------------- |
| `npm install`         | Install dependencies                          |
| `npm run dev`          | Start local dev server at `localhost:4321`    |
| `npm run build`        | Build production site to `./dist/`            |
| `npm run preview`       | Preview the production build locally           |

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and publishes it to GitHub Pages at `https://valentinewilson.github.io`.

**One-time setup after pushing this repo to GitHub:** go to the repo's **Settings → Pages** and set **Source** to **GitHub Actions**.
