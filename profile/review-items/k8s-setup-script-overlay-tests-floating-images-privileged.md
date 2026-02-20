# [Medium] NFS overlay tests combine privileged init with floating images

- **Repository:** `k8s-setup-script`
- **Severity:** **Medium**

## Evidence
- `k8s-setup-script/NFS_mount_test/merge_test.yaml:10 uses alpine:latest and privileged initContainer.`
- `k8s-setup-script/NFS_mount_test/merge_test.yaml:32 uses ubuntu:latest.`
- `k8s-setup-script/NFS_mount_test/overlay_test.yaml:10 and :31 repeat same pattern.`

## Impact
Test manifests can drift unexpectedly and set insecure copy patterns for operators.

## Recommendation
Pin test image tags and add warning comments about privileged usage scope.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
