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

## Why releases live here, not in CareTracker

The app source lives in the private `trypod33/CareTracker` repo. Because
that repo is private, its GitHub Releases (and any direct asset download
links) return 404 for the public. This site is public, so **release APKs
are mirrored here** as GitHub Releases on `Kinalm-website` instead.

### Publishing a new release APK to this site

1. Build and sign the release APK in CareTracker as usual (`./release.sh X.X.X`).
2. Download the `app-release.apk` asset from the CareTracker release
   (requires repo access) and save it locally.
3. Create a matching release here:
   ```bash
   gh release create vX.X.X app-release.apk --title "Kinalm vX.X.X" \
     --notes "See CareTracker changelog for full release notes." \
     --repo trypod33/Kinalm-website
   ```
4. Update the download/release-notes links in `index.html` and
   `docs/index.html` to point at `Kinalm-website/releases/...` (not
   `CareTracker/releases/...`) and push.

If `CareTracker` is ever made public, this mirroring step can be
removed and links can point directly back to it.
