# [Medium] Request mixes bearer token and credentialed cookie flow

- **Repository:** `CCGP-ui`
- **Severity:** **Medium**

## Evidence
- `CCGP-ui/src/components/hook/workspace/ConnectWorkspace.jsx:26-28 sends Authorization bearer token and withCredentials: true together.`

## Impact
Dual-auth patterns are error-prone and complicate CSRF/session hardening.

## Recommendation
Choose one canonical auth transport per endpoint and document expected session model clearly.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
