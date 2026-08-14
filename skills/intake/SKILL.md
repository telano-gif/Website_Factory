# Intake Skill

## Purpose
Turn a new client into a complete, bounded website brief without inventing facts.

## Input
- Client/company material supplied in `00_input/`
- Stated website requirements
- Existing brand/assets/references

## Produce
`INTAKE.md` containing only actionable facts and requirements:
- company identity and verified description
- audience
- business objective
- required pages
- services/products
- brand requirements
- supplied assets
- design references
- technical/deployment constraints
- known missing information
- explicit exclusions

## Rules
- Treat supplied material as the source of truth.
- Separate verified facts from client preferences and unknowns.
- Never fill missing company information with plausible copy.
- Do not research deeply; that belongs to Research.
- Do not make design decisions beyond recording requirements/references.

## Complete when
The next stage can understand what must be built, for whom, why, and what constraints apply without reopening the entire intake material.

## Handoff
`INTAKE_COMPLETE` → Research consumes `INTAKE.md`.
