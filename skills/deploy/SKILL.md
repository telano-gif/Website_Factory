# Deploy Skill

## Mission
Safely move an approved, QA-complete website from its independent source repository to production through GitHub → Vercel and verify the live result.

## Inputs
- Finished website repository
- `QA.md` with `QA_COMPLETE`
- Project deployment configuration

## Preconditions
Do not deploy unless:
- `QA_COMPLETE` is present
- no unresolved BLOCKER exists
- the intended client GitHub repository is identified
- the intended Vercel project/target is identified
- required environment variables/secrets are available through the provider, not source control

If any precondition fails, stop and record the blocker.

## Workflow

1. Verify the website repository and branch intended for production.
2. Verify the GitHub → Vercel connection/target.
3. Confirm required production environment variables are configured without exposing their values.
4. Trigger or allow the production deployment according to the project's configured workflow.
5. Wait for deployment completion.
6. Verify the production URL responds successfully.
7. Smoke-test critical routes, navigation and primary conversion flow on the live deployment.
8. Record deployment metadata and final status.

## Rules

- Never bypass QA to ship a website.
- Never commit secrets, tokens, API keys or provider credentials.
- Never assume a successful deployment means the live site is correct.
- Never overwrite another client's Vercel project or GitHub repository.
- Preserve the client's repository as the source of truth for the website.
- Use provider-native deployment mechanisms; do not introduce a custom deployment server unless explicitly required.

## Rollback / failure

If deployment fails, diagnose the smallest actionable failure and return the project to the appropriate stage. Do not repeatedly retry blindly.

If deployment succeeds but live smoke tests fail, mark deployment failed and return to Build/QA as appropriate.

## Produce
`06_deploy/DEPLOY.md` containing:
- repository/branch deployed
- Vercel target
- deployment result
- production URL
- verification checks
- environment configuration status (never secret values)
- failures/rollback status
- final deployment state

## Completion gate

Set `DEPLOYED` only when:
- the intended repository deployed successfully
- the production URL is reachable
- critical routes work
- the primary conversion path works
- no deployment blocker remains

Set `COMPLETE` only after the deployment record is written and final verification passes.

## Handoff
`DEPLOYED` → final project verification → `COMPLETE`.