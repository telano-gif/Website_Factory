# Factory Contract

## Mission

Turn a company from raw input into a tailored, production-ready website through a controlled sequence of specialist stages.

## Lifecycle

1. INTAKE — establish the company brief, requirements, assets and constraints.
2. RESEARCH — establish verified facts, audience, objectives and relevant context.
3. DESIGN — derive a concrete visual/interaction direction using research and the Design Library.
4. CONTENT — produce page/content structure grounded in verified information.
5. BUILD — implement the website in its own deployable repository.
6. QA — verify technical correctness, content fidelity, responsive behaviour and visual quality.
7. DEPLOY — publish the approved website through GitHub → Vercel.

## Handoff rule

Every stage has a canonical output. The next stage should use that output as its primary handoff rather than reconstructing the previous stage's work.

## Project isolation

Each client project is independent. Factory rules and skills are shared; client inputs, outputs and website source are not.

## Quality rule

A successful code build is not sufficient for completion. The website must also satisfy the project's content, design and QA requirements.

## Deployment boundary

The factory owns the production workflow. Each finished website owns its application code and Git history. Deployment targets GitHub and Vercel; credentials and provider-specific secrets must never be stored in the factory or client source.