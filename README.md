[![CloudNativePG](./logo/cloudnativepg.png)](https://cloudnative-pg.io/)

# CloudNativePG Governance

This repository contains the governance documents for the CloudNativePG
project:

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Governance Policy](./GOVERNANCE.md)
- [Contributing guidelines](./CONTRIBUTING.md)
- [AI Policy](./AI_POLICY.md)
- [List of Maintainers](./MAINTAINERS.md)
- [List of Component owners](./COMPONENT-OWNERS.md)
- [List of Contributors](./CONTRIBUTORS.md)
- [License](./LICENSE)

## Repositories

### Core Projects

The primary components for deploying and managing the project lifecycle.

| Repository | Description |
| --- | --- |
| [governance](https://github.com/cloudnative-pg/governance) | Central hub for project policies, AI policy, and general guidelines. |
| [cloudnative-pg](https://github.com/cloudnative-pg/cloudnative-pg) | The main Kubernetes Operator for PostgreSQL. |
| [charts](https://github.com/cloudnative-pg/charts) | Official Helm charts for the operator, database clusters and the Barman Cloud plugin. |
| [artifacts](https://github.com/cloudnative-pg/artifacts) | Storage for generated manifests, checksums, metadata, and image catalogs. |
| [cnpg-template](https://github.com/cloudnative-pg/cnpg-template) | A template repository for creating new CloudNativePG-related projects. |

### Container Images

Standardized images built for security, minimal footprint, and CNPG compatibility.

| Repository | Description |
| --- | --- |
| [postgres-containers](https://github.com/cloudnative-pg/postgres-containers) | Operand images for all community-supported PostgreSQL versions. |
| [postgres-extensions-containers](https://github.com/cloudnative-pg/postgres-extensions-containers) | Images for community extensions used as pluggable image volumes. |
| [pgbouncer-containers](https://github.com/cloudnative-pg/pgbouncer-containers) | Optimized images for PgBouncer connection pooling. |
| [postgis-containers](https://github.com/cloudnative-pg/postgis-containers) | PostgreSQL images bundled with PostGIS extensions. |
| [postgres-trunk-containers](https://github.com/cloudnative-pg/postgres-trunk-containers) | Images built from PostgreSQL `main` branch for early testing. |
| [pgcrash-containers](https://github.com/cloudnative-pg/pgcrash-containers) | Container images for `pg_crash` to test PostgreSQL resilience. |

### Community, Docs & Monitoring

User-facing resources, observability, and distribution.

| Repository | Description |
| --- | --- |
| [docs](https://github.com/cloudnative-pg/docs) | The documentation project and Hugo source for the operator docs. |
| [cloudnative-pg.github.io](https://github.com/cloudnative-pg/cloudnative-pg.github.io) | The main project landing page/website. |
| [cnpg-playground](https://github.com/cloudnative-pg/cnpg-playground) | Local learning environment scripts using Docker/Kind. |
| [grafana-dashboards](https://github.com/cloudnative-pg/grafana-dashboards) | Standardized Grafana dashboards for monitoring CNPG clusters. |
| [community-operators](https://github.com/cloudnative-pg/community-operators) | Fork for publishing the operator to OperatorHub.io. |
| [webtest](https://github.com/cloudnative-pg/webtest) | Internal tooling for website and documentation testing. |

### Libraries & Automation

Shared logic, API definitions, and CI/CD modules consumed by other components.

| Repository | Description |
| --- | --- |
| [api](https://github.com/cloudnative-pg/api) | The CloudNativePG API definitions and types. |
| [machinery](https://github.com/cloudnative-pg/machinery) | Common Go library for internal logic (extracted from the operator). |
| [barman-cloud](https://github.com/cloudnative-pg/barman-cloud) | Go library for interacting with Barman Cloud object stores. |
| [daggerverse](https://github.com/cloudnative-pg/daggerverse) | Dagger modules for portable CI/CD workflows. |

### Interface & Plugins (CNPG-I)

The extensibility layer that allows for custom backups and additional logic.

| Repository | Description |
| --- | --- |
| [cnpg-i](https://github.com/cloudnative-pg/cnpg-i) | The CloudNativePG Interface (CNPG-I) gRPC specification. |
| [cnpg-i-machinery](https://github.com/cloudnative-pg/cnpg-i-machinery) | Shared Go code for developing CNPG-I compatible plugins. |
| [plugin-barman-cloud](https://github.com/cloudnative-pg/plugin-barman-cloud) | The reference CNPG-I backup/restore plugin for Barman Cloud. |
| [cnpg-i-hello-world](https://github.com/cloudnative-pg/cnpg-i-hello-world) | A simplified template/example for building new plugins. |

### PostgreSQL Modules & Extensions

Software designed to run inside or alongside the PostgreSQL database engine.

| Repository | Description |
| --- | --- |
| [postgres-keycloak-oauth-validator](https://github.com/cloudnative-pg/postgres-keycloak-oauth-validator) | A PostgreSQL module for OAuth2/Keycloak token validation. |

### Testing & Automation

Tools dedicated to CI/CD, resilience testing, and GitHub Actions development.

| Repository | Description |
| --- | --- |
| [ciclops](https://github.com/cloudnative-pg/ciclops) | The Continuous Integration Circular Operations tool for the project. |
| [chaos-testing](https://github.com/cloudnative-pg/chaos-testing) | Infrastructure and scripts for running chaos experiments against CNPG. |
| [github-test](https://github.com/cloudnative-pg/github-test) | Playground and testing ground for GitHub Actions and automation workflows. |
