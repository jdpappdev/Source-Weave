# Sources and provenance

This repository formulates a first-party research workflow from existing user-selected practices and internal workflow assets. It does not vendor upstream skills, code, prompts, or media.

## Internal workflow assets used as design inputs

- Workspace routing and handoff practices: the user's workflow workspace map, including Development, Creative Studio, and Video Digest ownership.
- `transcript-to-experiment`: practice for distinguishing demonstrations, anecdotes, empirical claims, and speculation; checking decision-changing claims; and designing scoped experiments.
- `youtube-digest`: practice for timestamped video notes, transcript coverage checks, optional visual evidence, and distinguishing observed content from inference.
- OpenAI Whisper: optional speech-recognition companion used by the Video Digest project when captions are unavailable and the user explicitly opts in. Source code and model weights are not included in Source-Weave; users install the optional dependency and model separately. Whisper transcripts remain machine-generated evidence and may omit or hallucinate words.
- `apply-tutorial`: practice for turning a selected tutorial into a project-specific implementation handoff, inspecting prerequisites, adapting outdated steps, and verifying outcomes.
- Reusable workflow templates: task briefs, handoffs, evidence records, and measurement rules.

These assets informed the structure and routing boundaries. Their text and implementation files are not copied into this repository. Companion skills remain independently maintained and optional.

## Upstream references

No upstream repository or third-party skill text, examples, code, or assets are included in this repository. The optional companion reference below is documented for attribution; no Whisper code or weights are redistributed here.

- OpenAI Whisper, https://github.com/openai/whisper (release `v20250625`, MIT; checked 2026-11-14). Adapted only as an optional companion recommendation for local timestamped speech transcription in Video Digest. Source-Weave does not bundle or redistribute its code or model weights.

## Distribution

Original Source-Weave content is distributed under the MIT License in [LICENSE](LICENSE). This does not grant rights to redistribute third-party materials. Recheck upstream terms before adapting or bundling external content.
