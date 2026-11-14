# Sources and provenance

This repository formulates a first-party research workflow from existing user-selected practices and internal workflow assets. It does not vendor upstream skills, code, prompts, or media.

## Internal workflow assets used as design inputs

- Workspace routing and handoff practices: the user's workflow workspace map, including Development, Creative Studio, and Video Digest ownership.
- `transcript-to-experiment`: practice for distinguishing demonstrations, anecdotes, empirical claims, and speculation; checking decision-changing claims; and designing scoped experiments.
- `youtube-digest`: practice for timestamped video notes, transcript coverage checks, optional visual evidence, and distinguishing observed content from inference.
- OpenAI Whisper: optional speech-recognition companion used by the Video Digest project when captions are unavailable and the user explicitly opts in. Source code and model weights are not included in Source-Weave; users install the optional dependency and model separately. Whisper transcripts remain machine-generated evidence and may omit or hallucinate words.
- Hugging Face Transformers.js and the Xenova Whisper ONNX models: optional browser route used by Video Digest to transcribe selected local audio without PyTorch. The browser runtime and selected model are fetched from public hosts when used; no code or weights are bundled in Source-Weave. Audio is processed in the browser and only the generated transcript JSON is sent to the local loopback server.
- `apply-tutorial`: practice for turning a selected tutorial into a project-specific implementation handoff, inspecting prerequisites, adapting outdated steps, and verifying outcomes.
- Reusable workflow templates: task briefs, handoffs, evidence records, and measurement rules.

These assets informed the structure and routing boundaries. Their text and implementation files are not copied into this repository. Companion skills remain independently maintained and optional.

## Upstream references

No upstream repository or third-party skill text, examples, code, or assets are included in this repository. The optional companion references below document attribution and implementation boundaries; Source-Weave does not redistribute their code or model weights.

- OpenAI Whisper, https://github.com/openai/whisper (release `v20250625`, MIT; checked 2026-11-14). Referenced as the optional local timestamped speech-recognition companion in Video Digest.
- Hugging Face Transformers.js, https://github.com/huggingface/transformers.js (version `3.8.1`, Apache-2.0; checked 2026-11-14). Referenced for browser-based ONNX speech inference; its runtime is fetched by Video Digest rather than bundled here.
- Xenova Whisper ONNX models, https://huggingface.co/Xenova/whisper-tiny.en (Apache-2.0; checked 2026-11-14). Referenced as the browser route's downloadable model source; model files are not bundled in Source-Weave.

## Distribution

Original Source-Weave content is distributed under the MIT License in [LICENSE](LICENSE). This does not grant rights to redistribute third-party materials. Recheck upstream terms before adapting or bundling external content.
