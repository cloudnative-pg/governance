# CloudNativePG Subprojects

> [!NOTE]
> The subproject structure and its four committees are adopted per
> [GOVERNANCE.md](../GOVERNANCE.md); what is still rolling out is the
> repository access behind them (see the note under
> [GitHub Teams](#github-teams) below). The repository listings themselves
> reflect which repositories exist in each subproject; who owns them is
> recorded in [MAINTAINERS.md](../MAINTAINERS.md) and in each component's
> own `COMPONENT_OWNERS.md`, not here.

This is the index of CloudNativePG's four subprojects and their components.
Each subproject has its own file, listing every repository that falls under
it with a short description. Subprojects themselves, and the access/voting
rights each role carries, are defined in
[GOVERNANCE.md's Subprojects section](../GOVERNANCE.md#subprojects), not
here. Who owns what is recorded in two places, neither of them this
folder: [MAINTAINERS.md](../MAINTAINERS.md) lists each subproject's
maintainer committee, and each component's own `COMPONENT_OWNERS.md`
lists that repository's Component Owners, generated from
[`cnpg-infra`](https://github.com/cloudnative-pg/cnpg-infra)'s
`repo-tiers.yaml` alongside the `<repo>-owners` team that grants them
access. The Contributor tier is recorded the same way, in each
repository's own `CONTRIBUTORS.md`, and only where a repository has any.

- [Core](core.md)
- [Supply Chain](supply-chain.md)
- [Community, Docs & Ecosystem](community-ecosystem.md)
- [Extensibility](extensibility.md)

Two things apply to every file above, stated once here rather than repeated
in each: every repository in each file is already owned by that subproject's
own maintainer committee, via the corresponding [GitHub Team](#github-teams),
with any additional named Component Owner recorded in that repository's
own `COMPONENT_OWNERS.md` as above, not here. Path-scoped `CODEOWNERS` review-routing (a Component Owner
tagging a Contributor for review purposes, an operational choice that
carries no vote and no CNPG Organization Member status; see
[CONTRIBUTOR_LADDER.md's Component Owner section](../CONTRIBUTOR_LADDER.md#component-owner))
is tracked at full fidelity in
[`cnpg-infra`'s `componentowners-policy.yaml`](https://github.com/cloudnative-pg/cnpg-infra/blob/main/componentowners-policy.yaml)
instead.

The `governance`, `.project`, `.github`, `cnpg-infra`, and `cnpg-template`
repositories are not listed in any of these: none is part of any
subproject; see [README.md's Governance section](../README.md#governance).
`cnpg-infra` holds the org's admin tooling (repo settings, teams,
CODEOWNERS); `cnpg-template` is the template every new repository in the
org, including the other org-control repositories, is created from. Both
are Steering/CNCF-owned infrastructure for the org itself, same as the
other three, not a subproject deliverable. `cnpg-template` was previously
listed under Supply Chain in [supply-chain.md](supply-chain.md); that was
a discrepancy against `cnpg-infra`'s real, current classification, fixed
here as a routine editorial move rather than something requiring a vote
(see [GOVERNANCE.md's Subprojects section](../GOVERNANCE.md#subprojects)).

Which changes to these files need a governance vote and which are routine
editorial work is defined in
[GOVERNANCE.md's Subprojects section](../GOVERNANCE.md#subprojects), not
restated here. Each `subprojects/*.md` file, other than this index, is scoped in
`CODEOWNERS` to its own subproject's maintainer committee team (see
[CODEOWNERS](../CODEOWNERS)), so that a subproject can eventually update
its own component listing without needing sign-off from the others. Each
of those lines also carries `@cloudnative-pg/governance-owners`, this
repo's own owners team, so review routing works while all four committees
still hold the same five people. This index itself stays on the `@cloudnative-pg/governance-owners`
fallback permanently, since it isn't owned by any single subproject.

## GitHub Teams

Why a GitHub Team can never be the public record of who holds authority,
and why [MAINTAINERS.md](../MAINTAINERS.md) is, is covered in
[GOVERNANCE.md's GitHub Teams and Communication Channels section](../GOVERNANCE.md#github-teams-and-communication-channels).
This section is the operational half of that: the team names themselves.
All GitHub teams and repository permissions across the organization,
including every team listed below, are managed declaratively through the
[`cnpg-infra`](https://github.com/cloudnative-pg/cnpg-infra) repository's
scripts and config files, not created or edited by hand on GitHub. Names
are fixed below so nobody invents an ad hoc team when a repo is created or
a subproject rolls out.

| Team (GitHub slug) | Grants | Access |
| :---- | :---- | :---- |
| `<repo>-owners` (existing, per repository, e.g. `governance-owners`) | That repository's real `CODEOWNERS` owners, managed via `cnpg-infra` | Repository-scoped, per `cnpg-infra`'s `repo-tiers.yaml` |
| `admins` (existing) | Infrastructure Team, delegated by Steering (see [GOVERNANCE.md's Infrastructure Administration section](../GOVERNANCE.md#infrastructure-administration)) | `Admin` on every repository |
| `steering-committee` | Steering Committee | No repo access of its own; Admin on the org-control repos already comes from `admins` above. Its role is being the electorate for Steering-scoped [`.gitvote.yml`](../.gitvote.yml) profiles (`default`, `governance`) |
| `core-maintainers` | Core committee | `Write` on this repo, so its `CODEOWNERS` line is honored; `Maintain` on the [Core](core.md) repositories is the target, not yet granted |
| `supply-chain-maintainers` | Supply Chain committee | `Write` on this repo, so its `CODEOWNERS` line is honored; `Maintain` on the [Supply Chain](supply-chain.md) repositories is the target, not yet granted |
| `community-ecosystem-maintainers` | Community, Docs & Ecosystem committee | `Write` on this repo, so its `CODEOWNERS` line is honored; `Maintain` on the [Community, Docs & Ecosystem](community-ecosystem.md) repositories is the target, not yet granted |
| `extensibility-maintainers` | Extensibility committee | `Write` on this repo, so its `CODEOWNERS` line is honored; `Maintain` on the [Extensibility](extensibility.md) repositories is the target, not yet granted |

Team membership must mirror the rosters in MAINTAINERS.md; when a roster
changes, that change is made in `cnpg-infra`'s config and applied from
there, not by editing a team's membership directly on GitHub. Set new
teams to "Visible" within the organization for internal clarity; this does
not make membership public, it only helps other maintainers and component
owners see who's on which team.

> [!IMPORTANT]
> **Transitional, to be removed once rollout completes:** the org-wide
> `maintainers` team has already been deleted (superseded by the per-repo
> `<repo>-owners` teams above, which `cnpg-infra` already provisions and
> syncs today via `scripts/sync-project-owner-teams.sh` and
> `repo-tiers.yaml`'s `owners:` field). Subproject-committee teams
> (`core-maintainers` and the other three) are a separate, coarser-grained
> concept layered on top of that per-repo one. All four exist on GitHub and
> match the rosters in [MAINTAINERS.md](../MAINTAINERS.md), tracked in
> `cnpg-infra/org-policy.yaml`'s `subproject_committees` section and edited
> by hand rather than auto-synced, so a roster change needs the GitHub team
> reconciled in the same pass. What is still outstanding is repository
> access: each team is granted `write` on this repo (`cnpg-infra`'s
> `repo-policy.yaml`), without which GitHub ignores its `CODEOWNERS` lines
> entirely, but the `Maintain` grant on each subproject's own repositories
> in the table above is not in place yet.

## Communication Channels

Slack channel names are the corresponding GitHub team name above, prefixed
with `cloudnativepg-` (e.g. `core-maintainers` the team,
`cloudnativepg-core-maintainers` the channel), so a GitHub team and its
Slack channel map onto each other without guessing.

| Channel | Maps to |
| :---- | :---- |
| `cloudnativepg-core-maintainers` (renamed from `cloudnativepg-maintainers`) | Core committee |
| `cloudnativepg-supply-chain-maintainers` | Supply Chain committee |
| `cloudnativepg-community-ecosystem-maintainers` | Community, Docs & Ecosystem committee |
| `cloudnativepg-extensibility-maintainers` | Extensibility committee |
| `cloudnativepg-steering-committee` | Steering Committee (security response and CoC ratification are discussed here) |

All of these channels are private, so channel membership is no more visible
to the public than a GitHub Team is. MAINTAINERS.md stays the document of
record for who holds authority; these channels are operational plumbing that
must mirror it, not an alternative way to find out who's on a committee.
