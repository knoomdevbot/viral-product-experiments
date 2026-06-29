# QA Report: Working MVP Smoke

Status: PASS
Date/time: 2026-06-29 local pre-deploy
Tester: NED
Environment: local static server at http://127.0.0.1:4173, production URLs preconfigured in share links
Plan: `.projects/viral-product-experiments/qa/smoke-test-plan.md`

## Summary
- Passed: VP-INDEX, VC-CORE, VC-SHARE-DOWNLOAD static SVG path, SD-VALIDATION, SD-CORE-UNLOCK, SD-SHARE-DOWNLOAD static SVG path
- Failed: 0
- Blocked: 0
- Bugs filed/updated: none

## Evidence
- JS syntax check: `node --check /tmp/profile-card.js` and `node --check /tmp/friend-group-show.js` passed.
- VibeCard browser smoke: generation rendered result, production share URL was generated, SVG markup contained expected content, no console errors.
- ShowDrop browser smoke: malformed query params safely fell back, validation blocks fewer than 3 cast members, generation rendered result, share/claim unlock flow produced `unlocked=1`, Episode 2 rendered after unlock, SVG markup existed, no console errors.
- UI review evidence screenshots:
  - Initial VibeCard review: `/Users/moonk/.hermes/profiles/ned/cache/screenshots/browser_screenshot_cd9706e7faee4b78b54d630b4dd5187d.png`
  - ShowDrop post-fix review: `/Users/moonk/.hermes/profiles/ned/cache/screenshots/browser_screenshot_e6941a6e264a40de8476b206d249c9fa.png`

## UI Review Summary
- VibeCard: launch-blocking carousel clipping fixed by wrapping template pills; card centerpiece upgraded from dashed placeholder styling; production share URL used while local testing.
- ShowDrop: mobile input clipping fixed by stacked cast rows and multiline premise; poster artifact strengthened with show/episode tags and visual scene; relationship board upgraded from plain list to node-style board; production share URL used while local testing.

## Known MVP limitations
- Static-only: no backend persistence, auth, or real analytics.
- Downloads are SVG artifacts, not PNG/native social cards.
- Feedback path is email link.

## Result
MVP smoke and UI checks pass for production deployment.
