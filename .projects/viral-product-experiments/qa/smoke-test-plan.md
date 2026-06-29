# Smoke Test Plan: Viral Product Experiments

Environment: production GitHub Pages URLs.

## VP-INDEX
Steps: open index, verify both product links are visible and navigate correctly.
Expected: VibeCard and ShowDrop cards link to their production routes.

## VC-CORE
Steps: open VibeCard, change name/tags/lore/tone/style, click generate.
Expected: result card renders, no console errors, action buttons visible.

## VC-SHARE-DOWNLOAD
Steps: copy/share link, reload with URL params, download SVG.
Expected: restored state matches generated card; SVG file downloads.

## SD-VALIDATION
Steps: open ShowDrop, remove cast until fewer than 3, generate.
Expected: inline validation explains at least 3 cast members are required.

## SD-CORE-UNLOCK
Steps: enter 3+ cast, generate, try Episode 2 before share, copy share or claim role, generate Episode 2.
Expected: show package renders; Episode 2 remains locked until social action, then unlocks.

## SD-SHARE-DOWNLOAD
Steps: copy/share link, reload with URL params, download SVG.
Expected: restored state matches generated show; SVG poster downloads.
