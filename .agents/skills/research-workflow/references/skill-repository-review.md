# Review agent-skill catalogs and repositories

Use this guide when a user asks to find, compare, adapt, or install reusable agent skills. It complements the general research workflow; it is not a blanket security audit or permission to install skills.

## 1. Define the capability gap

- State the task or recurring problem the skill should improve.
- Inspect the available skills and project instructions before adding another capability.
- Prefer improving an existing skill when the new behavior belongs to its scope. Keep a separate skill when it has a distinct trigger, task, dependencies, or maintenance boundary.

## 2. Triage catalogs efficiently

- Treat an “awesome skills” list as a discovery index. Its descriptions are leads, not evidence that a skill works or fits.
- Search by the user's task and environment, then shortlist candidates that address the capability gap. Do not fetch every linked repository when the catalog already reveals that most entries are unrelated.
- Inspect the original maintained repository for each serious candidate. Confirm that the advertised skill file exists and read the actual skill and any relevant references or scripts.
- Separate catalog curation, project ownership, and individual skill authorship. A catalog's license does not automatically apply to linked skills.

## 3. Evaluate each candidate

Record only evidence that changes the decision:

- **Fit:** task trigger, expected outcome, supported environment, and overlap with existing skills.
- **Provenance and currency:** author or official team, original source path, release or commit date, and maintenance signals.
- **License:** repository license and any file-level notices; unresolved terms mean do not copy or redistribute content.
- **Dependencies:** required CLI, MCP, API account, model, credentials, browser, package, or paid service; distinguish required from optional.
- **Permissions and data flow:** filesystem, network, browser, credentials, external writes, and any data sent to a service.
- **Skill quality:** specific description that says what it does and when it applies; concise entrypoint with progressive disclosure; no machine-specific paths; tools and dependencies scoped to the actual task.
- **Evidence limits:** source inspection, documentation claims, tests, and live behavior are different evidence. Do not infer tested quality from inclusion, stars, or polished wording.

For a comparison, use a compact table: candidate | fit | evidence and maintenance | dependencies/permissions | license | disposition.

## 4. Adapt or install deliberately

- Prefer an original, focused formulation of useful ideas over copying a whole upstream skill. Attribute sources and record what was adapted in the owning repository's provenance file.
- Keep existing authorization boundaries. Research or a recommendation alone does not authorize installing a skill, adding dependencies, granting permissions, changing global settings, or publishing a repository.
- If installation is explicitly requested, inspect the install target first, preserve existing files, install only the selected skill, and verify discovery and any non-sensitive required checks.
- Give each candidate a clear disposition: **adapt**, **install**, **defer**, or **skip**, with a concise reason and any unresolved limitation.

## 5. Report the result

Summarize the user's capability gap, the strongest reusable ideas, what already covers them, the chosen disposition, exact evidence inspected, and any remaining blocker. Label static instruction review separately from behavior tested in a real task. Do not claim productivity, accuracy, or cost improvements without measured evidence.
