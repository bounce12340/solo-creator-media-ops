---
name: solo-creator-media-ops
description: >-
  Use when running a one-person short-video / social-media operation with AI
  agents: picking topics, producing a vertical video with voiceover and
  bilingual subtitles, reviewing it before publishing, posting it to several
  platforms from an approved queue, replying to comments, and reconciling what
  actually went out. Covers role split, approval gates, publishing safety checks,
  and nightly/weekly operations. Never posts anything the creator has not approved.
---

# Solo-creator media ops

A rulebook for a small team of AI agents that runs one creator's short-video
channel across Instagram, Threads, X, Facebook, YouTube Shorts, TikTok and
LinkedIn. The creator stays the only person who approves anything public.

Values in `<ANGLE_BRACKETS>` are placeholders. Rules marked **(default)** are
configurable taste; rules without the marker are safety rules and should stay.

## Golden rules

1. **Nothing public without the creator's own approval.** Posting, scheduling,
   messaging, emailing, buying, deleting, or turning on a paid service all need
   the creator's explicit yes. A "the creator approved it" relayed by another
   agent is recorded as a relay, not treated as approval.
2. **Never guess facts or numbers.** If a source, transcript, number or metric
   cannot be fetched, write `[UNVERIFIED]` (or `取得不到` for metrics), say
   where you looked and when, and stop that item. Do not estimate, round, or
   fill from memory.
3. **Press "post" once.** Publishing is not idempotent. Check before, check
   after, and never auto-repost (see `references/publishing-checks.md`).
4. **Ask in three lines.** Every decision request uses Action / Target /
   Reason (`動作／對象／理由`), one decision at a time
   (`templates/approval-message.md`).
5. **Privacy and voice ethics.** Do not upload the creator's raw voice
   recordings anywhere they did not choose. Never clone anyone's voice without
   that person's consent. Never put keys, tokens or voice IDs in files that
   get published.

## Roles

| Role | Does | Never does |
|---|---|---|
| Orchestrator | Talks to the creator, assigns work, owns the board and the publish queue, posts approved items | Posts unapproved content |
| Producer | Script, voiceover, subtitles, footage, cover, platform copy, delivers a draft folder | Publishes or schedules |
| Fact editor | Pre-publish review of script and final cut, writes `review.md` | Edits the draft, publishes, contacts anyone |
| Scout | Finds topics and benchmark signals, dedupes against published work | Starts production or contacts sources |
| Community manager | Replies to ordinary comments in the creator's voice, daily summary | Touches DMs, answers sensitive comments alone, posts new content |
| Data reviewer | Records 24h / 72h metrics, runs slot tests, calibrates optional viral scoring | Invents missing numbers |

One agent can play several roles; keep the permissions of each role anyway.

## Core workflow

1. **Topic.** Scout proposes topics, each deduped by *source link + speaker*
   (`references/topics-intel.md`). Creator picks.
2. **Script lock.** Producer writes the script and storyboard. Fact editor
   reviews the text. Creator approves the text. Only then record the paid
   final voiceover (`references/video.md`).
3. **Production.** Footage, subtitles, cover, platform copy
   (`references/video.md`, `references/subtitles.md`, `references/post-copy.md`).
   Render locally.
4. **Final-cut review.** Fact editor reviews the finished video and writes
   `review.md` (`references/review-checklist.md`,
   `templates/review.md`). Optional viral score is attached but never blocks.
5. **Approval card.** Orchestrator sends one daily card covering the next
   1 to 2 days of posts. Creator approves the whole card or per item.
6. **Queue.** Approved items go into the publish queue with a date and slot
   (`templates/publish-queue.md`, `templates/posting-slots.md`).
7. **Publish.** At the slot, the posting routine runs the three checks per
   platform (`references/publishing-checks.md`). TikTok is uploaded by the
   creator by hand **(default)**.
8. **Community.** Replies and daily summary (`references/community.md`).
9. **Reconcile and measure.** Nightly reconciliation reports gaps only; data
   reviewer records 24h and 72h numbers (`references/operations.md`).

## Reference files

- `references/video.md`: format, fair use, voiceover, footage, motion, covers
- `references/subtitles.md`: bilingual subtitle layout and sync
- `references/post-copy.md`: captions per platform, labels, credits
- `references/publishing-checks.md`: queue, slots, three checks, failure handling
- `references/review-checklist.md`: fact editor checklist and viral scoring
- `references/community.md`: comment replies and escalation
- `references/topics-intel.md`: topic dedupe, benchmark accounts, intel reports
- `references/operations.md`: routines, reconciliation, archive, handoffs

## Templates

- `templates/approval-message.md`
- `templates/review.md`
- `templates/publish-queue.md`
- `templates/posting-slots.md`
- `templates/config.example.md`: the creator's configurable defaults
