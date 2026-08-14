# Workflow Engine Contract

## Purpose
Enforce the Website Factory lifecycle. Skills are specialist instructions; this file defines when they may run, what they must leave behind, and when a project may advance.

## Lifecycle

`INTAKE → RESEARCH → DESIGN → IMAGERY → CONTENT → BUILD → QA → DEPLOY → COMPLETE`

QA may return a project to BUILD. Other stages may return to their immediate predecessor when their output exposes a missing or contradictory input. Do not skip stages.

## Project state

Each project has a `STATUS.md` containing:

```text
PROJECT: <name>
STAGE: <current stage>
STATE: <IN_PROGRESS|BLOCKED|COMPLETE>
LAST_COMPLETED: <stage or NONE>
NEXT_STAGE: <stage or NONE>
BLOCKERS: <none or concise list>
UPDATED: <date>
```

## Canonical artifacts

| Stage | Required output | Gate |
|---|---|---|
| Intake | `INTAKE.md` | `INTAKE_COMPLETE` |
| Research | `RESEARCH.md` | `RESEARCH_COMPLETE` |
| Design | `DESIGN_SPEC.md` | `DESIGN_COMPLETE` |
| Imagery | `IMAGERY.md` | `IMAGERY_COMPLETE` |
| Content | `CONTENT.md` | `CONTENT_COMPLETE` |
| Build | finished website + build validation | `BUILD_COMPLETE` |
| QA | `QA.md` | `QA_COMPLETE` |
| Deploy | `DEPLOY.md` | `DEPLOYED` |
| Final | deployment verified | `COMPLETE` |

## Gate rules

A stage cannot be marked complete unless its canonical output exists and its skill's completion criteria are satisfied.

The next stage consumes the previous canonical output. Do not repeatedly reread the entire project when the canonical artifact contains what is needed.

If a required fact/input is missing, mark the project `BLOCKED`. Do not fabricate it.

If QA finds a defect that requires implementation, return to BUILD. After a BUILD change, QA must run again; never preserve an old QA pass as proof for a changed build.

If a later stage discovers a material problem with an earlier output, return to the smallest stage that can correctly resolve it and invalidate downstream completion states as necessary.

## Invalidation

When a canonical artifact changes, downstream stages depending on it are no longer trusted until rerun.

Examples:
- Research change → Design, Imagery, Content, Build, QA and Deploy require revalidation.
- Design change → Imagery, Content, Build, QA and Deploy require revalidation.
- Content change → Build, QA and Deploy require revalidation.
- Build change → QA and Deploy require revalidation.
- QA change → Deploy requires revalidation.

Do not delete previous outputs merely because they are invalidated; mark their state stale when useful for auditability.

## Human oversight

Human approval is required when:
- a material factual gap cannot be verified
- a major design direction must change
- a HIGH QA issue is proposed for acceptance rather than fixed
- deployment target/repository is ambiguous
- credentials, domain ownership or other external access is required

The factory may execute routine work without approval when gates are satisfied.

## Completion definition

A project is `COMPLETE` only when:
- all required stage gates passed
- production deployment succeeded
- live smoke tests passed
- no unresolved blocker remains
- the production URL is recorded

A source-code build without a verified production deployment is not complete.
