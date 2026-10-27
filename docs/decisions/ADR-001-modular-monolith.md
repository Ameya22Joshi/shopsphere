# ADR-001: Start with a Modular Monolith

- Status: Accepted
- Date: 2026-10-28

## Context

ShopSphere is a learning project intended to teach backend fundamentals before distributed-system complexity is introduced.

## Decision

Start with a single FastAPI application organized into modules with clear responsibilities. Introduce separate workers and supporting infrastructure as the relevant milestones require them.

## Alternatives considered

1. Independent microservices from the beginning.
2. A single unstructured Python file.
3. A modular monolith that can evolve incrementally.

## Rationale

A modular monolith makes local development, testing, and debugging simpler while teaching HTTP, application design, data access, and business logic.

## Consequences

Positive:
- Lower initial complexity.
- Simpler local setup.
- Clearer learning progression.
- Easier integration testing.

Trade-offs:
- Independent service deployment and scaling are not available initially.
- Distributed failure modes must be introduced in later phases.

## Revisit conditions

Revisit when independent deployment, scaling, or failure isolation becomes a meaningful requirement, or when a specific learning milestone requires a separate process.