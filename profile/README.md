

## Enterprise foundations. Startup speed.
### Spend your runway on product differentiation - not engineering foundations.

Backbone gives funded SaaS teams Year 3 operational maturity immediately — forked into your own AWS account in about two days, for a fraction of what building it yourself costs.

[Backbone](https://backbonehq.io/) consists of the following discrete repositories:

| Repository                                                               | Visibility | Description                                                                                                         |
|--------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------|
| [backbone-kit](https://github.com/get-backbone/backbone-kit)             | Public     | Quarkus security + observability primitives: throttling, metrics, health checks etc.                                |
| [backbone-community](https://github.com/get-backbone/backbone-community) | Public     | Free community starter. Develop and run **all** Backbone services locally.                                          |
| `backbone-core`                                                          | Private    | Platform maturity that normally only emerges after several years of operational iteration.                          |
| `backbone-platform`                                                      | Private    | A mirror of `backbone-core` that clients fork, own and run. Includes AWS infrastructure and deployment golden path. |
| [backbone-docs](https://github.com/get-backbone/backbone-docs)           | Public     | Documentation repository published to the [readme platform](https://docs.backbonehq.io/).                           |


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

## Upstream contributions

Issues and fixes we have raised or validated against the tools Backbone depends on:

| Project | Contribution | Status |
|---------|--------------|--------|
| [Floci](https://github.com/floci-io/floci) | Cognito `InitiateAuth` + `REFRESH_TOKEN_AUTH` accepted arbitrary refresh tokens ([#2113](https://github.com/floci-io/floci/issues/2113)) | Fixed in [1.7.0](https://github.com/floci-io/floci/releases/tag/1.7.0) |
