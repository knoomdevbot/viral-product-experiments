# Deployment Notes

Date: 2026-06-29
Provider: GitHub Pages
Repository: https://github.com/knoomdevbot/viral-product-experiments
Pages source: `main` branch, `/docs` directory

## Public URLs
- Index: https://knoomdevbot.github.io/viral-product-experiments/
- AI profile-card experiment: https://knoomdevbot.github.io/viral-product-experiments/profile-card/
- AI friend-group show experiment: https://knoomdevbot.github.io/viral-product-experiments/friend-group-show/

## Verification
- `curl -L` should return HTTP 200 for all three URLs after each push.
- Expected page titles after the MVP deployment:
  - `Viral Product Experiments — Working MVPs`
  - `VibeCard AI — Working MVP`
  - `ShowDrop — Working MVP`
- Browser smoke checklist:
  - VibeCard generates a card, exposes a production share URL, and creates SVG markup.
  - ShowDrop validates fewer than 3 cast members, generates Episode 1, unlocks Episode 2 after share/claim, exposes a production share URL, and creates SVG markup.

## Operational notes
- Static MVPs only: no server, no database, no secrets.
- GitHub Pages is public and HTTPS-enforced.
- Updating deployment: edit files under `docs/`, commit to `main`, push to GitHub.
- Rollback: revert the relevant commit and push to `main`.
- Cost: GitHub Pages for this public static repo should be free under normal GitHub Pages limits.
