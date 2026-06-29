# VibeCard AI + ShowDrop FTUX/CUJ UX analysis

Date: 2026-06-29

## Problem statement

The original VibeCard AI and ShowDrop MVPs were technically functional but weak for first-time user testing:

- The first screen explained the idea more than it showed the artifact.
- The critical user journeys started with dense forms and too many choices.
- Output/share controls competed with setup before users understood the reward.
- Mobile-first social sharing context was not strongly reflected in the UI.

## Reference-service heuristic used

Because these experiments are social artifact generators, the useful reference pattern is not a SaaS onboarding page; it is the short-loop consumer creation pattern used by tools like quizzes, filters, profile-card makers, wrapped-style recaps, and social generators:

1. Show the shareable artifact immediately.
2. Offer a safe preset so users never face a blank page.
3. Ask for the fewest inputs needed for personalization.
4. Generate a visually complete result quickly.
5. Make copy/share/download the next obvious action.
6. Preserve restorable links so shared URLs reopen the same artifact.

## VibeCard AI changes

### FTUX analysis

- The first screen needed to answer “what will I get?” visually, not through explanatory text.
- The form needed to feel like “choose a vibe” rather than “fill out a profile.”
- The core artifact should be visible before any generation click.

### Implemented fix

- Rebuilt the first viewport around a large artifact preview and short hero promise: “Make yours. Send it. Watch friends ask for one.”
- Added preset starts: “It’s me,” “Roast a friend,” “Pet aura,” and “Creator card.”
- Changed style choices into compact, tactile chips.
- Kept the existing CUJ complete: preset → edit name/traits/lore → generate → copy caption/link or download SVG.
- Added clipboard fallback for environments where `navigator.clipboard` is unavailable.
- Preserved production restorable share URLs from local testing.
- Improved mobile resilience with min-width fixes, 46px touch targets, and more readable headline line-height.

### Verified CUJs

- Restored card from query params.
- Generated updated card after editing name/traits/lore.
- Produced production share URL while running locally.
- Generated valid SVG markup.
- Generated a share caption containing the card name and URL.

## ShowDrop changes

### FTUX analysis

- The original journey exposed too much setup and output at once.
- First-time users needed to see a fake-show poster/result before committing to the form.
- The post-generation universe should be revealed after the user clicks the primary action, not visible by default.

### Implemented fix

- Rebuilt the first viewport around a dark entertainment-poster visual system.
- Added immediate “Example result / what friends see” poster preview.
- Added quick starts: Friend chaos, Roommate sitcom, Workplace drama, Pet household.
- Unified the primary CTA around “Make our show.”
- Hid the dense share/results panel until generation, reducing first-screen overload.
- Kept the full CUJ: pick quick start/genre → edit cast → make show → copy link/download poster/claim role → unlock Episode 2.
- Added clipboard fallback.
- Preserved restorable production share URLs and query-param restoration.
- Fixed mobile overflow by allowing grid children and inputs to shrink within the viewport.

### Verified CUJs

- First load shows setup and example result without exposing dense output controls.
- “Make our show” reveals Episode 1 output.
- Share URL points to the production GitHub Pages route while local.
- Poster SVG markup is valid.
- Episode 2 remains locked until share/role claim.
- Role claim unlocks Episode 2.
- 390px mobile viewport has no horizontal overflow.

## Remaining research questions for live user testing

- Do users understand whether they are making an artifact for themselves or for a friend group before reading the full form?
- Which preset labels produce the fastest first click?
- Does the VibeCard output feel personal enough without AI API calls?
- Does ShowDrop’s Episode 2 lock create curiosity or confusion?
- Are users more likely to share a copied link, copied caption, or SVG image?
