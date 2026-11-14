# Video research fallback review — November 14, 2026

## Scope

Review the research-workflow instructions after adding an optional Whisper path
to the separate Video Digest project. Baseline: repository `70d4aff` (before this
change). Candidate: working tree on November 14, 2026. This is a static
instruction review; no agent behavior was replayed.

## Representative cases

| Case | Baseline result | Candidate result | Change | Evidence |
| --- | --- | --- | --- | --- |
| Video has platform captions | Use video-digest; check transcript coverage and relevant frames | Prefer supplied/platform captions, keep coverage and frame checks | Clarifies captions remain first choice | Baseline and candidate `research-workflow/SKILL.md`; Video Digest fetch path |
| Video has no captions | Use available video-digest; no explicit local transcription route | Allows local Whisper only when explicitly enabled; preserve machine-generated label and verify important quotes where practical | Adds a useful optional route and uncertainty handling | Video Digest README flags; `scripts/transcribe_whisper.py` provenance schema |
| Tutorial relies on slides/code | Inspect relevant frames and state what was reviewed | Same requirement remains | No intended change | Baseline and candidate video bullet; companion `youtube-digest` guidance |

## Judgment

Static review: **keep**, with behavior still unverified. The candidate preserves
caption-first use, visual inspection, and coverage caveats while making the
fallback opt-in and clearly separating generated speech text from human review.
No quality, speed, or credit improvement is claimed. Live fallback behavior and
real-audio accuracy require runtime access and remain untested because Windows
Application Control blocked the available Python runtime.
