# Repository Structure

This document describes the intended structure for SenGo. It is a planning baseline, not a claim that all application folders or services have already been implemented.

## Current structure

```text
.
├── .env.example
├── .gitignore
├── CONTRIBUTING.md
├── README.md
└── docs/
    ├── DEVELOPMENT_STANDARDS.md
    ├── GLOSSARY.md
    ├── PRODUCT_RULES.md
    ├── REPOSITORY_STRUCTURE.md
    └── DELIVERY_LIFECYCLE.md
```

## Proposed application structure

The following layout is proposed for the application bootstrap. Final paths may be refined when the framework and deployment architecture are approved.

```text
.
├── app/                    # Web application routes and layouts
├── components/             # Reusable UI components
├── features/               # Feature-oriented application modules
├── lib/                    # Shared utilities and integrations
├── types/                  # Shared TypeScript types
├── public/                 # Static assets
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── supabase/
│   ├── migrations/
│   └── seed/
└── docs/
    ├── architecture/
    ├── decisions/
    ├── operations/
    └── product/
```

## Structure principles

1. Keep product features grouped by domain where practical.
2. Keep database migrations version-controlled.
3. Separate public assets from private uploaded evidence.
4. Never store secrets in source control.
5. Keep tests close to the behaviour they validate or in clearly named test folders.
6. Keep product, architecture, security and operational decisions documented.
7. Avoid introducing infrastructure that is not needed for the approved MVP.

## Proposed technology direction

Next.js, Supabase/PostgreSQL, PostGIS and OpenStreetMap-compatible mapping have been identified as candidates in the backlog. They are not yet a final, approved implementation stack. No paid service or upgrade is authorised by this document.
