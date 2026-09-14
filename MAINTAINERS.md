# CloudNativePG Maintainers

This file records the committees: the Steering Committee, the
Infrastructure Team and Security Response Team it delegates to, and each
subproject's maintainer committee. The section a person appears under is
their domain of responsibility. Component Owners and Contributors are
recorded per component, in that repository's own `COMPONENT_OWNERS.md`
and `CONTRIBUTORS.md` (see
[CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md)), not here.

**Contact.** Security reports go to
[security@cloudnative-pg.io](mailto:security@cloudnative-pg.io) and Code
of Conduct reports to
[conduct@cloudnative-pg.io](mailto:conduct@cloudnative-pg.io), never to an
individual. For anything else, each committee has a channel listed in
[subprojects/README.md](subprojects/README.md#communication-channels), and
every person below is reachable on GitHub at the handle given. Individual
email addresses for security purposes are recorded in
[SECURITY-INSIGHTS.yml](SECURITY-INSIGHTS.yml).

Every subproject has a committee, of at least three members (see
[GOVERNANCE.md's Changes in subproject maintainer committee
membership](GOVERNANCE.md#changes-in-subproject-maintainer-committee-membership)).
All four are seeded with the same five people, the CloudNativePG
Maintainers as they stood before this restructuring, because that is who
held the authority being divided up. That is the starting point, not the
intended end state: each committee is self-selecting from the established
Component Owners of its own subproject's repositories, and the four are
expected to diverge as those people are promoted into them. Two changes
still to come are tracked publicly:
[#68](https://github.com/cloudnative-pg/governance/issues/68) for
org-balanced voting and the Steering seat mechanism, and
[#69](https://github.com/cloudnative-pg/governance/issues/69).

## Steering Committee

Per [GOVERNANCE.md's Steering Committee section](GOVERNANCE.md#steering-committee),
the Steering Committee is the group of CloudNativePG Maintainers, carried
forward unchanged from before this restructuring:

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Infrastructure Team

Per [GOVERNANCE.md's Infrastructure Administration section](GOVERNANCE.md#infrastructure-administration),
the Infrastructure Team is a distinct body from the Steering Committee,
even though today's membership happens to be identical. It's the existing
`admins` GitHub team:

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Security Response Team

Per [GOVERNANCE.md's Security Response Team section](GOVERNANCE.md#security-response-team),
this is the group that triages what arrives at the intake address and
routes it. Today it is the Steering Committee acting in that capacity, a
distinct role from its governance authority:

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Core Maintainers

Technical authority over every component listed in
[subprojects/core.md](subprojects/core.md):

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Supply Chain Maintainers

Technical authority over every component listed in
[subprojects/supply-chain.md](subprojects/supply-chain.md):

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Community, Docs & Ecosystem Maintainers

Technical authority over every component listed in
[subprojects/community-ecosystem.md](subprojects/community-ecosystem.md):

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

## Extensibility Maintainers

Technical authority over every component listed in
[subprojects/extensibility.md](subprojects/extensibility.md):

| Last Name | First Name | Handle | Organization |
| --- | --- | --- | --- |
| Bartolini | Gabriele | @gbartolini | EDB |
| Canovai | Francesco | @fcanovai | EDB |
| Cecchi | Leonardo | @leonardoce | EDB |
| Nenciarini | Marco | @mnencia | EDB |
| Ruocco | Armando | @armru | EDB |

Changes to a subproject's committee membership follow the
self-selection process in
[GOVERNANCE.md's Voting section](GOVERNANCE.md#voting) and are recorded
directly in the sections above; they do not require editing GOVERNANCE.md
itself. The org-control repositories, enumerated in
[GOVERNANCE.md's Subprojects section](GOVERNANCE.md#subprojects), sit
outside this file entirely: they are administered directly by the Steering
Committee, not by a subproject maintainer committee.

Every Organization cell above states the employer on that person's
registered Linux Foundation ID (LFID). Everyone listed holds one;
`.project`'s `maintainers.yaml` does not record employers yet, which is a
follow-up rather than a blocker to ratifying this roster. A change of
employer is updated here within 30 days, per
[CONTRIBUTOR_LADDER.md's Recording a Role Change](CONTRIBUTOR_LADDER.md#recording-a-role-change);
"Independent" is written out in full for someone with no employer tied to
their contribution, so an empty cell always means missing data rather
than no affiliation.

## Emeritus Maintainers

The following individuals have previously served as maintainers and are
recognised for their valuable contributions to the project:

- Jonathan Gonzalez (EDB)
- Philippe Scorsolini (Upbound)
