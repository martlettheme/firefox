# Martlet for Firefox

## Test locally

Run `npm run build`. Open `about:debugging#/runtime/this-firefox`, choose **Load Temporary Add-on**, and select `theme/manifest.json`. The temporary theme is removed when Firefox restarts. Use Firefox 142+ and test both appearance modes.

## Package

Build produces `dist/martlet-firefox.zip` for Mozilla Add-ons submission. Light and Dark are bundled together using `theme` and `dark_theme`; Firefox selects the appropriate variant. No JavaScript, permissions, tracking, fonts, or remote assets. This is an unsigned source archive; permanent installation requires Mozilla signing, which is not done yet. Store listing, screenshots, signing, and publication remain to do. The manifest declares no data collection. These colors apply to browser UI, not arbitrary website content.

These are generated distributions of [Martlet Theme](https://martlettheme.dev/), version 1.0.0. Canonical colors and generators live in [martlettheme/martlettheme](https://github.com/martlettheme/martlettheme). The source repository may require maintainer access. This repository includes a complete color snapshot in source.json and can build without access to that repository.

MIT license. Copyright 2026 James P. Howard, II.

## Maintenance

Edit the canonical palette and generator upstream, then run npm run build there. The complete distribution directories are emitted under artifacts/repositories/. Sync the relevant directory into this repository. To reproduce a snapshot here, run npm run build, then npm test. Node.js 22 or newer is used in CI. No registry publication runs automatically.
