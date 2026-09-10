# Supply Chain

Build, packaging, and testing infrastructure that supports the operator and
its images without being the operator's reconciliation logic itself. See the
[subprojects index](README.md) for how this fits into the wider structure,
and [GOVERNANCE.md](../GOVERNANCE.md#subprojects) for how subprojects are
defined.

> See [subprojects/README.md](README.md) for who owns these repositories
> and this file's own edit rights.

## Distribution

How the operator and its clusters get to users: Helm charts, generated
manifests and catalogs, and listings in other platforms' marketplaces.

| Repository | Description |
| --- | --- |
| [charts](https://github.com/cloudnative-pg/charts) | Official Helm charts for the operator, database clusters and the Barman Cloud plugin. |
| [artifacts](https://github.com/cloudnative-pg/artifacts) | Storage for generated manifests, checksums, metadata, and image catalogs. |
| [community-operators](https://github.com/cloudnative-pg/community-operators) | Fork of the upstream [k8s-operatorhub/community-operators](https://github.com/k8s-operatorhub/community-operators), used only to submit the operator's OperatorHub bundle upstream via PR (see note below). |

> `community-operators` is a fork of an external project, not a
> CloudNativePG-authored codebase, so it doesn't follow the same ownership
> model as the rest of this table: there's no ongoing feature review to gate
> with `CODEOWNERS`, just occasional pushes to update the bundle before
> opening a PR upstream. `@cloudnative-pg/supply-chain-maintainers` still
> needs `Maintain` access to push those updates, but "owns" it only in the
> sense of keeping it in sync, not technical authority over its content
> (that belongs to the upstream project).

## Container Images

Standardized images built for security, minimal footprint, and CNPG compatibility.

| Repository | Description |
| --- | --- |
| [postgres-containers](https://github.com/cloudnative-pg/postgres-containers) | Operand images for all community-supported PostgreSQL versions. |
| [postgres-extensions-containers](https://github.com/cloudnative-pg/postgres-extensions-containers) | Images for community extensions used as pluggable image volumes. |
| [pgbouncer-containers](https://github.com/cloudnative-pg/pgbouncer-containers) | Optimized images for PgBouncer connection pooling. |
| [postgis-containers](https://github.com/cloudnative-pg/postgis-containers) | PostgreSQL images bundled with PostGIS extensions. |
| [postgres-trunk-containers](https://github.com/cloudnative-pg/postgres-trunk-containers) | Images built from PostgreSQL `main` branch for early testing. |

## Libraries & Automation

Shared, reusable infrastructure consumed by other components, distinct from
the operator's own code even when extracted into a separate repository. Two
things that might look like they belong here don't: `api` and `machinery`
are the operator's own logic split out for Go module reasons (see
[Core](core.md)), and `barman-cloud` supports a single plugin rather than
being reused across several, so it sits with that plugin under
[Extensibility](extensibility.md).

| Repository | Description |
| --- | --- |
| [daggerverse](https://github.com/cloudnative-pg/daggerverse) | Dagger modules for portable CI/CD workflows. |

> `cnpg-template` used to be listed here. It's now classified as
> org-control infrastructure administered directly by the Steering
> Committee instead, alongside `governance`, `.project`, `.github`, and
> `cnpg-infra`. See [GOVERNANCE.md's Subprojects section](../GOVERNANCE.md#subprojects)
> and [subprojects/README.md](README.md).

## Testing & Automation

Tools dedicated to CI/CD, resilience testing, and GitHub Actions development.

| Repository | Description |
| --- | --- |
| [ciclops](https://github.com/cloudnative-pg/ciclops) | The Continuous Integration Circular Operations tool for the project. |
| [chaos-testing](https://github.com/cloudnative-pg/chaos-testing) | Infrastructure and scripts for running chaos experiments against CNPG. |
| [github-test](https://github.com/cloudnative-pg/github-test) | Playground and testing ground for GitHub Actions and automation workflows. |
