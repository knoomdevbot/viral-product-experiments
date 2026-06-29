# Deployment and Monitoring Runbook

Project: Viral Product Experiments
Provider: GitHub Pages
Production repo: https://github.com/knoomdevbot/viral-product-experiments
Production URLs:
- https://knoomdevbot.github.io/viral-product-experiments/
- https://knoomdevbot.github.io/viral-product-experiments/profile-card/
- https://knoomdevbot.github.io/viral-product-experiments/friend-group-show/

## Deploy flow
1. Edit files under `docs/`.
2. Run local static smoke checks with a simple HTTP server.
3. Commit to `main` and push.
4. GitHub Pages serves from `main` `/docs`.
5. Verify public URLs with `curl -L` and browser smoke tests.

## Secrets/config
None. Static MVP uses no API keys and no backend.

## Rollback
Revert the deployment commit and push to `main`, then poll the production URLs until updated.

## Health checks
- `curl -L -s -o /tmp/index.html -w '%{http_code}' https://knoomdevbot.github.io/viral-product-experiments/`
- Repeat for `/profile-card/` and `/friend-group-show/`.
- Browser smoke: generate one artifact in each app, copy/share link, and check console for JS errors.

## Cost
GitHub Pages public repo hosting is expected to be free under normal usage limits. Billing visibility beyond GitHub account settings is not instrumented.

## Product monitoring gaps
- Real product analytics are missing by design for the static MVP.
- Feedback path is `mailto:westcool10@gmail.com`.
- If either MVP receives real traffic, add privacy-safe analytics for page view, generate, share, unlock, and download events.
