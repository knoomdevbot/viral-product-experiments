# Metrics plan: Group Game Maker / ShowDrop

Date: 2026-06-29 PDT

## North-star learning metric

Shared-game starts per completed generated game.

For this static prototype, true shared-link attribution is deferred; first test uses manual observation plus local event trail.

## First-slice prototype events

Current static prototype logs local-only events in `localStorage.showdrop_events`:

- `quick_start_selected`
- `cast_member_added`
- `universe_generated`
- `episode2_unlock_viewed`
- `episode2_generated`
- `download_clicked`
- `restored_from_link`

## Funnel questions

1. Do users understand the promise?
   - manual: ask “what do you think this does?” after first screen.
2. Can users generate a game?
   - event/manual: `universe_generated`.
3. Do users personalize with personas/images?
   - manual: count edited cast members and whether avatar/image fields are used.
4. Do users show share intent?
   - event/manual: copied share link, claimed role, downloaded poster, or said they would send it.
5. Do recipients want to make their own?
   - manual: ask recipients whether they would remix with their own group.

## Backend analytics needed if experiment graduates

Privacy-safe event names:

- `game_started`
- `template_selected`
- `cast_member_added`
- `avatar_field_used` — boolean only, do not send image URL.
- `game_generated`
- `share_link_copied`
- `poster_downloaded`
- `role_claimed`
- `episode2_unlocked`
- `shared_link_opened`
- `remix_started`

Properties:

- `template_slug`
- `genre_slug`
- `cast_count`
- `has_avatar_count` — count only.
- `ref` / `campaign` slug.
- `session_id` anonymous random ID.

Never collect:

- friend names;
- image URLs;
- raw personas/traits;
- private chat content;
- contact lists.

## Manual test scorecard

For each tester/group record:

- Tester type: friend group / creator / fandom / other.
- Generated without help: yes/no.
- Cast count.
- Used emoji/avatar/image field: none / emoji / image URL.
- Share intent: no / maybe / yes.
- Recipient reaction: confused / amused / wants remix / concerns.
- Biggest friction.
- Best line/output.
