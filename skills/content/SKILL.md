# Content Skill

## Mission
Turn verified research into clear, persuasive, implementation-ready website content that fits the approved design and does not fabricate company facts.

## Inputs
- `INTAKE.md`
- `RESEARCH.md`
- `DESIGN_SPEC.md`
- approved client material/assets where needed

## Workflow

1. Map the required pages and conversion path from Intake + Design.
2. Define the job of each page and each major section.
3. Extract supported facts/claims from Research.
4. Write concise page content around audience needs and business objectives.
5. Map proof/claims to their evidence status.
6. Specify CTAs and form requirements.
7. Check content length against the approved layout/component system.
8. Identify missing client information rather than filling it with plausible copy.

## Produce
`03_content/CONTENT.md` containing:

- site-wide messaging hierarchy
- navigation and footer labels
- page-by-page section order
- section purpose
- headings/subheadings
- body copy
- CTAs
- forms/fields and success/error requirements
- proof elements and evidence status
- factual source/evidence references where consequential
- unresolved placeholders/blockers

## Writing rules

- Lead with what the company does and why the visitor should care.
- Write for the identified audience, not for an abstract "website visitor".
- Prefer specific, defensible language over generic marketing adjectives.
- Every substantive factual claim must be supported by Intake/Research or explicitly marked unresolved.
- Never invent services, clients, statistics, awards, certifications, testimonials, results, locations, credentials or years of experience.
- Do not turn researcher inference into company fact.
- Do not create fake social proof.
- Do not repeat the same value proposition in every section.
- Avoid filler such as empty superlatives and generic AI phrasing.
- Keep copy proportional to the approved visual hierarchy. Do not make the Build stage redesign pages to accommodate unnecessary text.
- Preserve required legal/compliance wording supplied by the client.

## Content architecture

For each page, define:

`JOB` — what the page must accomplish
`AUDIENCE` — who it addresses
`SECTIONS` — ordered content blocks
`CTA` — desired next action
`PROOF` — evidence used, if any
`BLOCKERS` — missing information that prevents accurate completion

## Content/design boundary

Design decides hierarchy, layout, component behaviour and visual language. Content decides the message and wording within that system. Do not redesign the site through copywriting.

If the design requires information the research does not support, flag the gap. Do not invent content to preserve the design.

## Completion gate

Set `CONTENT_COMPLETE` only when:
- every required page has its required content structure
- core copy is written
- CTAs/forms are defined
- consequential claims are supportable
- unresolved facts are explicit
- content fits the approved design direction

If a missing fact is essential to a truthful page, stop with a blocker.

## Handoff
`CONTENT_COMPLETE` → Build consumes `CONTENT.md` + `DESIGN_SPEC.md` + `IMAGERY.md` + only the source material/assets it needs.
