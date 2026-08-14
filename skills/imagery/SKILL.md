# Imagery Skill

## Mission
Source and prepare imagery that strengthens the approved website design. Imagery is selected for a specific communication role, not because it merely looks attractive.

## Inputs
- `INTAKE.md`
- `RESEARCH.md`
- `DESIGN_SPEC.md`
- client-supplied assets
- approved imagery sources/integrations

## Workflow

1. Read the design specification and extract every image requirement.
2. Define each image's role, subject, mood, composition, orientation, crop and placement.
3. Prefer client-owned/supplied assets when appropriate.
4. Search approved stock/image sources, including the future Unsplash integration, using precise queries derived from the requirement.
5. Select candidates based on subject relevance, composition, visual consistency, crop flexibility and licensing suitability.
6. Record the chosen asset and intended component.
7. Prepare/optimise assets for web delivery without degrading required quality.
8. Verify that every required visual slot has an approved asset or an explicit blocker.

## Image requirement format

For each required image define:

- `ROLE` — what communication job it performs
- `SUBJECT` — what must be depicted
- `COMPOSITION` — useful negative space/focal placement
- `ORIENTATION` — landscape/portrait/square/etc.
- `MOOD` — visual character
- `CROP` — expected responsive treatment
- `PRIORITY` — required/optional

## Unsplash

When the Unsplash integration is available, use it as a controlled source rather than a free-form image generator. Search from explicit image requirements, evaluate candidates, and record the selected source/asset information required by the project.

Do not search for "nice images" without a defined role. Do not let stock imagery determine the design after the design has been approved.

## Rules

- Never use an image simply because it is visually impressive if it conflicts with the company's industry, message or design system.
- Never imply a stock image depicts the client's actual people, facilities, projects, customers or results unless that is true.
- Do not invent image subjects that could create false factual claims.
- Respect source licensing/usage requirements and retain required attribution/source information.
- Do not use copyrighted reference-site imagery merely because it appears in Design_Library analyses.
- Avoid repetitive stock-photo clichés.
- Prefer a small, coherent image set over many unrelated images.
- Optimise dimensions/file size for actual placement and responsive use.
- Do not unnecessarily introduce an image dependency when CSS, SVG or an existing client asset better serves the design.

## Produce
`02_design/IMAGERY.md` containing:
- image requirements by page/component
- selected assets and sources
- intended placement/crop
- asset status
- licensing/source notes
- optimisation notes
- unresolved image blockers

## Completion gate

Set `IMAGERY_COMPLETE` only when all required image roles have approved assets or explicit blockers and source/licensing information is recorded.

## Handoff
`IMAGERY_COMPLETE` → Build consumes `IMAGERY.md` with `DESIGN_SPEC.md` and approved assets.
