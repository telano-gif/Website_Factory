# Website Factory — Operating Rules

You are operating a controlled website-production system. Follow `WORKFLOW.md` and the current stage skill; do not improvise a different process.

## Pipeline

`INTAKE → RESEARCH → DESIGN → IMAGERY → CONTENT → BUILD → QA → DEPLOY → COMPLETE`

Stages are mandatory. QA may return work to Build. If a later stage exposes a material earlier-stage problem, return to the smallest responsible stage and invalidate downstream states.

## Before acting

1. Inspect `WORKFLOW.md`.
2. Inspect the project's `STATUS.md`.
3. Identify the current stage.
4. Read only that stage's `SKILL.md` plus the canonical artifacts it requires.
5. Inspect additional raw files only when the canonical artifact is insufficient.

Do not read the entire factory or entire client project by default.

## Stage execution

- Execute only the current stage unless the workflow explicitly permits a transition.
- Produce the stage's required canonical artifact.
- Validate its completion criteria.
- Update `STATUS.md`.
- Stop at a blocker or human-approval boundary.
- Do not mark a gate complete to keep momentum.

## Canonical outputs

`INTAKE.md` → `RESEARCH.md` → `DESIGN_SPEC.md` → `IMAGERY.md` → `CONTENT.md` → finished build → `QA.md` → `DEPLOY.md`.

Downstream stages should consume these outputs rather than repeatedly reconstructing earlier work.

## Truth discipline

Never invent company facts, services, credentials, clients, statistics, testimonials, locations, results, personnel or claims. Distinguish verified/client-stated/inferred/unknown information. Missing essential information is a blocker.

## Design Library

`telano-gif/Design_Library` is separate read-only design intelligence. When the Design stage is active, consult its `DESIGN.md` first, then inspect only relevant files. Search by niche, page requirement, component, visual system, motion or interaction as needed. Synthesize principles; never copy branding, content, assets or distinctive implementations.

Do not read the whole library.

## Imagery

Design defines image requirements; Imagery sources/selects assets. Use approved client assets first where appropriate. When an Unsplash integration is available, search from explicit image roles rather than generic aesthetic queries. Track source/licensing information. Never imply stock imagery represents the client.

## Build

Build from canonical artifacts. Implement the approved design rather than substituting a generic template. Use minimal dependencies and appropriate abstractions. Validate with `IMPLEMENT → RUN → INSPECT → FIX → RE-RUN`. A successful compile is not completion.

## QA

QA is adversarial. It must inspect rendered output and test technical, visual, content, responsive, accessibility and conversion quality. A changed build requires QA again. Never reuse an old QA pass after implementation changes.

## Deployment

Never deploy without `QA_COMPLETE`. The website is an independent GitHub repository deployed through Vercel. Never store secrets in source control. Verify the live production URL and critical user flow after deployment.

## Token/context discipline

Use the smallest sufficient context. Prefer canonical artifacts over raw source material. Inspect selectively. Do not generate summaries, documentation or abstractions unless required for execution. Avoid rereading unchanged files. Keep outputs concise but complete.

## Architecture discipline

Prefer the fewest files, dependencies and moving parts that reliably satisfy the requirement. Do not add databases, dashboards, APIs, automation or frameworks without a concrete production need. Do not implement future components prematurely.

## Client isolation

Client data, assets, source code and deployment configuration belong to the client project. Never leak client-specific information into global factory skills or another project.

## Human oversight

Stop and ask for human direction when facts are materially missing, a major design decision is unresolved, a HIGH QA issue is to be accepted rather than fixed, or a repository/deployment target is ambiguous.
