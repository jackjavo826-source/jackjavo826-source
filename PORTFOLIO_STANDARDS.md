# Portfolio documentation standards

These repositories document personal engineering work. Every project should state its current maturity and make its evidence easy to inspect.

## Project record

| Section | What to record |
| --- | --- |
| Problem | Intended user, constraints, and a concrete success criterion |
| Status | Concept, prototype, tested, or released; identify missing evidence |
| Design | Architecture, interfaces, assumptions, and rejected alternatives |
| Setup | Hardware revision, dependencies, tool versions, wiring, and build/run steps |
| Verification | Date, environment, procedure, expected behavior, actual result, and limitations |
| Results | Measurements, screenshots, demonstrations, and links to the tested commit |
| Next steps | Specific unresolved engineering questions |

A planned test is not a passing test. Label simulated results, estimates, AI-assisted work, and hardware measurements accurately. Avoid performance or reliability claims without supporting evidence.

## Suggested repository layout

- `README.md`: overview, status, navigation, setup, and limitations
- `docs/`: design decisions, requirements, and test records
- `src/` or named project folders: reviewed source
- `examples/`: minimal, sanitized examples
- `tests/`: checks that exercise actual behavior

Create directories when they contain useful material; do not add empty placeholders.

## Publication review

Before a source release:

1. Review every file and the commit history for passwords, tokens, private keys, personal paths, network details, and identifying metadata.
2. Replace machine-specific values with documented examples or configuration variables.
3. Confirm ownership and permission to publish. Exclude restricted assignments, answer keys, course materials, and third-party content without permission.
4. Preserve required attribution and dependency notices. Add a license only after confirming the rights to the included work.
5. Build or run the relevant checks and record their actual outcome. State any hardware or environment that was unavailable.
6. Review the staged diff and verify the public result after publishing.

A `.gitignore` is a convenience, not a secret scanner; it does not remove previously committed data. If a credential is exposed, revoke it before addressing repository history.

## Security reports

Do not post credentials or exploitable private system details in public issues. Use GitHub private vulnerability reporting when available. Public issues should contain a minimal, sanitized reproduction.
