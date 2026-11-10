---
name: instagram-content-machine
description: >
  Runs a weekly Instagram content machine for a business account: blueprint, 100 ideas, 30-day calendar, Reel scripts, growth system, follower-to-client funnel and competitor review, using seven prompts adapted by E82 Studios. Drafts only; a person posts and answers DMs. Use when the user says "instagram content machine", "plan our Instagram", "Instagram calendar", "Reel scripts for our account", "grow our Instagram", or asks to turn Instagram followers into clients.
---

# Instagram Content Machine

Adapted by E82 Studios (@e82studios, https://www.instagram.com/e82studios/) from a public "Claude prompts for Instagram growth" thread. The seven prompts live in [`references/prompts.md`](references/prompts.md).

## Codex and Claude runtime

- Use this skill in Codex or Claude with the tools actually available in the current task. `AskUserQuestion` examples describe the questions, not a required API: use an available question tool within its limits, or ask in chat. Reuse answers and source material already supplied.
- Work in the user-selected project. Read its `about-me.md`, `voice.md` and relevant brand files before personalised work. Confirm the intended author if files conflict or contain starter defaults. Ask for missing facts or run `voice-builder`; never inherit the maintainer's identity, accounts or private files.
- Resolve bundled `references/` relative to this skill folder. For an explicitly requested profile refresh, read and update the canonical `about-me.md`, `voice.md` or `newsletter-voice.md` in place, preserving unrelated user facts and rules. Consumers must reread those canonical files. Use a new filename only for new deliverables that would collide with unrelated existing files. Installation alone never starts an interview or writes files. Do not write persistent learnings unless requested.
- Use supplied evidence first. Verify external claims through available search/source tools when needed. If a source or integration is unavailable, name the missing capability and offer supplied text/export input. Never invent facts, first-person experience, metrics or a successful tool run.
- Connect only services needed for the chosen route through the user's existing account. Never print credentials or overwrite connections. Drafting, saving and reviewing do not authorise publishing, sending messages or changing accounts.
- Never invent follower counts, results or client names; leave `[CLIENT FIGURE]` where a number must come from the user's own data. No follow/unfollow, engagement pods, bought followers or bulk automated DMs.

## Process

1. **Context.** Load the account's files. Ask once for anything missing: the offer, who buys, the booking or lead-magnet link, and weekly hours available.
2. **Blueprint (monthly).** Run prompt 1, then prompt 5. Save as `instagram/plan-YYYY-MM.md`.
3. **Calendar (monthly).** Run prompt 3 on the cadence from the plan. Save as `instagram/calendar-YYYY-MM.md`.
4. **Weekly batch.** Pick the week's slots, run prompt 4 for its Reels and prompt 2 for carousel and Story ideas. Pass each hook through `hook-generator` and each caption through `post-scorer` when installed.
5. **Funnel.** Run prompt 6 once, then reuse its DM reply drafts. A person sends every DM.
6. **Monthly review.** Ask the user for Insights exports and 5-10 competitor accounts' posts; run prompt 7 on that material only. Update the plan.
7. **Review gate.** Before handing over, check every draft against the style rules, list each number with its source, and cut any without one.

## Output

A folder of Markdown drafts: plan, calendar, weekly scripts and captions, DM replies, review notes. Each draft states its CTA and the pillar it serves.

## Verification

- Every draft traces to a calendar slot and a pillar.
- No number without a source; no banned word from the user's style rules.
- The handover says plainly that nothing was posted or sent.
