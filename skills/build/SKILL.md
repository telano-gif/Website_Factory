# Build Skill

## Mission
Turn the approved project artifacts into a polished, production-ready website that faithfully implements the design rather than collapsing into a generic template.

## Inputs
- `INTAKE.md`
- `RESEARCH.md`
- `DESIGN_SPEC.md`
- `IMAGERY.md`
- `CONTENT.md`
- approved client assets

## Before coding

1. Read the canonical artifacts in the order above.
2. Inspect the existing build/project scaffold before changing architecture.
3. Identify the framework, package manager, scripts, assets and constraints already present.
4. Resolve any contradiction in canonical artifacts before implementation; do not silently choose.
5. Create an implementation checklist from the design/content specifications.

## Implementation sequence

1. Establish the page/routes and global design tokens.
2. Build the core layout/navigation/footer.
3. Build the primary page composition and highest-value components first.
4. Add approved imagery/assets with intentional crops and responsive behaviour.
5. Implement typography, spacing, colour, surfaces and hierarchy from `DESIGN_SPEC.md`.
6. Implement interaction and motion specified by Design; every animation must have a purpose and respect reduced-motion preferences.
7. Implement forms and conversion flows from Content/Intake.
8. Compose remaining pages/sections.
9. Test responsive states and intermediate widths.
10. Run technical checks and perform a visual pass before handoff.

## Design fidelity

Treat `DESIGN_SPEC.md` as the source of truth for visual implementation.

Do not replace a specified concept with convenient defaults such as:
- generic card grids
- default component-library styling
- arbitrary gradients
- excessive rounded containers
- stock UI patterns unrelated to the design
- generic hero sections
- unnecessary animation

If a design decision is genuinely impossible or technically unsafe, record the conflict and choose the smallest defensible alternative rather than silently redesigning the site.

## Component discipline

Create reusable components where repetition or a meaningful interaction warrants them. Do not abstract one-off sections merely to increase component count.

Prefer:
- semantic HTML
- CSS/design tokens over scattered magic values
- accessible native controls where suitable
- minimal dependencies
- predictable state
- clear data/content separation

Avoid premature design-system frameworks, unnecessary animation libraries and architecture that exists only for hypothetical future sites.

## Content fidelity

`CONTENT.md` is the wording source of truth. Do not invent missing copy to make a page look finished.

If content is blocked, preserve an explicit project placeholder or stop for the required input according to the project state rules.

Never fabricate:
- company facts
- statistics
- testimonials
- clients
- certifications
- people
- project results
- locations
- credentials

## Imagery

`IMAGERY.md` is the asset-selection source of truth. Use approved assets and preserve their intended role/crop. Do not substitute random stock imagery because a section looks empty.

## Responsive behaviour

Design mobile, tablet/intermediate and desktop states intentionally. Do not treat responsive work as simply shrinking the desktop layout.

Check:
- navigation behaviour
- typography scale
- section order
- grid/card transformations
- image crops
- touch targets
- overflow
- motion
- forms

## Quality requirements

Before declaring `BUILD_COMPLETE`, verify:

- all required routes exist
- navigation and CTAs work
- no obvious dead ends or broken links
- supplied assets load correctly
- no accidental placeholder text remains
- layout works at common desktop/mobile widths and at intermediate widths
- keyboard focus is usable
- interactive controls have accessible names
- colour contrast is reasonable
- reduced motion is respected
- images are appropriately sized/formatted
- no avoidable console/runtime errors remain
- lint/type/build checks pass where available

## Validation loop

Do not stop at compilation.

Use this loop:

`IMPLEMENT → RUN → INSPECT → FIX → RE-RUN`

Where browser/visual tooling is available, inspect the rendered site rather than relying only on source code. Compare the result against `DESIGN_SPEC.md` and `CONTENT.md`.

## Output

The finished website lives in its own deployable repository under the project build area. Record the implementation status and any non-blocking deviations needed by QA.

## Completion gate

Set `BUILD_COMPLETE` only when:
- the site is implemented across required pages/routes
- design and content specifications are substantially satisfied
- imagery is correctly integrated
- responsive/accessibility fundamentals are addressed
- available technical checks pass
- a rendered visual inspection has been performed when tooling permits
- no known critical implementation defect remains

A successful `npm run build` alone is never sufficient.

## Handoff
`BUILD_COMPLETE` → QA consumes the rendered website, source repository and all canonical artifacts.