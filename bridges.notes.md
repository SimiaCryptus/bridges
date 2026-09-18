# Bridges — Implementation Notes

## Overview

Bridges (Hashiwokakero-inspired connection game) rendered on arbitrary
hex/tiling boards using Three.js/WebGL. Entry point: `index.html`, logic in
`src/main.js`.

## Navigation

- Added a persistent "← Home" link (top-right corner) on the game page so
  players can return to the site root (`/`) at any time.
- Styled via `.home-link` in `styles/main.css`: fixed position, blurred
  translucent panel consistent with the HUD's visual language, hover state
  matching existing button styles.
- Uses a plain anchor tag rather than a button since it performs navigation,
  not an in-page action.

## Structure

- `index.html`: sets up canvas (`#gl`), HUD aside (`#hud`), settings dialog
  (`#settings`), toast container (`#toasts`), and now the home link.
- `styles/main.css`: dark theme, HUD/settings dialog styling, responsive
  tweaks under 720px width.
- `src/main.js`: ES module, imports three.js via import map from CDN.

## Follow-ups

- Confirm the site root path (`/`) matches the actual deployment structure;
  adjust href if games are served from a subpath instead.
- Consider adding the same home link pattern to other games for consistency.
