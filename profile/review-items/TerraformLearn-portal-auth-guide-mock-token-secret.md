# [High] Auth guide includes mock token logic and default TURN secret

- **Repository:** `TerraformLearn`
- **Severity:** **High**

## Evidence
- `TerraformLearn/setup/04-portal-and-auth.md:43-46 validates literal valid-token.`
- `TerraformLearn/setup/04-portal-and-auth.md:74 hardcodes fallback TURN secret.`
- `TerraformLearn/setup/04-portal-and-auth.md:101-102 uses placeholder user_id logic.`

## Impact
Copy-paste adoption risks insecure auth behavior leaking into real environments.

## Recommendation
Mark as pseudocode or replace with production-safe examples that force external secret/auth providers.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
