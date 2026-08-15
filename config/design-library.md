# Design Library Dependency

Repository: `telano-gif/Design_Library`
Role: read-only design intelligence for the Website Factory.

## Purpose

The library supplies reusable design knowledge: principles, niche patterns, page layouts, components, visual systems, motion, interaction patterns, reference-site patterns, real-site design-language analyses and design recipes.

## Access protocol

The Design stage must access the library deterministically:

1. Read `DESIGN.md` at the library root first.
2. Inspect the repository tree to identify relevant directories/files.
3. Select files by path/filename before opening contents.
4. Fetch only the smallest relevant set of files for the project.
5. Do not rely on GitHub code search; it may not index every library file.
6. Do not read or ingest the entire repository.

## Actual structure

```text
DESIGN.md
00_DESIGN_PRINCIPLES.md
01_LAYOUTS/
02_COMPONENTS/
03_VISUAL_SYSTEMS/
04_MOTION/
05_INTERACTION/
06_NICHE_PATTERNS/
07_REFERENCE_SITES/
08_SOURCE_WORKFLOW.md
09_DESIGN_RECIPES/
10_REAL_DESIGN_SYSTEMS/
```

## What each layer provides

- `DESIGN.md` — operating rules for using the library.
- `00_DESIGN_PRINCIPLES.md` — universal design quality principles.
- `01_LAYOUTS/` — page and composition patterns.
- `02_COMPONENTS/` — reusable UI/component patterns.
- `03_VISUAL_SYSTEMS/` — typography, grid, spacing, colour and imagery systems.
- `04_MOTION/` — motion patterns and principles.
- `05_INTERACTION/` — interaction models and states.
- `06_NICHE_PATTERNS/` — patterns tailored to industries/niches.
- `07_REFERENCE_SITES/` — concrete page, layout and component patterns extracted from real websites.
- `08_SOURCE_WORKFLOW.md` — rules for obtaining and extracting external design references.
- `09_DESIGN_RECIPES/` — compact recipes for combining patterns toward a design objective.
- `10_REAL_DESIGN_SYSTEMS/` — compact analyses of the broader design language of real websites.

`07_REFERENCE_SITES` and `10_REAL_DESIGN_SYSTEMS` are deliberately different:

- Use `07_REFERENCE_SITES` when solving a concrete page, layout or component problem.
- Use `10_REAL_DESIGN_SYSTEMS` when studying broader visual language, hierarchy, typography, spacing, interaction or motion characteristics of a real site.

## Consumption model

Do not copy the library into the factory. The Design stage selectively inspects it after enough client context exists to search intelligently.

A typical selection sequence is:

1. `06_NICHE_PATTERNS/`
2. `01_LAYOUTS/`
3. `02_COMPONENTS/`
4. `03_VISUAL_SYSTEMS/`
5. `04_MOTION/` and `05_INTERACTION/` as required
6. `07_REFERENCE_SITES/` for concrete real-site page/layout/component references
7. `10_REAL_DESIGN_SYSTEMS/` for broader real-site design-language references
8. `09_DESIGN_RECIPES/` when synthesis would benefit from a predefined direction

Do not force every layer into every project. Select only references that solve actual design requirements. Combine compatible patterns rather than reproducing one reference site wholesale.

## Output contract

The Design stage converts selected library knowledge into the project-specific canonical artifact:

`DESIGN_SPEC.md`

`DESIGN_SPEC.md` lives at the **project repository root**.

Downstream Build must depend on `DESIGN_SPEC.md`, not on the entire Design Library. The Design Library is not a Build-stage dependency.

## Integrity

Use references as design intelligence, not as content or asset sources. Do not copy logos, proprietary branding, text, imagery or distinctive site implementations. The resulting design must be tailored to the client.

## Token efficiency

Inspect the library selectively. Read `DESIGN.md` first, then use the tree and filenames to locate the smallest relevant set of files. Avoid broad ingestion, duplicate references and unnecessary external research.