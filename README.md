# Sparkle - 成果發表網站

> 2026/5/18 | 臺北市立建國高級中學 | 自由入場

Sparkle 成果發表會官方網站，展示各學科領域的專題研究成果。

**Live:** https://sparkle-site.github.io/

## Pages

| Page | Description |
|:-----|:------------|
| **首頁** `/` | Hero, stats, highlights, category links |
| **專題** `/projects/` | 29 projects across 6 categories with JS filtering |
| **流程** `/schedule/` | Event timeline and venue info |
| **關於** `/about/` | About the event, team intro, contact |
| **分工** `/team/` | Staff list organized by team |

## Categories

數學 (3) · 物理 (6) · 化學 (7) · 生物 (6) · 資訊 (6) · 地科 (1)

## Tech

- **Astro** - static site generator (build only, no runtime)
- **HTML / CSS / JS** - no frontend framework
- **GitHub Pages** - deployed from `docs/` via GitHub Actions

## Deploy

The site is pre-built. The `docs/` folder contains the static output and is deployed automatically on push to `main`.

To rebuild after editing source files:

```sh
npm install
npm run build
cp -r dist/ docs/
```

Then commit and push.

## Project Structure

```
src/
  layouts/
    BaseLayout.astro    # Shared layout (nav, footer, global CSS)
  pages/
    index.astro         # Homepage
    about.astro         # About page
    schedule.astro      # Schedule & venue
    team.astro          # Staff list
    projects/
      index.astro       # Project gallery with filters
docs/                   # Built static files (deployed to GitHub Pages)
```
