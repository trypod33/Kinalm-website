# Kinalm Website

Public website repo for Kinalm — a warmer, simpler caregiving app for families.

This repository hosts the public-facing Kinalm marketing site, published via GitHub Pages from the `docs/` folder.

## Structure

- `index.html` — source copy of the site
- `docs/index.html` — the file actually served by GitHub Pages

Both files are kept in sync. When updating site content (new release highlights, version numbers, download links), update both files.

## Current version

The site currently reflects **Kinalm v2.5.0**. Update the following when cutting a new release:

- `<title>` tag and meta description
- "Now available: Kinalm vX.X.X" pill in the hero
- Download button `download="Kinalm-vX.X.X.apk"` attributes
- "View release notes" / "Open GitHub release" links (`releases/tag/vX.X.X`)
- "What's new in vX.X.X" section copy and release highlights list
- Footer version string
