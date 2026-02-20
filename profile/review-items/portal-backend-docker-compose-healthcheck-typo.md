# [High] Healthcheck endpoint typo can mark healthy app as unhealthy

- **Repository:** `portal-backend`
- **Severity:** **High**

## Evidence
- `portal-backend/docker-compose.yml:45 probes /api/helth (typo) instead of /api/health.`

## Impact
Container orchestration may repeatedly restart a healthy service due to false negatives.

## Recommendation
Correct path to /api/health and add CI lint to validate documented health endpoints.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
