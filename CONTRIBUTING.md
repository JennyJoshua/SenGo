# Contributing to SenGo

Thank you for helping build SenGo.

## Current project stage

SenGo is in its foundation and specification stage. Changes must follow the approved business model and must not imply that the service is legally cleared or operational.

## Before starting work

1. Read the repository [README](README.md).
2. Read [Product Rules](docs/PRODUCT_RULES.md).
3. Read [Development Standards](docs/DEVELOPMENT_STANDARDS.md).
4. Find the relevant GitHub Issue.
5. Confirm that the issue is not blocked by a dependency or approval gate.

## Branching

- Keep `main` stable.
- Use a focused branch for each issue or tightly related small batch.
- Suggested format: `docs/issue-<number>-short-name`, `feat/issue-<number>-short-name`, or `fix/issue-<number>-short-name`.
- Do not commit unfinished feature work directly to `main`.

## Commits

Use concise, descriptive commit messages. Suggested prefixes:

- `docs:` documentation
- `feat:` new functionality
- `fix:` defect correction
- `test:` tests
- `chore:` maintenance and tooling
- `security:` security-related changes

## Pull requests

Every pull request should:

- Link the relevant issue using `Closes #<number>` only when it fully completes that issue.
- Explain what changed and why.
- List tests and checks performed, including any not run.
- Identify security, privacy, legal or data migration implications.
- Stay within the approved issue scope.
- Include screenshots only when they materially help review UI changes.

Do not merge a pull request without the owner's explicit approval.

## Safety and approval gates

Explicit owner approval is required before:

- Merging into `main`.
- Production deployment.
- Destructive repository or data actions.
- Hosted database migrations.
- Paid services, upgrades or subscriptions.
- Material scope or business-model changes.
- Starting the commercial pilot.

Legal or regulatory questions must not be resolved by assumptions. Record unresolved items as blockers and seek qualified PNG advice where needed.

## Secrets and personal information

- Never commit credentials, API keys, access tokens, passwords or private keys.
- Use local environment variables or an approved secrets manager.
- Do not put real identity documents, private user data or delivery evidence in test fixtures.
- Use synthetic data in development and tests.
