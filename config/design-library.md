# Design Library Dependency

Repository: `telano-gif/Design_Library`
Role: read-only design intelligence for the Website Factory.

## Purpose

The library supplies reusable design knowledge: niche patterns, page layouts, components, visual systems, motion, interaction patterns, reference-site analyses and design recipes.

## Consumption model

Do not copy the library into the factory. The Design stage should selectively inspect the library when it has enough client context to search intelligently.

Search order should generally be:

1. Client niche / industry patterns
2. Required page/layout patterns
3. Relevant component patterns
4. Visual system / typography / spacing / colour patterns
5. Motion and interaction patterns
6. Reference-site analyses when useful
7. Design recipes for synthesis

Select only references that solve an actual design requirement. Combine compatible patterns rather than reproducing one reference site wholesale.

## Output

The future Design skill converts selected library knowledge into a project-specific `DESIGN_SPEC.md`. Downstream Build should depend on that specification, not on the entire library.

## Integrity

Use references as design intelligence, not as content or asset sources. Do not copy logos, proprietary branding, text, imagery or distinctive site implementations. The resulting design must be tailored to the client.

## Token efficiency

Inspect the library selectively. Do not read the entire repository for every project. Use filenames, directory structure and `DESIGN.md` to locate the smallest relevant set of files.