# QA Skill

## Purpose
Aggressively verify that the finished website is correct, polished and faithful to the approved project artifacts.

## Input
Built website + `INTAKE.md` + `RESEARCH.md` + `DESIGN_SPEC.md` + `CONTENT.md`.

## Check
- build/lint/type errors
- routes and navigation
- responsive layouts
- broken links/assets
- content accuracy and missing placeholders
- design-spec implementation
- typography, spacing and visual hierarchy
- interactions and motion
- accessibility fundamentals
- obvious performance issues
- metadata/basic SEO
- forms and user flows

## Rules
- Treat visual quality as a first-class QA concern, not just code correctness.
- Compare implementation against the canonical design/content artifacts.
- Fix issues that can be safely fixed; record issues requiring human judgement.
- Do not silently change approved content or design direction to hide a defect.

## Produce
`QA.md` with checks performed, defects found, fixes made, remaining blockers and final status.

## Complete when
All critical issues are resolved, no known blocking defect remains, and the website is suitable for deployment or has explicit human-review blockers.

## Handoff
`QA_COMPLETE` → Deploy.
