# Core

The operator itself, plus repositories that are effectively its own logic
rather than genuinely independent infrastructure, even though they live in
separate GitHub repositories: `api` and `machinery` are split out for Go
module reasons (see [Supply Chain's "Libraries & Automation"](supply-chain.md#libraries--automation)
for the distinction). Primarily the maintainers' responsibility;
path-level review-routing within the `cloudnative-pg` component is tracked
in [`cnpg-infra`'s `componentowners-policy.yaml`](https://github.com/cloudnative-pg/cnpg-infra/blob/main/componentowners-policy.yaml),
not here (see [GOVERNANCE.md's Subprojects section](../GOVERNANCE.md#subprojects)).
See the [subprojects index](README.md) for how this fits
into the wider structure, and [GOVERNANCE.md](../GOVERNANCE.md#subprojects)
for how subprojects are defined.

> See [subprojects/README.md](README.md) for who owns these repositories
> and this file's own edit rights, both apply here unchanged.

| Repository | Description |
| --- | --- |
| [cloudnative-pg](https://github.com/cloudnative-pg/cloudnative-pg) | The main Kubernetes Operator for PostgreSQL. |
| [api](https://github.com/cloudnative-pg/api) | The CloudNativePG API definitions and types. |
| [machinery](https://github.com/cloudnative-pg/machinery) | Common Go library for internal logic (extracted from the operator). |
