# Contributing to CloudNativePG

Welcome! We are glad that you want to contribute to the CloudNativePG project! 💖

The guidelines below are a starting point for all
[repositories under the CloudNativePG organization](README.md#repositories).

## Code of Conduct

CloudNativePG is a community-driven project. While many maintainers are
sponsored by their respective employers, they operate here on a voluntary
basis. Before contributing, please review our core policies:

- **[Code of Conduct](CODE_OF_CONDUCT.md)**: Our standards for a welcoming
  community.
- **[AI Policy](AI_POLICY.md)**: Guidelines regarding the use of Generative AI
  in contributions.

> [!IMPORTANT]
> **We are all human beings with finite time and a limited amount of cognitive
> load we can sustain at any given moment.** Given the rapid growth and technical
> complexity of the project, maintainers must carefully balance planned roadmap
> items and critical maintenance (such as the current transition of Barman Cloud
> to plugins and moving from base-image extensions to self-contained ones).

## Community Meetings

We extend a warm welcome to everyone to join our meetings. For details, please
visit the [CloudNativePG Community](https://github.com/cloudnative-pg#cloudnativepg-community-meetings)
page.

## How to Contribute

We welcome many types of contributions including:

- Issue Triage
- Answering questions on [Slack or GitHub Discussions](https://github.com/cloudnative-pg#getting-in-touch)
- Advocacy at Events (let us know when your talk about CloudNativePG is accepted!)
- The [CloudNativePG website](https://github.com/cloudnative-pg/cloudnative-pg.github.io)
- Documentation:
    - [Sources](https://github.com/cloudnative-pg/cloudnative-pg/tree/main/docs)
    - [Website](https://github.com/cloudnative-pg/docs)
- New features and Bug fixes
- Builds, CI/CD, and Release management
- [Communications / Social Media](https://github.com/cloudnative-pg#getting-in-touch) / [Blog Posts](https://cloudnative-pg.io/blog/)

### Contributing to source code

To respect everyone's time, please follow these steps before submitting a Pull
Request:

1.  **Search First**: Before reporting a new issue, please check the
    documentation and ensure a similar issue has not been opened in the past.
2.  **Open an Issue**: Always start by opening a GitHub Issue to discuss your
    idea. Ensure maintainers have agreed on the approach and priority before you
    spend time writing code.
3.  **Fork and Branch**: Fork the relevant project. We recommend developing
    your feature in a branch named with the issue ID (e.g., `dev/43`).
4.  **Test**: Ensure you have tested your code locally according to the
    specific repository's instructions.
5.  **Experimental Path**: If your patch cannot wait or is highly experimental,
    remember that the [**CNPG-I interface**](https://cloudnative-pg.io/docs/devel/cnpg_i)
    provides the freedom to build and test features as plugins. Once a feature
    is proven and well-received by the community, we can discuss moving it into the
    core.

If you are reporting a vulnerability, please refer to the
[Security Policy](https://github.com/cloudnative-pg/cloudnative-pg/blob/main/SECURITY.md).

> [!IMPORTANT]
> **External Contributors:** If you're contributing to the CloudNativePG
> operator from outside the core team, please note that some
> repository-specific instructions (such as those in the operator's detailed
> development docs) apply only to maintainers. See the
> [development contribution guide](https://github.com/cloudnative-pg/cloudnative-pg/blob/main/contribute/README.md)
> for complete details.

