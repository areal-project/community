# AReaL Project Governance

Welcome to the AReaL project's governance guide. AReaL is a community-driven open-source
project, and we believe that open, transparent collaboration is the best way to build a
healthy, inclusive, and effective community. This document explains how the project is
run — our principles, roles, responsibilities, and the way we make decisions. We have
kept things as simple and practical as possible so that everyone can understand how to
get involved and how the project operates.

## Core Principles

- **Openness.** All of our communication and decision-making happens in the open.
  Discussions, proposals, and decisions are recorded in public issues, pull requests,
  and community meetings so anyone can follow along.
- **Inclusivity.** We are committed to a friendly and welcoming environment where people
  from all backgrounds and organizations can participate and feel included.
- **Neutrality.** AReaL is a community-driven project. Decisions are based on technical
  merit and community consensus, and are not controlled by any single company or
  individual.
- **Meritocracy.** Influence and responsibility are earned through sustained,
  high-quality contributions and constructive participation, not through title or
  affiliation.
- **Simplicity.** We keep our governance processes as lightweight as possible and avoid
  unnecessary bureaucracy.

## Scope

This governance document applies to the AReaL project and all repositories owned by the
[`areal-project`](https://github.com/areal-project) GitHub organization, including the
main [areal-project/AReaL](https://github.com/areal-project/AReaL) repository and this
community repository. The complete list of official repositories is maintained in
[REPOSITORIES.md](REPOSITORIES.md).

## Roles and Responsibilities

AReaL uses a contributor ladder with four roles: **Contributor**, **Member**,
**Approver**, and **Maintainer**. Each role carries its own responsibilities,
qualifications, and privileges that reflect a person's level of involvement and the
trust they have earned in the community.

| Role            | Summary                                                                         |
| --------------- | ------------------------------------------------------------------------------- |
| **Contributor** | Anyone who files issues, opens pull requests, or joins discussions.             |
| **Member**      | A consistent contributor trusted with triage and review permissions.            |
| **Approver**    | A Member who reviews and approves changes in a specific area of the project.    |
| **Maintainer**  | A trusted leader who merges code, votes on project matters, and sets direction. |

For a detailed description of each role — including responsibilities, qualifications,
and privileges — see the [AReaL Contributor Ladder](COMMUNITY_LADDER.md). The current
holders of each role are listed under [roles/](roles/).

There is no single "benevolent dictator" or lead maintainer with final authority over
the project. Authority is shared by the Maintainer team and exercised through the
decision-making process described below.

### Community Moderators

The [Code of Conduct](CODE_OF_CONDUCT.md) refers to "Community Moderators" as the people
responsible for enforcement. In this project, the Community Moderators are the current
Maintainers listed in [roles/Maintainers.md](roles/Maintainers.md).

## Decision-Making

AReaL's repositories are the single source of truth for the project — its code, designs,
documentation, roadmap, and policies. In practice, every decision is made by proposing a
change and reaching agreement on it in the open:

1. Open an issue (or pull request) in the relevant repository to propose a change or
   raise a concern.
1. Discuss it in the comments so that everyone has a chance to weigh in.
1. Merge or close it based on community consensus.

We strive to make decisions by **consensus** among the Maintainers whenever possible.
Consensus does not require unanimity; it means that concerns raised during discussion
have been heard and addressed, and no Maintainer actively objects.

### Lazy consensus

For most non-controversial changes we rely on *lazy consensus*: once a proposal has
received initial approval, it is held for a short review window (typically **7 days**)
so that everyone has a final chance to comment. If no Maintainer objects within that
period, the change is considered approved.

### Resolving conflicts by vote

If the Maintainers cannot reach consensus through discussion, any Maintainer may call
for a vote by opening (or labeling) an issue that describes the conflict and the
proposed options. All active Maintainers are notified and given a chance to vote. Unless
a higher threshold is specified elsewhere in this document, the outcome is decided by a
**simple majority (more than 50%)** of the votes cast. Abstentions do not count toward
the total.

An **active Maintainer** is one who has participated in community activities (such as
reviewing pull requests, attending meetings, or contributing to discussions) within the
past three months.

### Pull request approval policy

The following rules apply to code and documentation changes in the project's
repositories:

- All pull requests require approval from at least **two Maintainers (or Approvers in
  their area of ownership)** before they can be merged. At least one approval must come
  from a code owner of the modified paths (see
  [`.github/CODEOWNERS`](https://github.com/areal-project/AReaL/blob/main/.github/CODEOWNERS)).
- A Maintainer who holds the repository **administrator** role may merge trivial changes
  (typo fixes, documentation-only edits, or dependency bumps verified by CI) and
  time-sensitive hotfixes without the second approval. Such bypasses must still go
  through a pull request and must be disclosed in the PR description.
- The branch protection rules on `main` are documented in
  [`.github/ruleset.json`](https://github.com/areal-project/AReaL/blob/main/.github/ruleset.json)
  and are the source of truth for the mechanical enforcement of this policy.

## Membership and Elections

We use a structured membership system to recognize and empower active contributors. The
process for becoming (or stepping down from) a Member, Approver, or Maintainer — along
with the voting thresholds, election timelines, and inactivity rules — is documented in
[Community Membership](COMMUNITY_MEMBERSHIP.md) and the
[Contributor Ladder](COMMUNITY_LADDER.md).

## Rights and Responsibilities of Participants

Everyone who participates in the AReaL community has certain rights and
responsibilities.

**Your rights:**

- To participate in any public discussion, issue, or pull request.
- To be treated with respect and in accordance with the
  [Code of Conduct](CODE_OF_CONDUCT.md).
- To have your contributions reviewed and considered on their technical merit.
- To propose changes to the project, including to this governance document.
- To grow into formal roles through the [Contributor Ladder](COMMUNITY_LADDER.md).

**Your responsibilities:**

- Follow the [Code of Conduct](CODE_OF_CONDUCT.md) and the
  [Contributing Guide](CONTRIBUTING.md).
- Act in the long-term best interest of the project and its users.
- Communicate openly, kindly, and honestly, and assume good faith in others.
- Give and accept constructive feedback gracefully.
- Disclose relevant conflicts of interest when participating in decisions.

The additional responsibilities that come with each formal role are described in the
[Contributor Ladder](COMMUNITY_LADDER.md).

## Communication

AReaL's day-to-day collaboration happens in public. The main channels are:

- **GitHub Issues** — bug reports, feature requests, and proposals in the
  [main issue tracker](https://github.com/areal-project/AReaL/issues).
- **GitHub Discussions** — questions, ideas, and open-ended discussion in
  [AReaL Discussions](https://github.com/areal-project/AReaL/discussions).
- **Community meetings** — regular community calls. Agendas, slides, and recordings are
  indexed in [meeting/README.md](meeting/README.md).
- **Security reports** — see [SECURITY.md](SECURITY.md) for private disclosure channels.

A fuller list of channels is kept in the [README](README.md#community--communication).

## Code of Conduct

All participants are expected to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
Violations can be reported privately to at <areal-security@googlegroups.com> or to the
Community Moderators (the current Maintainers listed in
[roles/Maintainers.md](roles/Maintainers.md)).

## Feedback

We welcome feedback on the project and on how the community is run:

- For ideas and product feedback, open a
  [discussion](https://github.com/areal-project/AReaL/discussions) or a feature-request
  issue.
- For feedback on governance or community process, open an issue in this repository with
  the `governance` label, or raise it in a community meeting.

Maintainers aim to acknowledge governance and community feedback within a reasonable
time and to respond to it transparently.

## Security

Security is a priority for the project. If you discover a vulnerability, please follow
the responsible-disclosure process described in [SECURITY.md](SECURITY.md). Do not
report security issues through public issues, discussions, or pull requests.

## Legal and Compliance

AReaL follows widely adopted open-source governance practices, consistent with the
expectations the Linux Foundation sets for the projects it hosts:

- **Licensing.** AReaL is released under the [Apache License 2.0](LICENSE).
  Contributions are accepted under the same license on an "inbound = outbound" basis.
  See [Licensing of Contributions](CONTRIBUTING.md#licensing-of-contributions).
- **Developer Certificate of Origin (DCO).** Every commit must be signed off under the
  [DCO](https://developercertificate.org/) to certify the contributor's right to submit
  it. We use the DCO in place of a Contributor License Agreement (CLA). See
  [Sign Your Work](CONTRIBUTING.md#sign-your-work-developer-certificate-of-origin-dco).
- **Vendor neutrality and antitrust.** AReaL is governed for the benefit of the project
  and its users, not any single company. To preserve neutrality, no more than half of
  the active Maintainers may be affiliated with the same company or organization (see
  [Maximum Representation](COMMUNITY_MEMBERSHIP.md#maximum-representation)).
  Participants in community meetings and discussions are expected to comply with
  applicable antitrust and competition laws, and must not use community forums to
  coordinate on pricing, markets, or other anticompetitive matters.
- **Trademarks.** "AReaL" and associated names and logos are used to identify the
  project. Please do not use them in a way that implies endorsement or affiliation
  without permission. Nominative references (for example, "compatible with AReaL") are
  welcome.

## Amending this Document

Changes to this governance document follow the
[Governance Change Process](COMMUNITY_MEMBERSHIP.md#governance-and-project-goal-changes).
In short:

- **Major changes** (for example, to roles, voting thresholds, or decision-making rules)
  require a **supermajority vote of at least 65%** of the active Maintainers.
- **Minor changes** (clarifications, typo fixes, formatting) may be made by a Maintainer
  after reaching general agreement, via a normal pull request.
