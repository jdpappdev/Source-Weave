# Architecture

Source-Weave is a local-first collection of agent instructions and optional research-record templates. The skill coordinates source selection, evidence handling, synthesis, and handoff. Research tools and specialist skills are supplied by the agent environment.

## Components

- **Agent skill (`.agents/skills/research-workflow/`)** — portable instructions for web, repository, video, and supplied-file research.
- **Skill references (`.agents/skills/research-workflow/references/`)** — optional formats for a durable research brief and source log. They are not required for ordinary answers.
- **Skill-repository review guide** — optional procedure for triaging large skill catalogs and inspecting shortlisted original sources, licenses, dependencies, and permissions.
- **Catalog (`CATALOG.md`)** — purpose, optional companions, and maturity of the repository's reusable skill.
- **Provenance (`SOURCES.md`)** — internal design inputs and boundaries around upstream content.
- **Documentation (`docs/`)** — review records and documentation notes as the project evolves.

## Workflow

```text
User question
      │
      ▼
Research skill ───── selects ─────► Available source tools
      │                                   │
      │ routes when useful                ▼
      ├────────► YouTube Digest       Source evidence
      ├────────► Transcript experiment     │
      └────────► Tutorial handoff         ▼
                                   Synthesis and next action
```

The skill does not make network requests or read project files on its own. It asks the compatible agent to use the available tools. Optional companion skills remain independently installed and maintained. Video Digest may use local Whisper when explicitly enabled to produce timestamped speech evidence; Whisper and its weights are not bundled here.

## Why there is no MCP server

The current capability is a portable workflow, not a searchable reference database or a service requiring a dedicated tool interface. An MCP server would add setup and maintenance without a demonstrated need. Revisit that choice only if the collection grows into structured source records or repeatable research operations that existing agent tools cannot handle well.

## Change boundaries

Keep the core skill concise and portable. Add reusable formats under its `references/` directory only when they solve recurring needs. If the workflow begins relying on a new companion or external source, document its optional status and provenance. Do not claim behavioral improvement from a static review alone.
