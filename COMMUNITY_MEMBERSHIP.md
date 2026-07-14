# AReaL Community Membership

This document explains the responsibilities that come with the different contributor
roles in the AReaL community, and the concrete processes for joining, advancing, and
stepping down. For a full breakdown of the roles, responsibilities, and qualifications,
please also read the [Contributor Ladder](COMMUNITY_LADDER.md). For the project's
governing principles, see [GOVERNANCE.md](GOVERNANCE.md).

- [How We Make Decisions](#how-we-make-decisions)
  - [Solving Conflicts](#solving-conflicts)
  - [Handling Abstentions](#handling-abstentions)
- [Managing Membership](#managing-membership)
  - [How to Become a Member](#how-to-become-a-member)
  - [How to Become an Approver](#how-to-become-an-approver)
  - [How to Become a Maintainer](#how-to-become-a-maintainer)
  - [Removing an Inactive Member/Approver/Maintainer](#removing-an-inactive-memberapprovermaintainer)
  - [Voluntary Departure](#voluntary-departure)
- [Governance and Project Goal Changes](#governance-and-project-goal-changes)
- [Election Process](#election-process)
  - [Election Additional Remarks](#election-additional-remarks)
    - [Maximum Representation](#maximum-representation)
    - [Vacancies](#vacancies)
- [Worked Example: Adding a New Member](#worked-example-adding-a-new-member)

## How We Make Decisions

AReaL is an open-source project that thrives on transparency. Our repositories are the
single source of truth for everything — our values, designs, documentation, roadmap, and
interfaces.

In short, every decision is made by updating the project. Any change, big or small, that
impacts AReaL follows these simple steps:

1. Open an issue in the relevant repository to propose a change or raise a concern.
1. Discuss the issue in the comments.
1. Merge or close the issue based on community consensus.

For most issues (excluding those that add new Maintainers), an issue can be approved if:

- At least one active Maintainer comments "LGTM" (Looks Good To Me).
- No other Maintainer objects to the change.

For the purpose of this document, an **active Maintainer** is one who has participated
in community activities (such as reviewing pull requests, attending meetings, or
contributing to discussions) within the past three months.

For significant issues, we use a **lazy consensus period**: after an issue receives
initial approval, it is held for a set amount of time (typically seven days) to give
everyone a final chance to discuss it. If no one objects, it can be merged or closed. If
concerns are raised, we resolve them before moving forward.

### Solving Conflicts

In the rare event of a disagreement among Maintainers that cannot be resolved through
discussion, we use a voting process to reach a decision:

- Any Maintainer can call for a vote by creating a new issue in the relevant repository,
  outlining the conflict and the proposed options.
- All active Maintainers are notified and given a chance to vote.
- The outcome is determined by a simple majority (more than 50%) of the votes cast,
  unless a higher threshold is required elsewhere in this document.

### Handling Abstentions

If a Maintainer chooses to abstain from voting on a particular issue, their abstention
does not count toward the total number of votes cast. The decision is based solely on
the votes of those who actively participate.

## Managing Membership

Our Members (and Approvers and Maintainers) share responsibility for the project's
success. In general, they:

- Are accountable for the project's outcomes.
- Are invested in the long-term improvement of the project.
- Dedicate time to all the necessary tasks, not just the fun ones.

Members often work hard behind the scenes, and their efforts are not always visible.
While it is easy to get excited about new features, it is just as important — and often
more challenging — to handle bug fixes, small improvements, stability work, and all the
other foundational tasks that keep the project strong.

### How to Become a Member

Members start out as dedicated contributors who are committed to the long-term success
of the project. If you aspire to become a Member, you should be actively involved in
resolving issues, contributing code, and reviewing pull requests for at least three
months.

Membership is built on trust, and that goes beyond just writing code. You earn the trust
of the current Members by consistently acting in the best interest of the project.

New Members can self-nominate or be nominated by an existing Approver or Maintainer
(through a nomination issue) and need a simple majority vote from the current eligible
voters to be approved. See the [Election Process](#election-process) for details.

### How to Become an Approver

Building on the [Election Process](#election-process), the additional requirements are:

1. You must already be a Member.
1. Be nominated by an existing Approver or Maintainer. Self-nomination is not allowed;
   the nominator and the nominee must be different people.
1. Document your contribution history and explain why you are suitable for the role,
   listing the specific areas you want to be responsible for.
1. Approval must be given by a simple majority (more than 50%) of current Maintainers.

### How to Become a Maintainer

Building on the [Election Process](#election-process), the additional requirements are:

1. You must have been an Approver for at least three months.
1. Be nominated by an existing Maintainer. Self-nomination is not allowed; the nominator
   and the nominee must be different people.
1. Be approved by a supermajority vote (at least 65% of current Maintainers).

### Removing an Inactive Member/Approver/Maintainer

An existing Member, Approver, or Maintainer can be removed from the active list if they
are no longer meeting the expectations of the role. If a person meets one of the
following criteria, any other Member, Approver, or Maintainer may propose their removal
through a pull request:

- They have not participated in community activities (such as reviewing pull requests,
  attending meetings, contributing to discussions, or submitting code) for a period
  exceeding the following limits:
  - Maintainer: more than three months.
  - Approver: more than six months.
  - Member: more than twelve months.
- They have violated the governance rules more than twice, with documented evidence.

Once the conditions are confirmed, the person can be removed following the same voting
thresholds as their election. The affected individual has the right to appeal within 14
days by creating an issue in this community repository, which triggers a review by the
current Maintainers. If someone is removed, they are added to the emeritus section of
the relevant roles file to recognize their past contributions.

### Voluntary Departure

If a Member, Approver, or Maintainer wishes to voluntarily step down, they may do so at
any time by creating a departure issue in this community repository. In this case:

- Create a departure notice:
  - Open an issue using the [departure template](.github/ISSUE_TEMPLATE/departure.md).
  - Notify the community at least seven days before your last day.
  - Specify your exact departure date.
- Provide transition details:
  - Share handover information.
  - Explain any ongoing responsibilities.

The departure is publicly announced and remains visible for at least seven days. During
this period:

- No formal voting is required.
- The departing person should include any relevant handover information in their notice.
- Other Members acknowledge the departure with a thank-you message.
- The departing person is added to the emeritus section of the relevant roles file to
  honor their contributions.

After the departure date, the Maintainer team moves the person and their GitHub ID to
the emeritus section and removes them from the AReaL GitHub organization if necessary.
This process ensures a proper handover and recognition while giving the community
sufficient notice.

## Governance and Project Goal Changes

Significant changes to the governance structure or project direction require special
consideration to ensure community alignment.

This process applies to:

- **Governance document updates**: major revisions to the governance, membership, or
  ladder documents.
- **Decision-making changes**: modifications to voting thresholds or consensus
  mechanisms.
- **Role structure changes**: adding or modifying community roles or responsibilities.
- **Project goal changes**: updates to the mission, vision, or strategic direction.
- **Repository structure changes**: significant reorganization of project repositories.
- **Other major changes**: any other changes with substantial community impact.

The process is:

1. **Proposal**: Any Maintainer creates an issue with the `governance` label including:
   - A description of the proposed changes.
   - The rationale and expected benefits.
   - An impact analysis and migration plan, if applicable.
1. **Discussion**: The community discusses the proposal in the issue to gather feedback.
1. **Voting**: Maintainers vote. Major governance changes require a supermajority (at
   least 65%) of active Maintainers; minor clarifications may proceed by general
   agreement.
1. **Documentation**: A pull request updates the governance documents to reflect the
   change and references the related issue.
1. **Announcement**: The change is announced publicly and noted in the next community
   meeting.

## Election Process

Candidates in an election should explain their past contributions to the project and
community, as well as their future plans and intentions.

To become a **Member**, follow these steps:

1. A nomination issue is created using the
   [nomination template](.github/ISSUE_TEMPLATE/nominate.md) in this community
   repository. You may create it yourself, or ask an existing Approver or Maintainer to
   help. The Approver and Maintainer lists are in
   [roles/Approvers.md](roles/Approvers.md) and
   [roles/Maintainers.md](roles/Maintainers.md).
1. While the nomination issue is open, the community can discuss it in the comments.
1. The nomination issue remains open for seven days for discussion and feedback.
1. The nominee is encouraged to attend the next community meeting with a short
   self-introduction and a summary of their contributions.
1. If there are no objections from eligible voters during the discussion period, a
   Maintainer starts the voting process in the nomination issue.
1. The election is voted on by current Maintainers and Approvers, and a simple majority
   (more than 50%) is needed to pass.
1. If approved, a Maintainer creates a pull request to update
   [roles/Members.md](roles/Members.md). The PR must link to the nomination/voting issue
   and receive at least two "LGTM" reviews from existing Approvers or Maintainers.
1. Once merged, the Maintainer team adds the new Member to the AReaL GitHub
   organization.

The process is similar for becoming an Approver or Maintainer, with the additional
requirements described above. Unlike Member nominations, Approver and Maintainer
nominations cannot be self-nominations: each one must have a nominee who is different
from the nominator. Approver nominations must be made by an existing Approver or
Maintainer, and Maintainer nominations must be made by an existing Maintainer.

To ensure a fair and transparent process, AReaL uses the following parameters for each
role:

<!-- markdownlint-disable -->

| Role       | Nomination Period | Voting Period | Eligible Voters                   | Voting Requirement     |
| ---------- | ----------------- | ------------- | --------------------------------- | ---------------------- |
| Member     | 7 days            | 7 days        | Current Maintainers and Approvers | Simple majority (>50%) |
| Approver   | 7 days            | 14 days       | Current Maintainers only          | Simple majority (>50%) |
| Maintainer | 7 days            | 14 days       | Current Maintainers only          | Supermajority (≥65%)   |

<!-- markdownlint-restore -->

- **Nomination Period**: The nominator creates an issue that remains open for seven days
  to allow community discussion.
- **Voting Period**: After the discussion phase, the voting period begins. It must be
  started by a Maintainer and remain open for the duration shown above.
- **Voting Eligibility**: Member votes are open to current Maintainers and Approvers;
  Approver and Maintainer votes are open to current Maintainers only.
- **Results and Implementation**: Votes are counted and the outcome is documented in the
  nomination issue and the meeting summary. New role holders are added to the GitHub
  organization by the Maintainer team and recorded in the relevant [roles/](roles/)
  file.

### Election Additional Remarks

#### Maximum Representation

To ensure balanced representation, no more than half of the active Maintainers may be
from the same company or organization. If an election would exceed this limit, only the
top vote recipients up to the limit serve, and additional seats are filled by the next
highest vote recipients from other organizations.

If this limit is exceeded outside of an election, it is resolved as follows:

- **Standing excess** (an organization is already above the limit when this rule takes
  effect): no new Maintainer nominations from that organization are accepted until its
  share returns to at or below the limit through normal turnover.
- **Excess by attrition** (the departure of Maintainers from other organizations pushes
  one organization above the limit): a special election is triggered within 30 days to
  fill the vacated seats, giving priority to qualified candidates from other
  organizations until the limit is restored.

#### Vacancies

If an elected Maintainer leaves, the candidate with the next most votes from the
previous election may be offered the seat. If that is not possible, a special election
is held using the eligible voters from the most recent election.

## Worked Example: Adding a New Member

**Background**: Jane Doe has been contributing to AReaL for three months, consistently
submitting bug fixes, documentation improvements, and participating in community
discussions.

1. **Nomination**: Jane creates a nomination issue using the
   [nomination template](.github/ISSUE_TEMPLATE/nominate.md), or an existing Maintainer
   helps her create it.
1. **Community discussion**: The nomination issue stays open for seven days. Community
   members ask questions, and Jane responds about her commitment and future plans.
   Eligible voters (Maintainers and Approvers) can raise concerns.
1. **Voting initiation**: Jane gives a short self-introduction at the next community
   meeting. If there are no objections, a Maintainer starts the vote in the issue.
1. **Voting**: Eligible voters cast their votes over seven days using GitHub issue
   reactions (👍 yes, 👎 no, 👀 abstain). A simple majority of the votes cast is required.
1. **Results and onboarding**: The result is announced (for example, 5 yes / 1 no / 1
   abstain — passes). A Maintainer opens a pull request to update
   [roles/Members.md](roles/Members.md). Once merged, Jane is added to the AReaL GitHub
   organization with the appropriate permissions and welcomed in the next meeting
   summary.
