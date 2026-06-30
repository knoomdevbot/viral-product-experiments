# Viral Product Experiments

Working production MVPs for two static, mobile-first viral/social entertainment experiments.

## Production URLs

- Index: https://knoomdevbot.github.io/viral-product-experiments/
- VibeCard AI: https://knoomdevbot.github.io/viral-product-experiments/profile-card/
- ShowDrop: https://knoomdevbot.github.io/viral-product-experiments/friend-group-show/

## MVP capabilities

### VibeCard AI
- In-browser collectible profile/result card generation.
- Card style, target, name, vibe tags, lore, tone, and regeneration seed.
- Restorable share URL using query parameters.
- Copyable share caption.
- Downloadable SVG artifact.
- Local-only prototype event trail in `localStorage`.

### ShowDrop
- In-browser friend-profile/persona web game generation.
- Genre slate, group type, premise, and 3–8 cast members.
- Cast members support name, persona/tiny lore, and optional emoji or image URL avatar.
- Inline validation for insufficient cast.
- Poster, Episode 1 hook, cast roles, relationship board.
- Social unlock via copied share/caption or role claim before Episode 2.
- Restorable share URL and downloadable SVG poster.

## Deployment

Hosted on GitHub Pages from `docs/` on `main`. No backend, no secrets, no paid infrastructure.

## Limitations / next slice

- No server-side persistence or real analytics yet.
- SVG export is intentionally lightweight; PNG export and native social share images are next-slice items.
- Feedback is via mailto links until a backend/form is added.
