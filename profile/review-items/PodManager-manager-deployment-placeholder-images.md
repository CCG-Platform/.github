# [High] Production manifests still contain placeholder/personal image refs

- **Repository:** `PodManager`
- **Severity:** **High**

## Evidence
- `PodManager/production/manager-deployment.yaml:26 uses nukunga123/pod-manager:latest.`
- `PodManager/production/manager-deployment.yaml:37 uses nukunga123/user-app:latest.`
- `PodManager/production_api/manager-deployment.yaml:37 uses nukunga123/user-app:latest.`

## Impact
Deployments may pull non-governed images and fail provenance/compliance expectations.

## Recommendation
Replace with organization-owned immutable images and enforce via CI validation.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
