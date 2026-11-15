# SenGo Development Standards

## 1. General principles

- Build for a controlled PNG pilot, while avoiding architecture that prevents national expansion.
- Prefer simple, maintainable and low-cost solutions.
- Do not add paid services or subscriptions without explicit owner approval.
- Implement the approved requirements; do not silently expand product scope.
- Design mobile-first and consider low-bandwidth connectivity and lower-end Android devices.
- Treat security, privacy and delivery custody as core product requirements.

## 2. Technology status

The current proposed direction includes Next.js, Supabase/PostgreSQL, optional PostGIS, and OpenStreetMap-compatible mapping. These choices remain subject to architecture review and explicit approval before application bootstrap or paid infrastructure commitments.

## 3. Code conventions

When application code is introduced:

- Use clear, descriptive names.
- Prefer small, focused modules and functions.
- Keep business rules out of presentation components.
- Validate all untrusted input at system boundaries.
- Use explicit types for domain entities and state transitions.
- Avoid duplicated business logic between client and server.
- Keep configuration separate from source code.
- Explain non-obvious security or business-rule decisions in comments or documentation.

## 4. Naming

- Use PascalCase for React components and type names.
- Use camelCase for variables and functions.
- Use kebab-case for branch names and documentation filenames.
- Use clear domain terms from [the glossary](GLOSSARY.md).
- Use UTC timestamps in persisted event records; convert for display using the user's locale and an explicit timezone policy.

## 5. Data and security

- Enforce authorization on the server and database, not only in the UI.
- Apply least-privilege access.
- Keep identity evidence, contact details, private journeys and delivery evidence private by default.
- Do not expose private journey data through search, API responses, logs or QR codes.
- Make sensitive state changes auditable.
- Use synthetic data for development and tests.
- Define retention and deletion rules before collecting real user evidence.

## 6. Testing expectations

For application work, add or update tests appropriate to the change:

- Unit tests for business rules and validation.
- Integration tests for database and authorization behaviour.
- End-to-end tests for critical user workflows.
- Negative tests for unauthorised access and invalid state transitions.

A check must not be reported as passing unless it was actually run and passed. If the repository does not yet have an executable application or test runner, state that limitation clearly.

## 7. Pull request standards

- One focused issue or small related batch per pull request.
- Link the issue.
- Explain scope, design decisions and risks.
- Record tests run and tests not run.
- Keep generated files and unrelated changes out of the PR.
- Do not merge into `main` without explicit owner approval.

## 8. Accessibility and performance

- Use semantic HTML and accessible labels.
- Ensure keyboard-accessible controls.
- Provide useful loading, empty, success and error states.
- Compress and appropriately size images.
- Avoid unnecessary large dependencies.
- Ensure core flows remain understandable on small screens and slow connections.

## 9. Approval gates

Owner approval is required for main merges, production deployment, destructive actions, hosted database migrations, paid services, material scope changes and commercial pilot launch.
