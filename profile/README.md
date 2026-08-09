

## Enterprise foundations. Startup speed.
### Spend your runway on product differentiation - not engineering foundations.

Backbone gives funded SaaS teams Year 3 operational maturity immediately — forked into your own AWS account in about two days, for a fraction of what building it yourself costs.

[Backbone](https://backbonehq.io/) consists of the following discrete repositories:

| Repository                                            | Visibility | Description                                                                                         |
|-------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------|
| [backbone-kit](https://github.com/get-backbone/backbone-kit)   | Public     | Infrastructure components for Quarkus services: rate limiting, metrics, health checks.     |
| `backbone-core`                                       | Private    | Platform maturity that normally only emerges after several years of operational iteration. |
| `backbone-platform`                                   | Private    | A filtered mirror of `backbone-core` that clients will fork, own and run with a licence.            |
| [backbone-docs](https://github.com/get-backbone/backbone-docs) | Public     | This public documentation repository.                                                      |


Backbone provides the following:

- A development environment built on free tier Floci that emulates AWS in full and spins up in seconds.
- An entire GitHub Actions pipeline which includes release automation; ECS deployments (diffed services only); infrastructure
  deployments (CDK); static code analysis (OWASP, SpotBugs, etc); code coverage, unit/integration test reports, and more.
- Full IaC support and repeatable automation for AWS environments, including thoughtful segregation of stateful vs stateless resources (FinOps).
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

For more detailed information, check out the [Backbone](https://backbonehq.io/) website and the [docs](https://docs.backbonehq.io/).
