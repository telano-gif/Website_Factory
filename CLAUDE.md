# Website Factory — Operating Rules

This repository is the reusable production system for building company websites.

## Pipeline

INTAKE → RESEARCH → DESIGN → CONTENT → BUILD → QA → DEPLOY

Stages are mandatory. A stage consumes the previous stage's canonical output and must satisfy its completion criteria before advancing.

## Core rules

- Inspect the repository and relevant project files before creating or changing anything.
- Keep the factory generic; never put client-specific facts into global skills.
- Never invent company facts, credentials, services, statistics, testimonials, locations or claims.
- Keep canonical stage outputs compact; do not force later stages to reread unnecessary raw material.
- Keep projects isolated from one another.
- Prefer the smallest reliable architecture and fewest moving parts.
- Do not add infrastructure, automation or dependencies without a concrete production need.
- The final website is an independent Git repository and ultimately deploys through GitHub → Vercel.

## Design Library

`telano-gif/Design_Library` is an external, read-only design-intelligence dependency. It is not copied into this repository.

The future Design stage must search it selectively based on the client's niche, audience, positioning, page requirements and desired visual direction. Use its niche patterns, layouts, components, visual systems, motion, interaction patterns and reference analyses as inputs. Synthesize; do not copy branding, content or assets from references.

Do not implement Design Library integration until its dedicated skill/component is being built.

## Stage completion

Each stage must leave a clear canonical output and update project state. If required information is missing or a stage is blocked, stop and record the blocker rather than fabricating an answer or silently skipping the stage.

## Current build rule

Build the factory incrementally, one component at a time. Do not implement future components prematurely. After each component, verify the result before proceeding.