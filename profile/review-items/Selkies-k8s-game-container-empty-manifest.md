# [High] Referenced game-container manifest is empty

- **Repository:** `Selkies`
- **Severity:** **High**

## Evidence
- `Selkies/readme.md:5 instructs apply of k8s-game-container.yaml.`
- `Selkies/k8s-game-container.yaml is 0 bytes.`

## Impact
Documented deployment path cannot provision workload as described.

## Recommendation
Provide a valid manifest template or remove instruction until file is implemented.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
