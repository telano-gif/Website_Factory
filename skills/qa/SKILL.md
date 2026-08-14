# QA Skill

## Mission
Act as an adversarial release gate. Find defects, weak implementation and deviations from the approved project—not merely syntax errors.

## Inputs
- Finished website source/render
- `INTAKE.md`
- `RESEARCH.md`
- `DESIGN_SPEC.md`
- `IMAGERY.md`
- `CONTENT.md`
- Build validation output

## QA sequence

### 1. Technical
- install/build/lint/type checks where available
- runtime/console errors
- routes and navigation
- internal/external links
- missing assets
- forms and submission/error states
- metadata and basic SEO

### 2. Visual
Inspect rendered pages, not only source code.

Check:
- first viewport communicates the company and primary action
- hierarchy and typography
- spacing/grid consistency
- section rhythm
- alignment
- imagery quality, crop and relevance
- responsive composition
- intermediate widths
- mobile navigation and touch targets
- visual polish and obvious unfinished areas

Compare against `DESIGN_SPEC.md`. Reject generic substitutions that materially weaken the approved direction.

### 3. Content
Compare rendered content against `CONTENT.md` and factual constraints in `RESEARCH.md`.

Find:
- invented claims
- altered facts
- missing sections/copy
- accidental placeholder text
- broken CTAs
- inconsistent terminology
- unsupported social proof

### 4. Interaction/accessibility
Check:
- keyboard navigation/focus
- semantic structure
- accessible names/labels
- contrast
- touch targets
- hover/focus/active states
- reduced motion
- modal/menu/form state behaviour
- obvious interaction dead ends

### 5. Performance
Look for obvious avoidable problems:
- oversized images
- unnecessary client-side code
- excessive dependencies
- needless animation/work on scroll
- layout shifts
- repeated expensive rendering

Do not optimise prematurely; fix material issues.

## Adversarial questions

Before passing, explicitly ask:

- Does this actually look like the approved design, or did Build fall back to a template?
- Does the site communicate the company within seconds?
- Is anything obviously AI-generated, repetitive or filler-heavy?
- Is there a section that exists only because a template expected it?
- Does mobile look intentionally designed?
- Are motion and visual effects helping or distracting?
- Could a visitor misunderstand any factual claim?
- Is any important CTA, route or form broken?
- What would a demanding client notice first?

## Severity

`BLOCKER` — prevents launch or creates serious factual, functional, accessibility or security risk.
`HIGH` — materially damages quality, UX, design fidelity or conversion.
`MEDIUM` — noticeable defect that should be fixed before final approval when practical.
`LOW` — polish/improvement that does not block release.

## Remediation

Fix safe, objective defects directly. For design/content decisions requiring judgement, record the issue and return the project to the appropriate stage rather than silently changing approved direction.

If Build can correct a defect, QA should trigger a Build → QA loop. QA does not become a second uncontrolled design phase.

## Produce
`05_qa/QA.md` containing:
- environment/checks performed
- pages/routes inspected
- defects by severity
- fixes performed
- unresolved issues/blockers
- design/content fidelity result
- final release recommendation

## Completion gate

Set `QA_COMPLETE` only when:
- no BLOCKER remains
- HIGH issues are resolved or explicitly accepted by the human overseer
- technical checks pass where applicable
- rendered visual inspection is complete
- content/design fidelity is acceptable
- required user flows work
- no obvious unfinished or fabricated content remains

A green build alone can never produce `QA_COMPLETE`.

## Handoff
`QA_COMPLETE` → Deploy consumes the finished website repository and `QA.md`.