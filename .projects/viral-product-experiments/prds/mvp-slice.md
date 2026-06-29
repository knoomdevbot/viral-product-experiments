# MVP Slice: Viral Product Experiments

Last updated: 2026-06-29
Owner: NED

## Goal
Ship working production MVPs for two viral/social AI entertainment ideas as static, no-secret GitHub Pages apps.

## Products

### VibeCard AI
Value proposition: turn lightweight profile/lore inputs into a collectible identity card that users can save and share.

Critical user journey:
1. User selects a card style and enters name, tags, lore, and tone.
2. App generates a polished result card immediately in-browser.
3. User can regenerate, download the card as SVG, copy a native-feeling share caption, and open/copy a reproducible share URL.

Acceptance criteria:
- No server/API key required.
- Result generation works with default and custom inputs.
- Share URL restores the generated state.
- Download exports a real SVG file.
- Works on mobile-width viewport.

### ShowDrop
Value proposition: turn a group into a fictional episodic show package with poster, cast roles, episode beat, relationship board, and social unlock.

Critical user journey:
1. User selects a genre and enters at least three cast members.
2. App generates a show package in-browser.
3. Episode 2 is locked until user copies a share caption/link or claims a role.
4. User can download the poster SVG and restore a share URL.

Acceptance criteria:
- No server/API key required.
- Validation blocks fewer than 3 cast members with useful inline copy.
- Share/claim unlocks Episode 2.
- Share URL restores the generated state.
- Download exports a real SVG poster.

## Metrics / feedback for this static MVP
- Instrumentation: local-only event trail in `localStorage` for prototype QA; production analytics is explicitly deferred because GitHub Pages static hosting has no backend.
- Feedback path: `mailto:westcool10@gmail.com` links on each page with product-specific subject.
- Next instrumentation slice: privacy-safe first-party page/generation/share/download events if either experiment gets real traffic.
