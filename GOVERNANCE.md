# CloudNativePG Governance

This document defines governance policies for the CloudNativePG project.

## Our Mission

*"Run PostgreSQL, the Kubernetes way."*

PostgreSQL is one of the most loved databases in the world, especially in
traditional VM and bare metal installations.

CloudNativePG was originally conceived by PostgreSQL experts and
Kubernetes administrators within [2ndQuadrant](https://www.2ndquadrant.com/) -
later acquired by [EDB](https://www.enterprisedb.com/) - with the goal to
increase the adoption of Postgres within Kubernetes environments.

## Values

Developing a PostgreSQL operator for Kubernetes requires the highest level of
technical quality for both PostgreSQL and Kubernetes.
The goal of CloudNativePG is to innovate in the data in Kubernetes space,
making it easier for organizations to build microservice applications that rely
on a PostgreSQL database directly inside Kubernetes.

We believe that an open source community is the most effective way to address
the complexity of the domain through teamwork, trust, merit, openness,
constructive dissent, diversity, commitment, and accountability.

CloudNativePG and its leadership embrace the following values:

* Technical excellence: Our mindset is to provide the best experience of
  PostgreSQL in Kubernetes, and this requires the highest skills in both
  technologies.

* Built-in Quality and Security: Automated testing is a way to improve
  the quality directly in the product, avoiding manual inspection (citing
  Dr. Deming). Similarly, security must be part of the development process.

* Openness: Communication and decision-making happen in the open and are
  discoverable for future reference. As much as possible, all discussions
  and work take place in public forums and open repositories. Dissent, if
  constructive and expressed with respect and manners, is encouraged as it
  is seen as an innovation enabler.

* Fairness: All stakeholders have the opportunity to provide feedback and submit
  contributions, which will be considered on their merits.

* Community over Product or Company: Sustaining and growing our community takes
  priority over shipping code or sponsors' organizational goals. Each
  contributor participates in the project as an individual.

* Inclusivity: We innovate through different perspectives and skill sets, which
  can only be accomplished in a welcoming and respectful environment.

* Participation: Responsibilities within the project are earned through
  participation, and there is a clear path up the contributor ladder into leadership
  positions.

## Project Roles

### Maintainers

Maintainers hold a crucial role in the comprehensive development of the entire
CloudNativePG project and its associated components. This privilege is granted
with some expectation of responsibility: maintainers are people who care about
the CloudNativePG project and want to help it grow and improve. A maintainer is
not just someone who can make changes, but someone who has demonstrated their
ability to collaborate with the team, get the most knowledgeable people to
review code, contribute high-quality code, and follow through to fix issues (in
code or tests).

A maintainer is a contributor to the CloudNativePG project's success and a
citizen helping the project succeed.

The maintainers are identified in the [`MAINTAINERS`](MAINTAINERS) file.

#### Changes in Maintainership

New maintainers are proposed by an existing maintainer and are elected by a ⅔
majority maintainers vote. Maintainers can be removed by a ⅔ majority
maintainers vote, leading to their transition to emeritus status.

#### Github Project Administration

Members designated as Maintainers will be included in the `maintainers` team,
where they will possess the `Maintain` role for every CloudNativePG repository.
Those Maintainers who are interested in assuming administrative
responsibilities for the organization's repositories can be appointed to the
`admins` team at any point, granting them the `Admin` role across all
repositories.

### Component owners

The component owners are tasked with the development of specific subprojects or
components within CloudNativePG. These components may be represented either by
a separate GitHub repository within the CloudNativePG organization (e.g.,
`postgres-containers`) or by a subdirectory in a GitHub repository (e.g.,
`./docs/` in `cloudnativepg`).

The owners of these components are delineated in the
[`COMPONENT-OWNERS`](COMPONENT-OWNERS) file within this repository, which also
specifies the component for which each individual is responsible.

#### Changes in component ownership

New component owners can be proposed by any maintainer and are elected by a ⅔
majority maintainers vote. Component owners can be removed by a ⅔ majority
maintainers vote.

#### Github Project Administration

Owners of components with dedicated GitHub repositories will be granted `Write`
access to their respective repositories, enabling them to merge approved pull
requests. Additionally, component owners will be incorporated into the
repository's `CODEOWNERS` file, ensuring clear attribution and accountability
for code contributions.

It's important to note that these owners will not receive `Maintain` or `Admin`
privileges for any CloudNativePG GitHub repositories."

## Meetings

Time zones permitting, Maintainers are expected to participate in the public
developers meeting (see ["Meetings" in the contributing guidelines](CONTRIBUTING.md#meetings)
page for details).

Maintainers will also have closed meetings to discuss security reports
or Code of Conduct violations. Such meetings should be scheduled by any
Maintainer on receipt of a security issue or CoC report. All current Maintainers
must be invited to such closed meetings, except for any Maintainer accused of a CoC violation.

## CNCF Resources

Any Maintainer may suggest a request for CNCF resources by creating a new
[Github discussion under the "Maintainers room" category](https://github.com/cloudnative-pg/cloudnative-pg/discussions/categories/maintainers-room),
or during a meeting.  A simple majority of Maintainers approves the request.
The Maintainers may also choose to delegate working with the CNCF to
non-Maintainer community members.

## Code of Conduct

[Code of Conduct](./code-of-conduct.md)
violations by community members will be discussed and resolved
on the [private Maintainer mailing list](mailto:conduct@cloudnative-pg.io).
If the reported CoC violator is a Maintainer, the Maintainers will instead
designate two Maintainers to work with CNCF staff in resolving the report.

## Voting

While most business in CloudNativePG is conducted by "lazy consensus",
periodically, the Maintainers may need to vote on specific actions or changes.
A vote can be taken in [a new Github discussion under the "Maintainers room" category](https://github.com/cloudnative-pg/cloudnative-pg/discussions/categories/maintainers-room),
or on [the private Maintainer mailing list](mailto:security@cloudnative-pg.io) for
security or conduct matters. Votes may also be taken during developer meetings.
Any Maintainer may demand a vote be taken.

Most votes require a simple majority of all Maintainers to succeed, and changes
to this Governance require a 2/3 vote of all Maintainers.
