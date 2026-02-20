# [Low] Quick Start assumes parent-folder clone layout

- **Repository:** `Document`
- **Severity:** **Low**

## Evidence
- `Document/README.md:38-39 uses cp Document/templates/... paths.`

## Impact
Commands fail for users executing from within the Document repo root.

## Recommendation
Use repo-local paths (templates/...) and add both usage variants if needed.

## Validation notes
- Evidence collected via direct repository inspection in worker-2 review pass.
