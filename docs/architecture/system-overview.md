# ShopSphere — System Overview

## Initial architecture

A single FastAPI application will expose versioned REST endpoints.

Initially, data may be held in memory to teach HTTP and application fundamentals.

## Target evolution

Client
  -> Nginx
  -> FastAPI application
  -> PostgreSQL

FastAPI
  -> Redis for selected cached reads

Order processing
  -> RabbitMQ
  -> Celery workers

Operations
  -> Docker and Docker Compose
  -> Kubernetes
  -> Prometheus and Grafana

Delivery
  -> GitHub Actions

## Architecture principles

- PostgreSQL is the persistent source of truth.
- Redis is a cache, not the primary database.
- Background tasks must be designed for retries and duplicate delivery.
- Infrastructure is introduced incrementally.
- The architecture diagram will evolve as features are implemented.