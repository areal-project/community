# Contributing to AReaL

Thank you for your interest in contributing to AReaL! We welcome contributions from
everyone, whether you're fixing bugs, improving documentations, adding new features, or
helping with code reviews. This guide will help you get started.

Please review our [Code of Conduct](CODE_OF_CONDUCT.md) before participating and our
[Governance](GOVERNANCE.md) document to understand how the project is managed.

## Table of Contents

- [Quick Start](#quick-start)
- [Sign Your Work: Developer Certificate of Origin (DCO)](#sign-your-work-developer-certificate-of-origin-dco)
- [Licensing of Contributions](#licensing-of-contributions)
- [Tips for Using AI-Assisted Coding](#tips-for-using-ai-assisted-coding)
- [CI/CD](#cicd)

## Quick Start

1. **Fork and Clone:**

   ```bash
   # Fork the repository on GitHub, then:
   git clone https://github.com/YOUR-USERNAME/AReaL
   cd AReaL
   ```

1. **Install Development Dependencies:**

   Check our
   [installation guide](https://areal-project.github.io/AReaL/en/tutorial/installation.html)
   for detailed setup instructions.

1. **Set Up Pre-commit Hooks:**

   ```bash
   # Install hooks (includes formatting, linting, and commit message checks)
   pre-commit install --install-hooks
   # Subsequent commits will automatically check your files and commit messages.
   # Use -s to add the required Developer Certificate of Origin sign-off (see below):
   git commit -s -a -m 'feat(engine): my change'
   ```

1. **Find an Issue:**

   - Browse
     [good first issues](https://github.com/areal-project/AReaL/labels/good%20first%20issue)
   - Check [help wanted](https://github.com/areal-project/AReaL/labels/help%20wanted)
     issues
   - Or create a new issue using our
     [issue templates](https://github.com/areal-project/AReaL/issues/new/choose)

1. **Make Your Changes:**

   - Create a branch: `git checkout -b your-feature-name`
   - Make your changes with proper formatting
   - Test your changes following the next step

1. **Test Your Changes:**

   ```bash
   # --sw: step-wise debugging
   # --lf: run the last failed test first
   pytest -sv --sw --lf tests/
   ```

   Our test suite includes:

   - Running all examples to ensure they can execute one RL step
   - Checking individual engine functionalities, including rollout, forward-backward,
     and weight updates
   - Verifying numerical consistency of our packed data format with HuggingFace padded
     input, with and without Ulysses
   - Testing staleness management functionality
   - Ensuring GSM8K SFT loss decreases and RL rewards increase
   - Running other unit tests for individual components

   Some unit tests require multiple GPUs. The entry point scripts are located under
   `tests/torchrun`. In the corresponding test files (e.g.,
   `test_data_redistribution.py`), we use subprocesses to launch distributed experiments
   with `torchrun` and wait for results.

   If you have modified documentation, prepare doc in English and Chinese (use
   [/translate-doc-zh](../en/reference/ai_assisted_dev.md#commands) if needed), then
   build the docs and preview locally:

   ```bash
   ./docs/build_all.sh
   ```

1. **Submit a Pull Request**

We suggest applying our provided agent harness command `/create-pr` whenever possible.
Use that in `claude`, `opencode`, or any other coding agent CLI.

**IMPORTANT**: For new features and code refactoring, please submit a corresponding
issue or open a draft PR to discuss with the core developers before making any code
changes. Directly opening a PR that conflicts with our future [roadmap](ROADMAP.md) may
waste your effort.

## Sign Your Work: Developer Certificate of Origin (DCO)

Following common open-source and Linux Foundation practice, AReaL requires every commit
to be **signed off** under the
[Developer Certificate of Origin (DCO)](https://developercertificate.org/), version 1.1.
The DCO is a lightweight way for contributors to certify that they wrote the
contribution, or otherwise have the right to submit it under the project's open-source
license. We use the DCO instead of a Contributor License Agreement (CLA).

To sign off, add a `Signed-off-by` line to each commit message using your real name and
an email address you can be reached at:

```text
Signed-off-by: Jane Doe <jane.doe@example.com>
```

Git can add this line for you automatically with the `-s` (or `--signoff`) flag:

```bash
git commit -s -m 'feat(engine): my change'
```

If you forget to sign off, you can amend the most recent commit:

```bash
git commit --amend -s --no-edit
```

or sign off a range of earlier commits with an interactive rebase:

```bash
git rebase --signoff HEAD~<number-of-commits>
```

Pull requests whose commits are not signed off cannot be merged. By signing off, you
make the certification reproduced below.

<details>
<summary>Developer Certificate of Origin 1.1</summary>

```text
By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

</details>

## Licensing of Contributions

AReaL is released under the [Apache License 2.0](LICENSE). Unless explicitly stated
otherwise, all contributions you submit are accepted under the same license on an
"inbound = outbound" basis: the terms under which you contribute are the same terms
under which the project is distributed. Do not submit code, documentation, datasets, or
other material that you are not authorized to contribute under this license, and
properly credit any third-party sources as required by the
[Code of Conduct](CODE_OF_CONDUCT.md).

## Tips for Using AI-Assisted Coding

See the full
[AI-Assisted Development Guide](https://areal-project.github.io/AReaL/en/reference/ai_assisted_dev.html)
for detailed documentation.

## CI/CD

### Pre-commit Checks

Pre-commit checks run automatically on every PR. CI executes
`pre-commit run --all-files` to verify formatting (Ruff, clang-format, mdformat) and
linting. Commit messages are also validated against
[Conventional Commits](https://www.conventionalcommits.org/) format (e.g., `feat: ...`,
`fix: ...`, `docs: ...`, `gov: ...`).

As long as you have `pre-commit install --install-hooks` set up locally, your code will
be checked before each commit and your commit messages will be validated automatically.

### Tests

Tests for PRs are triggered when the PR is manually tagged with `safe-to-test`. The test
suite runs on ephemeral GCP compute engines with 2 A100 GPUs (40GB memory).

> **IMPORTANT:** To re-run tests, **DO NOT** click the "Re-run workflow" button on
> GitHub. Instead, remove the `safe-to-test` tag and then add it back.

**Writing Tests for New Features:**

If you have implemented a new feature, we highly recommend writing tests and adding them
to our pytest workflow. Place your test files under `tests/test_*.py` and mark them with
our pre-defined pytest markers:

- `slow`: Tests that take more than 30 seconds to run. These will not run in the CI/CD
  workflow unless also marked with `ci`.
- `ci`: Tests that should run in the CI/CD workflow (only needed for `slow` tests).
- `gpu`: Tests that use a single GPU.
- `multi_gpu`: Tests that use more than one GPU.

Our CI/CD runs tests selected by `pytest -m "not slow or ci"`. Since our CI machines
only have two GPUs, please skip tests that require more than 2 GPUs to prevent CI
failures. For example:

```python
import pytest
from areal.infra.platforms import current_platform

# ordinary tests are supposed to run fast, and will run in CI
def test_fast_operation():
    ...

# slow operations that will NOT run in CI
@pytest.mark.slow
def test_slow_operation():
    ...

# slow operations BUT must be tested in CI
@pytest.mark.slow
@pytest.mark.ci
def test_slow_operation():
    ...

# skip tests for more than 2 GPUs
@pytest.mark.skipif(current_platform.device_count() < 4, reason="This test requires 4 GPUs")
def test_some_multi_gpu_functionality():
    ...
```

### Image Building

The image building workflow can be triggered manually from any branch by users with
write permissions to the repository.

**Triggering the Workflow:**

You can trigger the workflow from any branch using either method:

1. **Via GitHub UI:**

   - Go to **Actions** → **"Build and Test Docker Image"**
   - Click **"Run workflow"** dropdown
   - Select the branch you want to build from
   - Click **"Run workflow"**

1. **Via GitHub CLI:**

   ```bash
   # Build from main
   gh workflow run build-docker-image.yml --ref main

   # Build from a feature branch
   gh workflow run build-docker-image.yml --ref feature/my-changes

   # Build from current branch
   gh workflow run build-docker-image.yml --ref $(git branch --show-current)
   ```

**Pipeline Stages:**

The workflow executes the following stages sequentially:

1. **Build**: Builds the Docker image and pushes it with `:test` tag
1. **Test**: Automatically runs the full test suite using the `:test` image
1. **Promote**: If tests pass, promotes the image by retagging `:test` → `:dev`
1. **Cleanup**: Always deletes the `:test` image from the registry (success or failure)

Building the image from scratch takes approximately 1-2 hours, plus additional time for
running the test suite.

**Normal PR Testing:**

The PR-based test workflow (triggered by the `safe-to-test` label) remains unchanged and
uses the `:dev` image. This allows testing PRs against the last known-good image.

______________________________________________________________________

Thank you for contributing to AReaL! 🙏
