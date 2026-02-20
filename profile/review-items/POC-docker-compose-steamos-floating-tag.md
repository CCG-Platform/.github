# [Medium] Compose runtime depends on floating latest image

- **Repository:** `POC`
- **Severity:** **Medium**

## Evidence
- `POC/docker-compose.yaml:5 uses lscr.io/linuxserver/steamos:latest.`

## Impact
Unpinned base image can introduce unexpected runtime changes.

## Recommendation
Pin image digest or explicit version tag and document upgrade cadence.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
