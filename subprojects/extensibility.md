# Extensibility

The interfaces, modules, and standalone tooling that let CloudNativePG and
PostgreSQL be extended or operated on without changing the operator's core,
including the plugin-based backup and recovery ecosystem
(`plugin-barman-cloud`, `klio`) and the libraries behind it, and Postgres
tooling that has nothing to do with Kubernetes at all. See the
[subprojects index](README.md) for how this fits into the wider structure,
and [GOVERNANCE.md](../GOVERNANCE.md#subprojects) for how subprojects are
defined.

> See [subprojects/README.md](README.md) for who owns these repositories
> and this file's own edit rights.

`plugin-barman-cloud` is the template to follow when classifying a new
CNPG-I plugin:

- The plugin itself (the thing that talks to CNPG) belongs under
  "Interface & Plugins (CNPG-I)" below.
- A shared library reused across multiple plugins, and genuinely independent
  of any one of them, belongs under
  [Supply Chain's "Libraries & Automation"](supply-chain.md#libraries--automation)
  instead.
- Anything Postgres-native that isn't delivered as a CNPG-I plugin, whether a
  compiled extension/module (like `postgres-keycloak-oauth-validator`) or a
  standalone tool or utility that operates on Postgres independent of
  Kubernetes, belongs under "PostgreSQL Extensions & Tooling" below. Being
  Postgres-native rather than Kubernetes-native is what puts a project here
  rather than under Core or Supply Chain.

`barman-cloud`, the library `plugin-barman-cloud` wraps, sits here with the
plugin rather than under Supply Chain: the second bullet above is for a
library reused across several plugins and independent of any one of them,
and this one supports a single plugin. It was previously listed under
[Core](core.md), on the grounds that the operator still consumes it
directly for native backup and restore; it moved here as a routine
editorial change, ahead of that native support being removed, rather than
waiting for it.

## Interface & Plugins (CNPG-I)

The extensibility layer that allows for custom backups and additional logic.

| Repository | Description |
| --- | --- |
| [cnpg-i](https://github.com/cloudnative-pg/cnpg-i) | The CloudNativePG Interface (CNPG-I) gRPC specification. |
| [cnpg-i-machinery](https://github.com/cloudnative-pg/cnpg-i-machinery) | Shared Go code for developing CNPG-I compatible plugins. |
| [plugin-barman-cloud](https://github.com/cloudnative-pg/plugin-barman-cloud) | The reference CNPG-I backup/restore plugin for Barman Cloud. |
| [barman-cloud](https://github.com/cloudnative-pg/barman-cloud) | Go library for interacting with Barman Cloud object stores, wrapped by `plugin-barman-cloud` and still used by the operator's native backup support. |
| [klio](https://github.com/cloudnative-pg/klio) | Multi-Tiered Backup and Recovery Plugin for CloudNativePG. |
| [cnpg-i-hello-world](https://github.com/cloudnative-pg/cnpg-i-hello-world) | A simplified template/example for building new plugins. |

## External Dependencies

Forks of external upstream projects that a component above depends on.
Not CloudNativePG-authored code, so it doesn't follow the same ownership
model as the rest of this file (see the note below).

| Repository | Description |
| --- | --- |
| [kopia](https://github.com/cloudnative-pg/kopia) | Fork of the upstream [kopia/kopia](https://github.com/kopia/kopia), the deduplication/backup engine `klio` depends on. |

> `kopia` is a fork of an external project, not a CloudNativePG-authored
> codebase: there's no ongoing feature review to gate with `CODEOWNERS`,
> just occasional pushes to keep it in sync with what `klio` needs. Its
> default branch is `klio`, not `main`.

## PostgreSQL Extensions & Tooling

Software that operates on or with PostgreSQL directly: compiled extensions
and modules, or standalone Postgres-native tools and utilities, independent
of Kubernetes and not delivered as a CNPG-I plugin.

| Repository | Description |
| --- | --- |
| [postgres-keycloak-oauth-validator](https://github.com/cloudnative-pg/postgres-keycloak-oauth-validator) | A PostgreSQL module for OAuth2/Keycloak token validation. |
