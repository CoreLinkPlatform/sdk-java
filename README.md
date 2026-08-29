# CoreLink Java SDK

> **Maturity: Scaffold / Planned** — there is no supported Java source tree, build descriptor, dependency coordinate, or published artifact yet.

This repository is the planned official Java/Spring client boundary for versioned CoreLink public APIs.

## Planned baseline

The first supported implementation must define:

- supported Java runtime baseline;
- build tool and package coordinates;
- reproducible generation from versioned CoreLink OpenAPI contracts;
- immutable contract provenance in generated/released artifacts;
- OAuth/Bearer authentication and explicit tenant context;
- typed problem/error behavior and bounded retries;
- Spring-oriented integration guidance where useful;
- conformance against an accepted mock/sandbox/runtime revision.

## Public-contract rules

The SDK may expose only CoreLink-owned public concepts. Provider-specific device/connectivity/identity models remain implementation details. Generated schemas must not be hand-edited to create a Java-only public contract.

## Backlog

- [JAVA-01](https://github.com/CoreLinkPlatform/sdk-java/issues/2) — Java baseline, build, coordinates and generation.
- [JAVA-02](https://github.com/CoreLinkPlatform/sdk-java/issues/3) — authentication, tenant context, typed errors/retries and Spring guidance.
- [JAVA-03](https://github.com/CoreLinkPlatform/sdk-java/issues/4) — signed prerelease/stable artifacts with conformance.

## Release requirements

Before publishing a supported artifact, the release must identify compatible contract/runtime revisions, satisfy organization provenance/signing policy, pass tenant/auth/error/recovery conformance, and document prerelease versus Stable maturity.

## Related sources

- [API contracts](https://github.com/CoreLinkPlatform/api-contracts)
- [Developer docs](https://github.com/CoreLinkPlatform/developer-docs)
- [Release policy](https://github.com/CoreLinkPlatform/.github/blob/main/RELEASE_POLICY.md)

Do not add Maven/Gradle coordinates from planning text to an application until this repository publishes a real versioned package.