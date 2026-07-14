# Security Policy

The AReaL maintainers take the security of the project and its users seriously. We
appreciate responsible disclosure of vulnerabilities and will work with reporters to
investigate and remediate issues promptly.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues,
discussions, or pull requests.**

To report a vulnerability, use one of the following private channels:

1. **GitHub private advisory (preferred).** Navigate to the **Security** tab of the
   affected repository (for example
   [areal-project/AReaL](https://github.com/areal-project/AReaL/security/advisories)),
   open **Advisories**, and click **Report a vulnerability**.
1. **Email.** If you cannot use GitHub advisories, send an email to the
   [Security Team](roles/Security-Team.md) at **<areal-security@googlegroups.com>**.
   Encrypt sensitive details if possible.

When reporting, please include:

- A clear description of the vulnerability and its potential impact.
- Steps to reproduce, including affected versions, commits, or configurations.
- Any proof-of-concept code or logs, if available.
- Suggested mitigations, if you have them.

You can expect an acknowledgement within **3 business days**. If you do not hear back
within that window, please follow up via the same channel or contact another maintainer
listed in [roles/Maintainers.md](roles/Maintainers.md).

## Disclosure process

After a report is received, the maintainers will:

1. Confirm receipt and begin triage.
1. Reproduce and assess the impact of the issue.
1. Develop and validate a fix in a private branch or draft advisory.
1. Coordinate a release and a public advisory with the reporter.
1. Publicly disclose the issue after a fix is available, crediting the reporter unless
   they request otherwise.

We aim to resolve confirmed vulnerabilities and publish an advisory within **90 days**
of the initial report. Embargo periods may be adjusted based on severity, complexity,
and coordination with affected downstream users.

## Supported versions

Security fixes are typically applied to the **latest released minor version** on the
`main` branch of [areal-project/AReaL](https://github.com/areal-project/AReaL). Older
versions may receive fixes on a best-effort basis. See the
[releases page](https://github.com/areal-project/AReaL/releases) for the current
supported version.

## Scope

This policy covers all repositories owned by the
[`areal-project`](https://github.com/areal-project) GitHub organization. Vulnerabilities
in third-party dependencies should be reported upstream; you may still notify us so we
can track and pull in fixes.

## Safe harbor

We will not pursue legal action against researchers who, in good faith:

- Make every effort to avoid privacy violations, service disruption, and data
  destruction during their research.
- Only interact with their own accounts and test environments.
- Give us reasonable time to respond and remediate before any public disclosure.

Thank you for helping keep AReaL and its users safe.
