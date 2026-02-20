# [High] Access token stored in localStorage

- **Repository:** `CCGP-ui`
- **Severity:** **High**

## Evidence
- `CCGP-ui/src/components/hook/auth/HookLogin.jsx:30-33 stores accessToken in localStorage.`

## Impact
localStorage tokens are readable by injected JavaScript, increasing blast radius of XSS.

## Recommendation
Prefer httpOnly secure cookies or keep short-lived tokens in memory with refresh-token rotation.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
