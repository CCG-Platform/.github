# [Medium] Repository table is incomplete relative to active repos

- **Repository:** `.github`
- **Severity:** **Medium**

## Evidence
- `.github/profile/README.md:123-132 lists only six repositories.`

## Impact
Public org profile can mislead contributors about where active components live (demo, POC, game-container, k8s-setup-script, CCG-Platform repo).

## Recommendation
Either list all active repositories or explicitly split the table into "Core" and "Ancillary/Experimental" sections.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
