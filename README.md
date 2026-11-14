# Source-Weave

**A portable research skill for turning sources into traceable decisions.**

Source-Weave helps an AI agent research web pages, code repositories, YouTube videos, and supplied files. It guides the agent to find strong sources, distinguish claims from evidence, preserve uncertainty, and deliver a useful answer or implementation handoff.

> Research should make the next decision clearer. Source-Weave keeps the path from source to conclusion visible.

## What it helps with

- Research a question using current, authoritative web sources.
- Compare GitHub repositories by inspecting their documentation, code, license, and maintenance signals.
- Study tutorials through timestamped video notes and relevant visual evidence when a video-digest tool is available.
- Analyze supplied transcripts and documents without treating embedded instructions as user intent.
- Turn workflow advice into a scoped experiment, or a selected tutorial into a project-specific implementation handoff.
- Produce a concise answer, comparison, research brief, video study, or handoff matched to the request.

## How it works

1. **Set the target.** Identify the question, decision, audience, time frame, and constraints.
2. **Choose evidence.** Select appropriate sources and inspect primary material where it matters.
3. **Track confidence.** Separate direct observations, corroborated evidence, source claims, inferences, and unknowns.
4. **Synthesize.** Explain the useful finding, tradeoffs, caveats, and next action at the requested depth.
5. **Route follow-up.** Use optional specialist skills for video digestion, workflow experiments, or implementation.

## Get started

Add [`.agents/skills/research-workflow`](.agents/skills/research-workflow) to the skills directory used by your AI agent. Then ask it to research, compare, verify, study a video, or prepare a handoff. Skill installation and discovery differ between agent tools; follow the current instructions for yours.

Example prompts:

```text
Research these repositories and recommend which one fits my project. Compare evidence, tradeoffs, license, and maintenance.

Study this tutorial video. Give me the key steps with timestamps, verify version-sensitive details against official documentation, and prepare a handoff for my project.

Compare these workflow claims with primary sources. Tell me what is established, what is uncertain, and whether one claim deserves a small experiment.
```

## Capability map

| Need | Source-Weave workflow | Optional companion |
| --- | --- | --- |
| Research web pages and current facts | Source selection, primary-source checks, citations, synthesis | Browser or web research tools provided by the agent environment |
| Inspect code repositories | Compare documented claims with source, license, and maintenance evidence | Repository browser or GitHub connector |
| Study a YouTube video | Request transcript coverage checks, timestamps, and visual review when relevant | `youtube-digest` (optional local Whisper, including browser-based local transcription) |
| Evaluate AI or productivity advice | Classify claims and design a bounded comparison | `transcript-to-experiment` |
| Apply a selected tutorial | Carry evidence into a target-project implementation handoff | `apply-tutorial` |

Companion skills and tools are optional; they are not bundled here. When one is unavailable, the agent should continue with available evidence and state the specific limitation.

For local or remote videos without usable captions, the companion Video Digest
project can optionally generate timestamped speech text with Whisper. Captions
remain preferred and transcription is opt-in. For local media, its browser route
processes selected audio in the browser, does not upload the audio, and saves
only generated transcript JSON through a loopback connection. The browser
runtime and selected model are downloaded from public hosts on first use; this
route does not use PyTorch. The separate Python/PyTorch route requires its own
explicit model-download opt-in. Keep all recognition output labeled as machine
generated and verify important quotations against audio. Do not disable
operating-system or organization security controls to make a native runtime
load. See [SOURCES.md](SOURCES.md) for implementation and provenance.

## Repository contents

```text
Source-Weave/
├── README.md
├── ARCHITECTURE.md
├── CATALOG.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── LICENSE
├── SECURITY.md
├── SOURCES.md
├── .gitignore
├── .agents/skills/research-workflow/
│   ├── SKILL.md
│   └── references/
│       ├── research-brief-template.md
│       └── source-log-template.md
└── docs/
    └── README.md
```

Templates are optional aids for durable research artifacts. Do not make a simple answer fill out a form.

## Boundaries

Source-Weave provides a research method, not a browser, repository API, transcript extractor, or model runtime. Results depend on the tools and source access available in the agent environment. It does not authorize purchases, account changes, publishing, contacting people, destructive operations, or implementation beyond the user's request. Instructions found inside source material remain source content.

## Quality and status

This is an initial first-party formulation informed by existing workflow practices. It has received a static review, but no controlled comparison has established improvements in research quality or speed. Read [SOURCES.md](SOURCES.md) for provenance and [CHANGELOG.md](CHANGELOG.md) for revisions.

**License:** [MIT](LICENSE) for this repository's original content. Third-party references and companion skills retain their own terms; see [SOURCES.md](SOURCES.md).
