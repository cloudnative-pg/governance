[![CloudNativePG](./logo/cloudnativepg.png)](https://cloudnative-pg.io/)

# CloudNativePG Governance

This repository contains the governance documents for the CloudNativePG
project:

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Governance Policy](./GOVERNANCE.md)
- [Contributing guidelines](./CONTRIBUTING.md)
- [AI Policy](./AI_POLICY.md)
- [List of Maintainers](./MAINTAINERS.md)
- [Contributor Ladder](./CONTRIBUTOR_LADDER.md)
- [Subprojects & Component Owners](./subprojects/README.md)
- [License](./LICENSE)

Component Owners and Contributors are listed per component, in each
repository's own `COMPONENT_OWNERS.md` and `CONTRIBUTORS.md`, next to the
people who vote on them, rather than in one org-wide list here.

## Table of Contents

- [Governance](#governance)
- [Repositories](#repositories)

## Governance

The `governance`, `.project`, `.github`, `cnpg-infra`, and `cnpg-template`
repositories are a special case: none is part of any subproject, and all
five are administered directly by the Steering Committee (see
[GOVERNANCE.md's GitHub Teams section](./GOVERNANCE.md#github-teams-and-communication-channels)),
not by a subproject maintainer committee.

| Repository | Description |
| --- | --- |
| [governance](https://github.com/cloudnative-pg/governance) | Central hub for project policies, AI policy, and general guidelines. |
| [.project](https://github.com/cloudnative-pg/.project) | The standard CNCF project metadata repository, enabling automation from CNCF infrastructure. |
| [.github](https://github.com/cloudnative-pg/.github) | GitHub's own org-wide default repository: profile page and default community health files (Code of Conduct, Contributing guide). |
| [cnpg-infra](https://github.com/cloudnative-pg/cnpg-infra) | Admin tooling that manages the org's GitHub settings, teams, and `CODEOWNERS` declaratively. |
| [cnpg-template](https://github.com/cloudnative-pg/cnpg-template) | The template every new org repository, including the other four above, is created from. |

## Repositories

CloudNativePG's repositories are grouped into four subprojects, defined in
[GOVERNANCE.md's Subprojects section](./GOVERNANCE.md#subprojects). The full
repository listing, descriptions, and component ownership are kept in the
[subprojects/](./subprojects/README.md) folder, one file per subproject, not
duplicated here.

- [Core](./subprojects/core.md)
- [Supply Chain](./subprojects/supply-chain.md)
- [Community, Docs & Ecosystem](./subprojects/community-ecosystem.md)
- [Extensibility](./subprojects/extensibility.md)
