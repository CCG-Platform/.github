# [Critical] Workspace runtime injects hardcoded password and TURN secret

- **Repository:** `demo`
- **Severity:** **Critical**

## Evidence
- `demo/k8s_handler.py:100 sets PASSWD to mypasswd.`
- `demo/k8s_handler.py:106 sets long static SELKIES_TURN_SHARED_SECRET.`
- `demo/k8s_handler.py:120 uses floating nvidia-egl-desktop:latest image.`

## Impact
Hardcoded credentials materially increase credential leakage and unauthorized access risk.

## Recommendation
Move all secrets to Kubernetes Secret resources and use immutable, pinned image references.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
