# AReaL Contributor Ladder

This document outlines the different contributor roles and responsibilities within the
AReaL project. Think of it as a guide to help you understand your role, what is expected
of you, and how you can grow with us in the community.

- [Goals](#goals)
- [Scope](#scope)
- [General Guidelines](#general-guidelines)
  - [Everyone is Welcome](#everyone-is-welcome)
  - [Guidance](#guidance)
  - [Continued Contributions](#continued-contributions)
  - [Consensus for Merging](#consensus-for-merging)
  - [Starting the Conversation](#starting-the-conversation)
- [Contributor Ladder](#contributor-ladder)
  - [Contributor](#contributor)
  - [Member](#member)
  - [Approver](#approver)
  - [Maintainer](#maintainer)

## Goals

We have put this document together with a few key goals in mind:

- To ensure the long-term health and sustainability of the AReaL community.
- To encourage new contributors to get more involved and take on formal roles.
- To provide a clear path for those looking to grow into leadership positions.
- To build a strong pipeline of future leaders for the project.

## Scope

This guide covers the roles and responsibilities for everyone who contributes to the
AReaL open-source project and its repositories. Whether you are writing training code,
improving documentation, adding examples, creating tests, or helping in other ways, this
is for you.

## General Guidelines

### Everyone is Welcome

We truly appreciate every contribution. You do not need a formal title to create or
review pull requests, help with issues, or join discussions. Taking on a formal role is
completely optional, so feel free to contribute in any way that works for you.

### Guidance

As described in our [Contributing Guide](CONTRIBUTING.md), we welcome all kinds of
contributions, whether it is pull requests, issues, or new feature ideas. If you are new
here, we recommend starting with smaller, meaningful changes. They are easier to review
and a great way to get familiar with our processes and our [roadmap](ROADMAP.md).

Because AReaL is an open-source project, review times can vary depending on when
Maintainers and Approvers are available. You can build trust and speed up your
progression by making consistent, smaller contributions or by giving constructive
feedback on other people's work.

Every time we merge a contribution, we are committing to maintaining it for the long
haul. That is why larger changes require not just a lot of effort, but also a proven
track record so the community can trust that you will be around to support your changes.
For substantial features or refactoring, please open an issue or a draft pull request to
discuss the design with the maintainers before writing the code.

### Continued Contributions

If you are thinking about applying for one of the roles below, we hope it is because you
plan to stay active at that level. If life gets in the way and you can no longer keep up
with the responsibilities of your role, it is perfectly fine to step down. Members who
are inactive for an extended period may be moved to emeritus status and removed from the
AReaL GitHub organization, but you can always go through the process again when you are
ready. See
[Removing Inactive Members](COMMUNITY_MEMBERSHIP.md#removing-an-inactive-memberapprovermaintainer)
for details.

### Consensus for Merging

If you think a change might be controversial, please hold off on merging and give others
a chance to share their thoughts. Even if you have merge access, it does not mean you
should always use it. We want to avoid blocking pull requests indefinitely, but it is
important to make sure everyone's perspective is heard first.

### Starting the Conversation

If you are interested in moving up the ladder and taking on one of these roles, reach
out to an existing Approver or Maintainer in a
[GitHub Discussion](https://github.com/areal-project/AReaL/discussions) or at a
community meeting. We are here to help you get started.

## Contributor Ladder

Our ladder has four main roles: **Contributor**, **Member**, **Approver**, and
**Maintainer**. Contributors usually start at the first level and move up as they become
more involved and make a bigger impact. Each role comes with its own set of
responsibilities, qualifications, and privileges that reflect a contributor's level of
involvement and the trust they have earned in the community.

Here is a quick look at the roles:

<!-- markdownlint-disable -->

| Role            | Responsibilities                                                       | Qualifications                                                               | Privileges                                                               |
| --------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Contributor** | Follow our Code of Conduct & Contributing Guide                        | Anyone who participates in the community                                     | Can be assigned issues and request reviews                               |
| **Member**      | Contribute regularly and complete tasks you volunteer for              | A history of contributions over at least three months                        | Trigger CI/CD, review PRs, and recommend others for Member status        |
| **Approver**    | Review PRs in your area of expertise and maintain quality              | A Member with a solid track record of high-quality reviews                   | Approve PRs in specific areas and recommend others for Approver          |
| **Maintainer**  | Merge PRs, coordinate releases, and help shape the project's direction | Long-term contributions, leadership, and a deep understanding of the project | Merge code, represent the project publicly, and nominate new Maintainers |

<!-- markdownlint-restore -->

Each role is defined by three key things:

- **Responsibilities**: The tasks and duties we expect from you at this level.
- **Qualifications**: The criteria you need to meet to earn this role.
- **Privileges**: The rights and benefits you get as a contributor at this level.

As the project grows, these roles and responsibilities might evolve. The final say on
role assignments belongs to the project Maintainers, following the process in
[Community Membership](COMMUNITY_MEMBERSHIP.md).

### Contributor

A **Contributor** is anyone who adds value to the project. This can be through code, but
it does not have to be. This role is where most new or occasional contributors start.

- **Responsibilities**:

  - Follow the project's [Code of Conduct](CODE_OF_CONDUCT.md).
  - Stick to the [Contributing Guide](CONTRIBUTING.md).

- **Qualifications**:

  - Open to anyone who wants to be part of the community.
  - Contributions can include things like:
    - Joining community discussions.
    - Reporting bugs or giving feedback.
    - Testing new releases and sharing your experience.
    - Helping out with documentation, tutorials, or translations.
    - Attending or speaking at community events.
    - Submitting pull requests.
    - Helping other users or answering questions.
    - Spreading the word about the project.

- **Privileges**:

  - You can be assigned to issues and request reviews on your contributions.

This is the first step toward becoming a Member.

### Member

A **Member** is a consistent contributor who is actively involved in the project.
Members have more permissions in our repositories and are trusted to act in the
community's best interest.

- **Responsibilities**:

  - Make regular contributions to the project.
  - Finish any tasks or initiatives you volunteer for.
  - Continue to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

- **Qualifications**:

  - A history of successful contributions, including at least one of these:
    - Submitting or reviewing pull requests.
    - Fixing issues or bugs.
    - Making other impactful contributions.
  - You are actively contributing to an area of the project where Member privileges
    would be helpful.
  - A track record of contributing (code, reviews, discussions) for at least three
    months.
  - You consistently follow the project's Code of Conduct.

- **Privileges**:

  - You can trigger CI/CD pipelines (for example, by applying the `safe-to-test` label).
  - You can leave reviews and comments on pull requests.
  - You can triage issues and apply labels.
  - You can recommend other Contributors to become Members.
  - You can be nominated for higher roles as described in our governance.

The current Member list is maintained in [roles/Members.md](roles/Members.md).

### Approver

An **Approver** is a Member who takes ownership of a specific part of the project (such
as a training engine, an algorithm, the documentation, or the test suite). Approvers
play a key role in keeping our quality high by reviewing and approving changes in their
area.

- **Responsibilities**:

  - Handle all the responsibilities of a Member.
  - Regularly review pull requests in your area of expertise.
  - Make sure changes meet our coding standards, do not introduce regressions, and are
    good for the project.
  - Help triage issues in your area.
  - Help other contributors grow toward becoming Approvers.

- **Qualifications**:

  - You must already be a Member.
  - A proven track record of high-quality reviews and contributions.
  - Deep understanding of your specific area.
  - A commitment to maintaining responsibility for your designated area.
  - Supportive of new and occasional contributors, helping refine pull requests for
    merging.

- **Privileges**:

  - GitHub permissions to approve pull requests and manage labels in your areas.
  - You can recommend and review other Members for the Approver role.

The current Approver list is maintained in [roles/Approvers.md](roles/Approvers.md).

### Maintainer

A **Maintainer** is a highly trusted member of the project with the authority to merge
code, vote on project matters, and help guide the project's direction. This role is for
those who have shown a deep, sustained commitment to the community.

- **Responsibilities**:

  - Fulfill all the responsibilities of an Approver.
  - Merge pull requests to the main branch.
  - Maintain the codebase's overall quality, stability, and performance.
  - Coordinate releases and keep documentation up to date.
  - Shape the project's technical direction and [roadmap](ROADMAP.md).
  - Mentor new contributors and Maintainers.
  - Engage in strategic and policy discussions for the project.
  - Participate in voting on key project decisions as per the
    [governance rules](GOVERNANCE.md#decision-making).
  - Help enforce the [Code of Conduct](CODE_OF_CONDUCT.md) as a Community Moderator.
  - Review and approve promotions to the various roles within the project.

- **Qualifications**:

  - A history of long-term, high-quality contributions and leadership.
  - An in-depth understanding of the project's architecture and design.
  - Supportive of new contributors, aiding in refining their contributions.
  - Demonstrates independent judgment for the project's benefit, beyond personal or
    employer interests.
  - Actively mentors others in the community.
  - Additional requirements are detailed in
    [Community Membership](COMMUNITY_MEMBERSHIP.md#how-to-become-a-maintainer).

- **Privileges**:

  - You can merge code into the project repositories.
  - You can vote on project-level decisions.
  - You can represent the project in public.
  - You can nominate new Maintainers.

The current Maintainer list is maintained in
[roles/Maintainers.md](roles/Maintainers.md).
