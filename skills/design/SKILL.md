# Design Skill

## Mission
Turn verified company context into a distinctive, coherent, implementable website design—not a generic AI template.

## Inputs
- `00_input/`
- `INTAKE.md`
- `RESEARCH.md`
- client brand/assets/references

## Design Library

Use `telano-gif/Design_Library` as read-only design intelligence. Its `DESIGN.md` is the operating manual and must be consulted before library research.

Search selectively, in this order as needed:
1. niche patterns
2. page layouts
3. components
4. visual systems
5. motion
6. interaction
7. source/reference analyses
8. design recipes

Inspect filenames/search results first; open only relevant files. Do not read the entire library. Prefer 3–6 strong compatible patterns over a large collection of effects.

Pattern selection must respond to:
- business objective
- audience
- niche conventions
- available content
- brand character
- technical constraints
- accessibility
- performance

References are evidence, not templates. Extract principles such as composition, hierarchy, spacing, typography relationships, interaction model, motion principle, image treatment and information architecture. Do not copy logos, copy, proprietary assets, distinctive artwork, exact page composition or unique interactions.

## Design process

1. Establish audience, business goal, niche, page set, content density, brand character and primary conversion action from Intake/Research.
2. Identify the visual problem the site must solve.
3. Search the Design Library for the smallest relevant set of patterns.
4. Select compatible patterns and resolve conflicts before implementation.
5. Define an original visual system and page architecture.
6. Define imagery roles and art direction; image sourcing is handled by the imagery stage when available.
7. Define purposeful interaction and motion.
8. Define deliberate responsive recomposition, not desktop stacking.
9. Produce the compact implementation specification.

## Produce
`02_design/DESIGN_SPEC.md` containing:
- design concept
- audience/business/UX rationale
- visual hierarchy
- page architecture and section sequence
- typography strategy
- colour strategy
- spacing/grid system
- component/pattern selections
- imagery/art direction and image roles
- interaction/motion strategy
- responsive strategy
- accessibility/performance constraints
- selected Design Library references + the decision each contributes
- implementation priorities

Keep it compact. Build should be able to implement it without guessing.

## Quality rules

- The first viewport clearly communicates what the company/site does.
- Typography and spacing are intentional.
- Section rhythm varies without losing coherence.
- Imagery supports content and art direction.
- Interactions have clear affordances.
- Motion has a job: reveal hierarchy, show continuity, explain relationships, communicate state or add restrained atmosphere.
- Respect reduced motion.
- Mobile and intermediate widths are deliberately composed.
- Contrast and keyboard/touch usability are acceptable.
- Visual quality must not require unnecessary dependencies or sacrifice performance.

Reject generic failure modes such as:
- SaaS-card grids everywhere
- giant headline + gradient + blobs with no concept
- excessive rounded cards
- random glassmorphism
- generic stock-photo heroes
- repeated identical section structures
- animation used to disguise weak content
- impressive visuals that obscure the company's message

## Boundaries

Research establishes facts and context; Design establishes visual/UX direction; Content establishes wording; Build implements the approved system. Do not fabricate company facts or substitute unsupported content to make a design work.

## Completion gate

Set `DESIGN_COMPLETE` only when the page architecture, visual system, component patterns, imagery direction, interaction/motion and responsive strategy are sufficiently resolved for Build to proceed without major design guesses.

## Handoff
`DESIGN_COMPLETE` → Content and Build consume `INTAKE.md`, `RESEARCH.md`, `DESIGN_SPEC.md` and only the source material/assets they actually need.
