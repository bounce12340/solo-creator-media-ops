# Posting slots

## Phase 1: slot test (<START_DATE> to <END_DATE>)
Rotate candidate slots one per day. Other wakes exit silently.

| Date | Slot | Item | Actual time | Off-slot? | 24h views | 72h views |
|---|---|---|---|---|---|---|
| <YYYY-MM-DD> | <SLOT_A> | | | | | |
| <YYYY-MM-DD> | <SLOT_B> | | | | | |
| <YYYY-MM-DD> | <SLOT_C> | | | | | |

At the end, compare median 24h and 72h views per slot, excluding off-slot
and deviating days. The creator picks the fixed slot.

## Phase 2: fixed slot
- Fixed slot: <HH:MM TZ>
- Catch-up check: <HH:MM TZ> (about 1 hour later, dedupe first)
