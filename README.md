# CoreLink Java SDK

The future official Java SDK for CoreLink public APIs, including Java and
Spring-based partner applications.

## Current status

This repository is a scaffold: it contains no Java source, build descriptor or
published package. It is not ready to add as a dependency.

## Planned capabilities

- A typed client based on reviewed public API contracts.
- OAuth client-credential support with safe secret handling.
- Tenant-scoped device, provisioning, command, telemetry and event operations.
- Pagination, retries, structured problem responses and webhook verification.
- A supported Java baseline, dependency coordinates and Spring integration
  guidance.

## Contract and release policy

The SDK may expose only canonical CoreLink public concepts. Provider-specific
Traccar, OpenRemote and Keycloak models remain implementation details. Every
release must identify its compatible public API version and be tested against a
matching platform release.
