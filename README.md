# CoreLink Java SDK

> **Maturity: Experimental / Generated Baseline** — reproducible Java generation/build now exists, but there is no supported Maven Central/Stable artifact yet.

This repository is the official Java/Spring client boundary for versioned CoreLink public APIs.

## Current baseline

- Java: 17+
- generated from `corelink-public-v1.yaml` `1.0.0-draft`
- immutable contract commit: `5bdc07b80c8acbd0617b75e2d7ae3edd17f6324b`
- OpenAPI Generator: `7.12.0`
- planned coordinates: `io.corelink:corelink-sdk`
- current generated prerelease version: `0.1.0-SNAPSHOT`

CI generates the client from the pinned immutable contract and compiles the generated Maven project. See [CODEGEN.md](CODEGEN.md) and [`.corelink-contract.json`](.corelink-contract.json).

## What this baseline proves

- Java build/runtime baseline and coordinates are defined.
- Code generation is reproducible from an immutable contract input.
- Public models are generated from CoreLink-owned schemas instead of hand-written Java-only contracts.
- Provider-specific device/connectivity/identity models remain internal implementation details.

## What is not supported yet

- Maven Central or another supported public artifact channel.
- Stable compatibility guarantees.
- Java-specific OAuth/session ergonomics, retry policy or typed convenience wrappers beyond generated behavior.
- Spring integration guarantees.
- Sandbox/conformance acceptance for the broader API surface.

Those are owned by JAVA-02/JAVA-03.

## Backlog

- [JAVA-01](https://github.com/CoreLinkPlatform/sdk-java/issues/2) — Java baseline, build, coordinates and generation.
- [JAVA-02](https://github.com/CoreLinkPlatform/sdk-java/issues/3) — authentication, tenant context, typed errors/retries and Spring guidance.
- [JAVA-03](https://github.com/CoreLinkPlatform/sdk-java/issues/4) — signed prerelease/stable artifacts with conformance.

## Contract rules

The SDK exposes only CoreLink-owned public concepts. Provider-specific IDs, raw protocol payloads and Control/internal APIs are not part of the Java public SDK contract.

## Related sources

- [API contracts](https://github.com/CoreLinkPlatform/api-contracts)
- [Developer docs](https://github.com/CoreLinkPlatform/developer-docs)
- [Release policy](https://github.com/CoreLinkPlatform/.github/blob/main/RELEASE_POLICY.md)
- [Repository maturity](https://github.com/CoreLinkPlatform/.github/blob/main/REPOSITORY_MATURITY.md)
