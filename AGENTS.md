# CoreLink Java SDK Agent Context

This repository is part of the CoreLink product.

## Canonical context

Follow `CoreLinkPlatform/product-planning/AGENTS.md`, `PRODUCT_ARCHITECTURE.md`, `GLOSSARY.md`, `STANDARDS.md`, and `architecture/repository-map.yaml`. Public API behavior is normative in `CoreLinkPlatform/api-contracts`.

## Repository responsibility

`sdk-java` provides the supported Java developer interface for CoreLink public APIs.

## Boundaries

- Generate or implement behavior from supported public contracts; do not invent endpoints or fields.
- Preserve compatibility according to contract/versioning policy.
- Do not expose internal provider models or implementation-only identifiers.
- Keep ergonomics idiomatic for Java without changing CoreLink domain semantics.
- Examples and documentation must use canonical terminology.
