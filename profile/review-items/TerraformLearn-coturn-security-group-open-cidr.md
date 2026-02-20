# [Medium] Coturn security group examples open ports to world

- **Repository:** `TerraformLearn`
- **Severity:** **Medium**

## Evidence
- `TerraformLearn/setup/06-coturn-setup.md:286,292,298 use --cidr 0.0.0.0/0.`

## Impact
Wide-open ingress examples can lead to unnecessary exposure and abuse costs.

## Recommendation
Constrain CIDRs where possible and explicitly label 0.0.0.0/0 as temporary test-only guidance.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
