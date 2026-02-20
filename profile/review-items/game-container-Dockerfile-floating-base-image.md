# [Medium] Container build starts from floating latest base image

- **Repository:** `game-container`
- **Severity:** **Medium**

## Evidence
- `game-container/Dockerfile:1 uses ghcr.io/selkies-project/nvidia-egl-desktop:latest.`

## Impact
Build reproducibility and vulnerability triage become harder when base moves implicitly.

## Recommendation
Pin to digest or explicit version tag and schedule controlled upgrade windows.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
