# Agent-skill catalog review — November 27, 2026

## Scope

Reviewed VoltAgent's Awesome Agent Skills catalog as a discovery source for improving Source-Weave and the user's reusable research workflow. The catalog describes 1,000+ skills; this review does not claim to inspect every linked skill repository. It checked the catalog's scope and quality notes, then selected research- and skill-quality-relevant entries for closer inspection.

## Evidence inspected

- VoltAgent catalog README and quality criteria: task-specific skill descriptions, progressive disclosure, portable paths, and scoped tools.
- Catalog note that each listed skill is independently maintained and is not audited or guaranteed.
- Catalog entries for Notion research documentation and Trail of Bits' underspecified-request guidance; these point to specialized tools and are not being installed or copied.
- Existing Source-Weave research workflow, templates, repository boundaries, and companion-skill documentation.

## Static review cases

| Case | Existing guidance | Candidate guidance | Judgment | Evidence |
| --- | --- | --- | --- | --- |
| User supplies a large skills catalog | General repository research checks README, license, history, setup, and implementation | New guide treats catalog descriptions as discovery leads and narrows candidates to the capability gap | More specific triage without attempting to inspect unrelated entries | Existing and revised `research-workflow/SKILL.md`; new reference |
| User asks to adopt a listed skill | Existing guidance does not explicitly distinguish catalog license from each linked skill's terms | New guide checks original source, file-level terms, dependencies, permissions, data flow, and overlap before recommending a disposition | Adds boundaries that prevent blind copying or installation | New skill-repository review guide and VoltAgent repository license/disclaimer |
| User wants a reusable capability integrated into Source-Weave | Existing workflow routes research and optional specialist skills | New guide prefers focused original adaptation, requires provenance, and keeps install/publish actions within authorization | Fits Source-Weave's portable and optional-companion design | README, architecture, and source provenance changes |

## Judgment

**Keep as a focused extension to the research workflow.** This is a static instruction review, not a behavior comparison. The skills catalog informed discovery and quality criteria; no third-party skill content was imported. Test the new workflow on a future skills repository review before claiming improved research quality or efficiency.
