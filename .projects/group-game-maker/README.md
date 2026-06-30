# Group Game Maker Experiment

Date started: 2026-06-29 PDT
Owner: NED
Workspace: `/Users/moonk/.openclaw/workspace/task-worktrees/viral-product-experiments-group-game`
Prototype surface: `docs/friend-group-show/` (`ShowDrop`)

## Product thesis

People are more likely to share a tiny web game when their friends, group-chat roles, profile images, or fictional personas are visibly inside the game. The share hook is not “take my quiz”; it is “you are in this.”

## MVP experiment

Adapt ShowDrop from a generic fake-show generator into a friend-profile/persona mini-game maker:

1. Creator picks a genre/template.
2. Creator adds 3–8 cast members with names, personas, and optional emoji/profile-image URLs.
3. App generates a mobile-first fake-show package: poster, episode hook, cast roles, relationship board, and locked Episode 2.
4. Creator shares/copies the link or claims a role to unlock Episode 2.
5. Recipient opens the link, sees the group/personas, and is prompted to make their own version.

## Current implementation state

- Static, no-backend prototype exists in `docs/friend-group-show/index.html`.
- This experiment branch adds profile/persona framing plus optional avatar/image URL fields.
- No secrets, accounts, private chat import, or external APIs are required.

## Key constraints

- Consent-friendly only: do not scrape friend profile images or private chat content.
- Avoid humiliating or accusatory results; output should feel playful, affectionate, and fictional.
- No login for the first experiment.
- Share links can preserve names/personas/avatar URLs, but local uploaded files are not part of this slice.

## Primary decision to make after the test

Do we see enough creation + sharing intent to justify building a richer game-template engine and real analytics backend?
