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
- `curl -L` returned HTTP 200 for all three URLs.
- Page titles verified:
  - `Viral Product Experiments`
  - `VibeCard AI — Prototype`
  - `ShowDrop — Prototype`

## Operational notes
- Static prototypes only: no server, no database, no secrets.
- GitHub Pages is public and HTTPS-enforced.
- Updating deployment: edit files under `docs/`, commit to `main`, push to GitHub.
- Rollback: revert the relevant commit and push to `main`.
- Cost: GitHub Pages for this public static repo should be free under normal GitHub Pages limits.
