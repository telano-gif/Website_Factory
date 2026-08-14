# Design Skill

## Purpose
Create a distinctive, implementable design direction from the client context and the separate Design_Library.

## Input
`INTAKE.md` + `RESEARCH.md` + client assets/references.

## Design Library
Use `telano-gif/Design_Library` as read-only design intelligence. Search selectively by niche, audience, page requirement and visual objective. Consult its `DESIGN.md` operating guidance first, then inspect only relevant patterns/layouts/components/visual systems/motion/interaction/reference analyses.

Do not copy a reference site. Synthesize compatible patterns into a client-specific system.

## Produce
`DESIGN_SPEC.md` defining:
- design concept and rationale
- visual hierarchy
- typography
- colour system
- spacing/grid
- page structures
- component patterns
- imagery direction and requirements
- interaction/motion direction
- responsive behaviour
- accessibility-critical decisions
- selected Design_Library references and what each contributes
- explicit implementation priorities

## Rules
- Design for the client's niche, audience and objective; do not default to generic AI aesthetics.
- Every major visual decision must solve a communication or UX purpose.
- Separate inspiration from implementation decisions.
- Do not use reference-site content, logos, proprietary branding or copied assets.
- Keep the specification compact enough for Build to consume directly.

## Complete when
Build can implement the intended visual system and page/component structure without guessing the design direction.

## Handoff
`DESIGN_COMPLETE` → Content and Build consume `DESIGN_SPEC.md` alongside prior canonical outputs.
