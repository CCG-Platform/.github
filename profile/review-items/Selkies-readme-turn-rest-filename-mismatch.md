# [Medium] README command references non-existent manifest filename

- **Repository:** `Selkies`
- **Severity:** **Medium**

## Evidence
- `Selkies/readme.md:4 uses k8s-turn-rest.yaml.`
- `Repository contains Selkies/k8s-tun-rest.yaml (missing "r").`

## Impact
Setup command sequence fails for first-time users.

## Recommendation
Align README command and file naming (turn vs tun) and add quick smoke-check command.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
