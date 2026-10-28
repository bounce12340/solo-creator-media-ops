# Video content

## Format (default)
- Vertical 1080x1920, under 3 minutes.
- **Key-point summary + short original clips.** For interview or talk topics,
  the video is a summary of the key points intercut with short clips from the
  original interview. Do not ship a voiceover-only version when original
  footage exists.
- One clear selling point up front; the first 3 seconds should carry the best
  line from the source when one exists.

## Fair use of original clips
- Keep each clip short, credit the source on screen and in the caption, and
  pair it with your own summary or commentary. No whole-segment reposting.
- Do not buy licences **(default)**. Sources that require a paid formal
  licence (for example, major financial news networks) are not used. If the
  fact editor finds one, it is a must-fix and blocks publishing.
- If you cannot tell whether a source needs a licence, mark it
  `[UNVERIFIED]` and send it to the creator as an Action / Target / Reason
  decision.
- The review lists every clip with start/end time, length and credit line.
- Fair use differs by country. This is an operating rule, not legal advice.

## News
- News videos report the news only. No first-person opinion in the
  creator's voice unless the creator asks for it.
- Do not force a framing (for example, an "AI governance" angle) onto every
  story.

## Voiceover
- **(default)** Language: `<VOICEOVER_LANGUAGE>` (the reference setup uses
  English voiceover with a secondary Chinese subtitle line).
- **(default)** Voice: the creator's own cloned voice `<VOICE_ID>` on
  `<TTS_PROVIDER>`, model `<TTS_MODEL>`, speed 1.0. Never speed the final
  track up.
- Clone only a voice whose owner consented. Do not upload the creator's raw
  recordings to any cloud they did not choose.
- **Lock the script first.** The paid final voiceover is recorded only after
  the fact editor has reviewed the text and the creator approved it. Changing
  a locked script means re-review and re-approval. A free local voice may be
  used for a rough cut; if its model licence is non-commercial, the rough
  track never ships.
- Before a paid re-record, report the estimated credits and get approval.
- When quoting someone who spoke another language, label the line
  "Translated from <LANGUAGE>".

## Footage
- Background footage must match what the line actually means in context,
  not just a keyword in it.
- No brand logos in frame. No real faces behind cards that carry the
  creator's name, handle or opinion (viewers may mistake the stock actor for
  the creator).
- Footage should be bright and moving; avoid static dark backgrounds
  **(default)**.

## Motion for data cards (default)
- Price, cost, benchmark and number-comparison cards are rendered by code,
  frame by frame, as a pure function of time `render_at(t)`: no clocks, no
  unseeded randomness, same frame renders identically twice.
- Hit beats: element entries and cuts land on the music beat; layout changes
  once per bar, not every beat.
- Readability: on-screen text stays at least 0.3 s per character + 0.5 s;
  contrast at least 4.5:1 on every frame; no more than 3 flashes per second.
- Keep a growing BANNED list (for example: purple-blue gradients, glow, lens
  flare, decorative particles, everything fading in at once, everything
  centered, text still moving while being read). Add any default that slips
  into a render. Never remove items.
- Corrections are written in frames ("peak at frame 84 is 2 frames late"),
  not feelings. Fix 1 to 2 items per round.

## Covers
- Cover is packed with visual elements: subject, a big readable hook, a
  supporting visual. It must read at thumbnail size.
- No brand logos on covers either.

## Rendering
- Render locally. Do not send footage to cloud render services
  **(default)**.
- Before export: sample one frame per second for faces and brands, decode
  the whole file without errors, and make an IG copy under about 45 MB.

## Music
- Add background music when possible and record title, source and licence
  in the draft's facts file. Missing music or a missing credit does not
  block publishing.
- Keep music 18 to 22 dB under the voice.
