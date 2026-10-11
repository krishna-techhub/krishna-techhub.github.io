# Krishna Tech Hub — Developer Website & Policies

## Project Overview
Official GitHub Pages developer portal (`https://krishna-techhub.github.io`) showcasing 3 Android apps, serving privacy policies, terms of service, and Google AdMob `app-ads.txt` crawler compliance.

## Applications
- **PDF Hub : PDF Editor & Tools** (`com.pdfhub`) — Policy: `pdf-hub-privacy-policy.html`
- **QR Hub : Ultimate QR & Barcode Studio** (`com.qr.hub`) — Policy: `qr-hub-privacy-policy.html`, Terms: `qr-hub-terms.html`
- **ScrollCount : Reels & Shorts Tracker** (`com.techhub.scrollcount`) — Policy: `scrollcount-privacy-policy.html`

## Architecture & Directory Structure
- `index.html`: Main developer showcase landing page (Vercel/Linear dark theme, glassmorphism, responsive down to 320px).
- `assets/brand/`: Official brand emblem, logos, and web icons:
  - `krishna-tech-hub-neon-logo.png`: High-resolution official neon emblem.
  - `header-k-icon.png`, `glossy-k-icon.png`: Header and card icons.
  - `favicon.ico`, `favicon-32x32.png`: Root and branding favicons.
- `assets/apps/`: App-specific assets organized by slug:
  - `pdf-hub/`: `icon.png`, `banner.png`, `favicons/` (complete multi-resolution icon kit)
  - `qr-hub/`: `icon.png`, `banner.png`, `favicons/` (complete multi-resolution icon kit)
  - `scrollcount/`: `icon.png`, `favicons/` (complete multi-resolution icon kit)
- `app-ads.txt`: AdMob publisher verification string (`google.com, pub-5378252094188023, DIRECT, f08c47fec0942fa0`).
- `.nojekyll` & `_config.yml`: Prevents Jekyll processing on GitHub Pages to serve root and static assets reliably.
- `favicon.ico`: Root-level W3C standard favicon preventing browser/crawler 404 errors.

## Design System & Coding Standards
- **Aesthetic:** Dark glassmorphism (`rgba(17, 24, 39, 0.75)`, `backdrop-filter: blur(16px)`), modern typography (Inter / Plus Jakarta Sans), neon glowing borders.
- **Responsiveness:** 100% fluid layouts down to 320px mobile viewports (`min-width: 0` on flex items, `@media (max-width: 480px)` and `@media (max-width: 640px)`). Zero horizontal scroll.
- **Zero Build Step:** Plain HTML5, CSS3, and Vanilla JavaScript with progressive enhancement.
- **Interactive Logo Lightbox:** Any `.logo-trigger` element opens the high-res neon logo modal with view/download actions.

## Deployment & Git Workflow
- Hosted via GitHub Pages from repository `krishna-techhub/krishna-techhub.github.io` on branch `main`.
- **Local Testing:** Test by opening `index.html` directly in any browser or running `python -m http.server 8000`.
- **Gotchas & CDN Cache:**
  - The `.nojekyll` file at root prevents Jekyll from skipping directories starting with `_` or dotfiles.
  - GitHub Pages CDN cache updates within ~60–90 seconds after `git push origin main`.
- Deploy commands:
  ```bash
  git add .
  git commit -m "Update site"
  git push origin main
  ```

## New App / Policy Addition Checklist
When adding a new app or policy:
1. Add app asset bundle under `assets/apps/<app-slug>/` (`icon.png`, `favicons/`).
2. Create `<app-slug>-privacy-policy.html` using the existing template layout with `min-width: 0` on flex items.
3. Include `.logo-trigger` on brand icons and inject the Logo Lightbox modal snippet.
4. Add the app card in `index.html` with direct Google Play link and policy page link.
5. Update footer links across all HTML files and verify `app-ads.txt` if AdMob ads are added.

## Contact & Developer Identity
- Developer Entity: Krishna Tech Hub
- Support Email: `krishnatechhub@gmail.com`
- GitHub Organization/Profile: `https://github.com/krishna-techhub`
- Live Website: `https://krishna-techhub.github.io/`
