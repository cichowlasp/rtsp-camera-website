# RTSP Camera — Website

Promotional website for the **RTSP Camera** app (turn your phone into a private IP camera). Built with [Astro](https://astro.build) + Tailwind CSS v4.

## Structure

```
src/
  pages/
    index.astro         # Landing page
    [slug].astro        # Renders legal content (privacy)
  components/
    Welcome.astro       # Hero + features + gallery
    Navigation.astro    # Sticky nav + theme toggle
    Footer.astro        # Footer
  content/legal/
    privacy.md          # Privacy Policy (served at /privacy)
public/
  CNAME                 # Custom domain (GitHub Pages)
  favicon.svg / *.png   # App icon
```

## Develop

```sh
pnpm install
pnpm dev          # http://localhost:4321
pnpm build        # builds to ./dist
pnpm preview      # preview the production build
```

## Deploy

The `.github/workflows/deploy.yml` action deploys to **GitHub Pages** on every push to `main`. The custom domain is set in `public/CNAME` (`rtsp-camera.cichowlasp.org`).

## To-do before launch

- [ ] Replace the App Store URL (`idYOUR_APP_ID`) in `Welcome.astro` with the real one.
- [ ] Swap the placeholder screenshot cards in `Welcome.astro` for real screenshots.
- [ ] Replace the placeholder support email (`cichowlas.p@gmail.com`) in `privacy.md` / footer.
