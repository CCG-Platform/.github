# [Medium] Multiple services run mutable portal-app:latest image

- **Repository:** `portal-backend`
- **Severity:** **Medium**

## Evidence
- `portal-backend/docker-compose.yml:34,53,59,65 use portal-app:latest.`

## Impact
Operational debugging/rollback is harder when worker/beat/flower can drift across pulls.

## Recommendation
Use immutable tags (git SHA/version) shared across all app services in compose.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
