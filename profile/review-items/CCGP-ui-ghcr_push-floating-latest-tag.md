# [Medium] CI pipeline pushes mutable latest image tag

- **Repository:** `CCGP-ui`
- **Severity:** **Medium**

## Evidence
- `CCGP-ui/.github/workflows/ghcr_push.yml:42-45 builds and pushes :latest in addition to SHA tag.`

## Impact
latest tag mutability reduces deployment reproducibility and rollback confidence.

## Recommendation
Promote immutable SHA/version tags and gate latest retagging behind explicit release workflow.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
