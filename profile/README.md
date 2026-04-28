# Production-grade microservices from day one.

## Enterprise foundations. Startup speed.

The [Forge Platform](https://forgeplatform.software/) consists of the following discreet repositories:

| Repository                                            | Visibility | Description                                                                                         |
|-------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------|
| [forge-kit](https://github.com/get-forge/forge-kit)   | Public     | Infrastructure components for Quarkus services: rate limiting, metrics, health checks.              |
| `forge-core`                                          | Private    | A zero-trust, horizontally scalable microservices platform built with Quarkus, and deployed on AWS. |
| `forge-platform`                                      | Private    | A filtered mirror of `forge-core` that clients will fork, own and run with a licence.               |
| [forge-docs](https://github.com/get-forge/forge-docs) | Public     | This public documentation repository.                                                               |


The Forge Platform provides you with the following:

- A development environment built predominantly on free tier LocalStack that emulates AWS in full and spins up in seconds.
- An entire GitHub Actions pipeline which includes release automation; ECS deployments (diffed services only); infrastructure
  deployments (CDK); static code analysis (OWASP, SpotBugs, etc); code coverage, unit/integration test reports, and more.
- Full IaC support and repeatable automation for AWS environments, including thoughtful segregation of stateful vs stateless resources.
- A clean, well-documented, and well-tested codebase that you can fork and modify.
- A stateless reference web application that you can deploy locally and to AWS and use immediately.
- The following foundational services provide the base for you to build domain services (e.g. search, quote, booking, etc.):
  - actor-service; canonical user profile and identity-linked domain data
  - audit-service; immutable event and action trail for compliance and observability
  - auth-service; JWT issuance, validation, and user/service authentication workflows
  - document-service; document metadata, storage orchestration, and retrieval APIs
  - notification-service; template-driven outbound messaging and delivery orchestration
- The following edge services that provide client-facing composition and delivery layers:
  - backend-actor; BFF orchestration tier
  - backend-web; disposable reference UI and consumable frontend
- Comprehensive Prometheus metrics and Grafana dashboards for observability.

For more detailed information, check out the [Forge Platform](https://forgeplatform.software/) website and [Technical Documentation](https://get-forge.github.io/forge-docs/).
