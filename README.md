# OrbitGov — Responsive Governance Platform Prototype

A responsive, interaction-rich web prototype for a multi-tenant workforce and
global project governance platform.

This is a **front-end prototype**: all data is mocked in `site/app.js`. There is
no backend, no build step and no dependencies beyond a web font loaded from
Google Fonts.

## Features

- Admin / Lead Manager / Manager role switcher
- Responsive executive dashboard
- Regional command center with a country detail drawer
- Project portfolio table and project publishing flow
- Workforce capacity, org chart and mock Excel ingest validation
- Drag-and-drop Kanban board
- Interactive roadmap / Gantt view
- Light and dark themes (persisted to `localStorage`)
- Desktop, tablet and mobile layouts, with bottom navigation on mobile

## Layout

```
site/            # everything that gets published
  index.html
  styles.css
  app.js
.github/workflows/deploy-pages.yml
```

## Run locally

Serve the `site/` folder with any static server:

```bash
python3 -m http.server 8080 --directory site
```

Then open <http://localhost:8080>.

Opening `site/index.html` directly from the filesystem also works.

## Deploying

The `Deploy to GitHub Pages` workflow publishes the contents of `site/`.

One-time setup, needed before the first successful run:

1. Go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.

The workflow then runs on every push to `main`, and can also be started
manually from the **Actions** tab via **Run workflow**. Until Pages is enabled
the deploy step will fail, since the repository has no Pages site to publish to.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>K</kbd> | Focus global search |
| <kbd>Esc</kbd> | Close the open drawer, modal or mobile sidebar |
