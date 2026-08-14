# Deploy Skill

## Purpose
Move an approved, QA-complete website from its independent source repository to production through GitHub → Vercel.

## Input
`QA.md` showing `QA_COMPLETE` + finished website repository.

## Produce
A deployed website with deployment state recorded in the project.

## Rules
- Never deploy a project that has not passed QA.
- Keep the client website repository independent from Website_Factory.
- Never store provider credentials or secrets in source control.
- Verify the intended GitHub repository and Vercel project before deployment.
- Confirm the production deployment and basic reachability after deployment.
- Record the production URL and deployment status.

## Complete when
The intended GitHub repository is connected to the intended Vercel project, production deployment succeeds, and the live site is verified.

## Handoff
`DEPLOYED` → project may be marked `COMPLETE` after final verification.
