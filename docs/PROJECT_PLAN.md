# ShopSphere — Project Plan

## Phase 0: Project initiation

- Define scope, requirements, assumptions, and acceptance criteria.
- Establish repository documentation and Git workflow.
- Record the initial architecture decision.
- Verify the first documentation commit is pushed.

Exit criteria: documentation is committed and available on GitHub.

## Phase 1: Core API

- Learn HTTP, REST, routing, Pydantic, and dependency injection.
- Implement health, product, cart, and order endpoints.
- Introduce automated tests and consistent error handling.

Exit criteria: endpoints meet their acceptance criteria and tests pass.

## Phase 2: Database

- Evaluate PostgreSQL setup options.
- Design relational models and constraints.
- Introduce SQLAlchemy 2.0 and Alembic.
- Implement transactions and integration tests.

Exit criteria: data persists across restarts and failed transactions preserve consistency.

## Phase 3: Authentication

- Implement registration and login.
- Hash passwords and issue expiring tokens.
- Enforce authorization and resource ownership.

Exit criteria: protected operations reject unauthorized requests.

## Phase 4: Caching

- Establish a database-backed performance baseline.
- Add Redis and a cache-aside strategy.
- Implement TTL and invalidation.

Exit criteria: cache behavior is tested and stale data risks are addressed.

## Phase 5: Background processing

- Introduce RabbitMQ and Celery.
- Add asynchronous post-order tasks.
- Explore retries, idempotency, and failure recovery.

Exit criteria: background processing is independently testable and duplicate delivery is handled safely.

## Phase 6: Reverse proxy

- Configure Nginx and upstream routing.
- Test timeouts and error behavior.

Exit criteria: application requests can be routed through the proxy.

## Phase 7: Containers

- Create Docker images and Compose configuration.
- Configure networking, environment variables, volumes, and health checks.

Exit criteria: services start reproducibly from documented instructions.

## Phase 8: Kubernetes

- Deploy workloads to a local cluster.
- Learn Services, probes, resources, and replica scaling.

Exit criteria: deployments and basic recovery behavior are verified.

## Phase 9: Load testing

- Establish a baseline.
- Gradually increase workload using k6.
- Analyze latency, throughput, and errors.

Exit criteria: results and limitations are documented.

## Phase 10: Monitoring

- Expose and collect application metrics.
- Configure Prometheus and Grafana dashboards.

Exit criteria: relevant metrics can be observed under a controlled workload.

## Phase 11: CI/CD

- Automate linting and tests using GitHub Actions.
- Build container images in CI.
- Add deployment automation only when justified.

Exit criteria: failing checks block successful CI completion.

## Working method

For every feature: plan, define acceptance criteria, compare alternatives, design, implement, test, review, document, and commit.

Phases are sequential by default, but the plan may be refined as dependencies become clearer.