# Operations

## Routines are graded; changes need approval
- Keep a list of every scheduled routine with its schedule, purpose and a
  grade (keep / slow down / merge / remove).
- The orchestrator may propose changes; it applies them only after the
  creator approves. Read a routine's saved prompt before editing it.

## Daily posting routine
- Wakes at the slot and once for a catch-up check. Step 0 of the catch-up is
  the dedupe check. Runs the three checks on every platform
  (`publishing-checks.md`).

## Nightly reconciliation (default 23:30 local)
Compare the publish queue with what is actually live and report only:
- approved items that were missed
- items posted twice
- posts missing their URL in the log
- items missing `review.md` or their score
- leftover scheduled posts that should not be there
Each problem is one Action / Target / Reason block. The routine never posts,
deletes, or edits anything. When everything matches, it stays silent.

## Weekly archive and disk space (default Sunday early morning)
- Videos published at least 3 days ago: upload the final video, captions and
  credits to the archive drive, compare file sizes, and only after a size
  match delete local media files. Text files stay local.
- Excluded: unpublished drafts and tests.
- Clear caches older than 30 days and intermediate files of published
  episodes. Keep a deletion log.
- Ask the creator when disk use is over 60% or an unknown item over 2 GB
  appears.
- Silent when there is nothing to report.

## Handoffs between agents
- Every handoff is sent as high priority and waits for an explicit
  **"taken over" (`已接手`)** reply from the receiving agent.
- A **handoff watchdog** runs twice a day (default 10:00 and 20:00). It
  nudges agents whose handoffs are stuck and contacts the creator only when
  a decision is needed.

## Failure handling everywhere
- Missing source, transcript, number or metric: write `[UNVERIFIED]` at that
  spot, list all such items at the top of the delivery, and stop that item.
- Back up a file before changing it. Deleting needs approval.
- Never turn on a paid service or add a new API key without asking.

## Secrets
- Keys live in environment variables or a secret manager, never in files,
  chats, logs or published repos. Nobody types the creator's passwords for
  them.
