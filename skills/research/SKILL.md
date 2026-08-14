# Research Skill

## Mission
Turn an approved intake into the smallest reliable evidence base needed to build a convincing, accurate website.

## Inputs
- `00_input/` source material and assets
- `INTAKE.md`
- Client-provided URLs/references

## Research sequence

1. Read `INTAKE.md` and identify factual gaps that materially affect the website.
2. Inspect supplied company material first.
3. Research the company's own/primary sources before secondary sources.
4. Research only website-relevant industry/audience/context gaps.
5. Record evidence for consequential claims.
6. Resolve contradictions or flag them explicitly.
7. Stop when additional research is unlikely to improve the website.

## Evidence hierarchy

Prefer, in order:
1. Client-provided source documents
2. Official company sources
3. Government/regulatory/standards bodies and other authoritative primary sources
4. Reputable specialist/industry sources
5. General secondary sources only when useful

Never treat search snippets, aggregators or unsourced claims as sufficient evidence for important facts.

## Produce
`01_research/RESEARCH.md` containing:

- Company: verified identity, description, location and relevant history
- Audience: who the site needs to persuade and their likely needs/problems
- Offering: verified products/services/capabilities
- Positioning: evidence-supported differentiators; distinguish stated claims from researcher inference
- Industry/context: only information that changes messaging, structure or trust
- Proof: clients, projects, certifications, credentials, statistics or other evidence only when verified
- Requirements: implications for pages, information hierarchy and conversion
- Gaps: missing information that materially limits accuracy/quality
- Conflicts: contradictory facts with sources and resolution/status
- Sources: concise source register for consequential facts

Use compact evidence labels where useful:
`VERIFIED` / `CLIENT-STATED` / `INFERRED` / `UNKNOWN` / `CONFLICT`

## Geographic and temporal discipline

Check that evidence refers to the correct company/entity, geography and time period. Never silently substitute a nearby geography, similarly named organisation, outdated figure or broader market statistic.

## Content discipline

Do not invent:
- services or capabilities
- clients or partnerships
- testimonials
- awards/certifications
- statistics
- locations
- years of experience
- guarantees/results
- personnel or credentials

If a plausible claim cannot be evidenced, mark it `UNKNOWN`.

## Design boundary

Research may identify audience, positioning, content hierarchy, visual communication needs and useful references. It must not prescribe the visual design system. The Design stage decides that using `RESEARCH.md` and the Design Library.

## Token discipline

Do not dump browsing notes into `RESEARCH.md`. Keep only findings that affect the website and enough source context to verify consequential claims. Avoid researching facts that will not appear in or influence the site.

## Completion gate

Set `RESEARCH_COMPLETE` only when:
- core company facts are verified or explicitly marked unknown
- audience/objective context is sufficient
- major website-relevant claims have evidence
- contradictions are resolved or documented
- material gaps are explicit
- the output is compact enough for downstream stages

If a missing fact is essential and cannot be verified, stop with a blocker rather than fabricate it.

## Handoff
`RESEARCH_COMPLETE` → Design consumes `INTAKE.md` + `RESEARCH.md` and selected source material only when necessary.
