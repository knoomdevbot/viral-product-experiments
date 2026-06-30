# Experiment: Friend-profile web game maker

Date: 2026-06-29 PDT
Product surface: ShowDrop / `docs/friend-group-show/`

## Hypothesis

A creator is more likely to share a generated web game when the game visibly includes their friends, group-chat personas, or profile-image-like avatars, because the share message becomes personal: “you are in this.”

## Target audience

Initial wedge: US Gen Z / young-adult friend groups who already share group-chat jokes, memes, personality results, TikTok links, or party-game prompts.

Secondary wedge: fandom / creator communities that use fictional personas, OCs, or recurring cast archetypes.

## Critical user journey

1. Land on ShowDrop.
2. Understand within 5 seconds that it turns friends/personas into a playable fake show.
3. Choose a quick template.
4. Add or edit 3–8 cast members with persona traits and optional emoji/image URL.
5. Generate the game package.
6. Copy share link, claim a role, or download the poster.
7. Recipient opens the shared game and understands they can make their own version.

## Variant under test

### Variant A — Friend-profile framing

Hero promise: “Put your friends inside the game.”

Inputs:
- name
- persona / tiny lore
- emoji or image URL

Generated output:
- poster with visible cast avatars
- Episode 1 hook
- cast role cards
- relationship board
- Episode 2 locked until share/role claim

## Success thresholds for first manual seed test

Use a very small seed: 10–20 people or 3–5 friend groups.

Green-light signals:
- 60%+ of testers can generate a game without help.
- 30%+ click/copy share, claim a role, or download a poster.
- At least 2 recipients independently say they would send it to a friend/group chat.
- At least 1 recipient asks to make their own version.

Yellow-light signals:
- People like the concept but setup feels too slow.
- Users use personas/emoji but avoid profile images.
- Recipients enjoy the output but do not understand the “make mine” loop.

Kill or pivot signals:
- Users find friend-image/persona use creepy even with manual entry.
- Share intent is under 10% after completion.
- Output feels generic even with friend names/personas.

## Acquisition seed

Manual only for the first experiment:
- Send prototype to a small friend/community sample.
- Ask each tester to make one group show with fictional or consent-friendly names/personas.
- Ask whether they would send it to the actual group chat.

Suggested prompt:

> I’m testing a tiny web-game idea: make a fake show starring your friend group. Can you try it with 3–5 nicknames/personas and tell me whether you’d send the result to the group chat?

## Safety/permission rules

- Do not ask testers to upload/scrape real social profile images.
- Profile image URLs are optional; emoji/personas are acceptable substitutes.
- Encourage nicknames and fictionalized traits.
- Avoid sexual, hateful, bullying, or reputation-damaging outputs.

## Decision rule

If the first manual seed test clears green-light share/remix signals, build the next slice:
- real event analytics;
- “make your own version” CTA on shared links;
- 2–3 more game templates;
- image upload with local preview and explicit consent copy;
- generated 9:16 share card PNG.
