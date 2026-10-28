# Publishing flow and checks

## Queue
- **(default)** One main post per day, taken only from approved items in the
  publish queue (`templates/publish-queue.md`).
- Posting off-slot or adding an extra post breaks the slot test. If the
  creator asks for it, remind them first, then mark the item "off-slot" so the
  data reviewer can exclude it.

## Slot test, then a fixed slot
- Rotate a few candidate slots for a fixed period (for example three slots
  over three weeks). The data reviewer records 24h and 72h views per post and
  compares medians at the end.
- After the creator picks a fixed slot, run one posting wake at the slot and
  one catch-up check about an hour later. Remove the extra wakes.

## Platforms handled by the creator (default)
- The creator uploads and schedules TikTok by hand. The post enters the
  metrics log only after it actually goes live.

## The three checks (every platform, every post)
1. **Dedupe before posting.** Open the account page (or API) and confirm this
   item is not already posted. Catch-up runs do this first, too.
2. **Read back after pasting.** After inserting the caption, read the field
   back and compare it to the source file character for character,
   including line breaks and the last hashtag.
3. **Press post once, then confirm one post.** If the result is unclear,
   check the account page instead of pressing again. About 20 minutes later,
   confirm there is exactly one copy.

## On failure
- Any check fails: stop on that platform, report it to the creator, move on
  to the next platform only if it is independent.
- **Never repost automatically.** A repost needs a fresh decision.
- The posting report lists each platform's URL and the result of each of the
  three checks.

## Small edits after approval
Allowed without re-approval: typos, punctuation, line breaks, fixing a broken
link to the same target, hashtag order, music-credit formatting. Everything
else (claims, numbers, quotes, title, hook, legally sensitive wording, any
video edit) needs re-approval. Log small edits next to the queue item.

## Browser posting tips
- Upload one platform at a time.
- Insert caption files in one go, never type them key by key.
- Refuse "leave page?" dialogs while an upload is running; wait for the
  platform's "shared" confirmation.
