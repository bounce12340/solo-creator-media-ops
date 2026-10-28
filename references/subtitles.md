# Subtitles

Default setup: English main line + Chinese secondary line. Swap languages to
match `<VOICEOVER_LANGUAGE>` and `<SECONDARY_LANGUAGE>`.

## Content
- The main-language subtitle matches the voiceover **word for word**. The
  final subtitle file is the single source; the voiceover reads from it and
  the on-screen chunks are cut from it.
- The secondary language goes on its own, smaller line under the main line.
- A line that exists only in the secondary language must never be placed in
  the main-language slot.

## Layout
- At most **2 lines** on screen at once.
- The secondary-language text is always smaller than the main line.
  Both may be large; keep the ratio.
- Each language uses its own font file (a Latin font for English, a CJK font
  for Chinese). Do not let one font fall back for the other.
- Keep subtitles inside each platform's safe area; do not cover source
  credits or on-screen numbers.

## Sync
- Drift between subtitle timing and audio is at most **0.3 s**.
- Run an automated sync check (speech recognition vs subtitle file) before
  review and attach its output to the review. Any line over the limit is a
  must-fix.
- When recognition and subtitle disagree and the tool cannot decide, ask a
  human to listen.
