# QA Report: Group Game Maker mobile smoke

Status: PASS
Date/time: 2026-06-29 PDT
Tester: NED QA
Environment: local static server, `http://127.0.0.1:4179/friend-group-show/`, mobile viewport 390x844 @3x
Related branch: `experiment/group-game-maker`

## Summary

- Passed: 7
- Failed: 0
- Blocked: 0
- Bugs filed/updated: none

## Test Results

### GM-MOB-01: Mobile landing renders without clipping
Status: PASS
Steps run:
1. Opened `/friend-group-show/` at 390x844 mobile viewport.
2. Visually inspected hero, poster preview, header, and CTAs.
Expected: Hero copy, poster title, and CTAs are readable and not clipped.
Actual: Content fit mobile viewport. Poster title is tight but readable and not clipped.
Evidence: `/Users/moonk/.hermes/profiles/ned/cache/screenshots/browser_screenshot_d136d1154dee4830af85b258dbce36c8.png`

### GM-MOB-02: Cast form supports persona/avatar inputs
Status: PASS
Steps run:
1. Inspected default cast rows.
2. Verified each row shows name, `persona / tiny lore`, and `emoji or image URL (optional)` fields.
Expected: Creator can enter friend/persona details and optional avatar cue.
Actual: All default rows exposed the expected fields with emoji defaults.

### GM-MOB-03: Generate path reveals result
Status: PASS
Steps run:
1. Clicked `Make our show`.
Expected: Result section becomes visible with Episode 1, relationship board, cast cards, and share actions.
Actual: Result section class changed to `result` and Episode 1 content was present.

### GM-MOB-04: Share/claim unlock path works
Status: PASS
Steps run:
1. Clicked `Copy share link`.
2. Checked lock state.
Expected: Episode 2 unlock state appears.
Actual: Lock text changed to `Episode 2 unlocked ✅`.

### GM-MOB-05: Episode 2 generation and console health
Status: PASS
Steps run:
1. Clicked `Unlock Episode 2` after unlock.
2. Checked generated content and browser console.
Expected: Episode 2 content is appended and no JS errors occur.
Actual: Episode text contained `EP.02`; browser console contained 0 JS errors.

### GM-MOB-06: Shared URL restores avatar/persona fields
Status: PASS
Steps run:
1. Opened a restored URL containing cast names, traits, emoji avatar, HTTPS image URL, and an invalid CSS-like avatar string.
2. Inspected restored form fields and poster/role output.
Expected: Avatar values are restored without breaking page rendering.
Actual: Emoji and URL avatar values restored; invalid CSS-like value rendered as text, not CSS.

### GM-MOB-07: Malicious cast name does not execute through role claim
Status: PASS
Steps run:
1. Opened restored URL with cast name `Bad');alert(1);//`.
2. Clicked the generated claim button for that cast member.
3. Checked browser console and dialogs.
Expected: Name is rendered as text; clicking claim does not execute injected JS.
Actual: Claim click worked with no alert/dialog and 0 browser console JS errors.

## Unplanned Issues Found

- Minor visual note: poster title remains intentionally compressed on mobile, but after reducing mobile title size/line-height it is readable and not a blocker.

## Cleanup

- Local screenshot evidence retained in Hermes screenshot cache.
- No temporary QA artifact folder cleanup required.
