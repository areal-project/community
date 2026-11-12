# AReaL Community Meeting Notes (2026-10-31)

English | [Chinese](README_CN.md)

These notes summarize the discussions, decisions, and action items from the meeting.
Progress, validation results, and timelines reflect the status as of the meeting date.

## Key Decisions and Updates

### 1. VRM Optimizations and Bug Fixes

- **Vision Tower freezing and cache refresh**: Updating Vision Tower parameters during
  RL training while reusing stale embedding caches in SGLang inference causes drift in
  the training-inference log-probability difference (log p diff). Two approaches were
  agreed upon: freeze Vision Tower weights during RL training, or refresh the cache
  during the S-stage plug-in step.
- **Consistent image compression**: Differences between the training-side Hugging Face
  processor and SGLang's inference-side image processing, such as compression ratios for
  large image blocks, have been addressed. The `AREAL_VRM_ALIGN_SGLANG` environment
  variable, which defaults to `true`, aligns training-side image compression with SGLang
  to reduce training-inference discrepancies.
- **FSDP benchmarking tool**: A benchmarking tool for the FSDP training backend is
  available, with a README and usage guide for single-GPU performance evaluation and
  stress testing.

### 2. Standardized Benchmarking

The community plans to introduce standardized benchmark methods and datasets covering
IR/VR, agent workloads, and other scenarios, drawing on similar work in the vLLM
community. These benchmarks will evaluate AReaL's performance and the performance impact
of merged PRs. The team is conducting internal validation to ensure unbiased evaluation.

### 3. Score Centering Support

AReaL now supports Score Centering with the SGLang and FSDP backends to mitigate the
effects of training-inference discrepancies. Results shared at the meeting showed
improved training accuracy.

**Limitation: Score Centering and rejection sampling cannot be used together.**

### 4. Hardware Ecosystem Expansion

- **AMD GPUs**: End-to-end execution is working. Contributors have provided a
  Dockerfile, and related bug-fix PRs have been merged into the main repository.
- **Intel XPUs**: Initial support has been merged into the main repository. Only
  small-scale experiments have been completed; large-scale validation is still pending.
- **CI policy**: AMD and Intel support is integrated directly into the main repository.
  Passing NVIDIA GPU CI remains a prerequisite for merging changes; changes that fail
  these checks will not be merged for now.

### 5. FP8 Training Support

- **Current status**: A PR adding FP8 training support for Qwen2.5 Dense models has been
  submitted and is undergoing initial validation. Two configurations are supported: BF16
  training with FP8 inference, and FP8 training with FP8 inference.
- **Recommended configuration**: Tests showed substantial drift in training-inference
  discrepancies when using FP8 for both training and inference. **BF16 training with FP8
  inference** is currently recommended to balance performance gains and numerical
  stability.
- **Next steps**: The PR is expected to merge in the week following the meeting for
  community use and validation. Further work will explore which parts of MoE models are
  suitable for FP8 quantization.

### 6. Controlling Training-Inference Policy Version Gaps

Two mechanisms have been added to address excessive policy version gaps caused by slow,
long-tail data in asynchronous training:

- **Inference side**: Discard stale data during sampling.
- **Actor side**: Mask tokens that are too old so they do not contribute to the loss.

These mechanisms control policy-version staleness in the data to improve training
stability. The related PR is awaiting review and merge.

### 7. AReaL Autopilot Presentation (Wenshuang Li)

- **Goal**: Reduce manual intervention in model adaptation and deployment through
  full-lifecycle automation.
- **Kernel Evolution**: Use agents to automatically search for and evolve efficient
  Unified Kernels that satisfy numerical consistency requirements. Measurements on H20
  showed approximately 10% higher end-to-end throughput and 2-5x speedups in attention
  test cases.
- **Elastic Training**: Decouple components through a microservices architecture and
  dynamically allocate or release Actor resources based on workload. A demo verified
  dynamic scaling from 0 to 4 GPUs for the Actor. Simulations showed approximately
  10%-20% improvement; testing on real workloads remains pending.

## Action Items

| Owner                 | Action                                                                                                                                            | Timeline / Status                          |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ | :----------------------------------------- |
| Jiale Li              | Merge the FP8 training support PR for Qwen2.5 Dense models for community use and validation.                                                      | Expected in the week following the meeting |
| Jiale Li              | Merge the policy version gap control PR, including stale-data discarding on the inference side and token masking on the Actor side.               | Pending Approver review                    |
| Jiale Li and team     | Continue internal validation of standardized benchmark methods and datasets; release them to the community once unbiased evaluation is confirmed. | In progress                                |
| Wenshuang Li and team | Organize TicToc project materials, move them to the community, and share them more broadly.                                                       | After the materials are organized          |
| Wenshuang Li          | Test Workload-Aware Dynamic Reconfiguration in Elastic Training on real workloads; only simulations have been completed so far.                   | Immediate next step                        |
| Community members     | Raise PRs that need priority review and merging during community meetings or in the WeChat group.                                                 | Ongoing                                    |

## Open Questions and Discussion

### 1. FP8 Support on Ascend NPUs

Jiale Li asked Yong whether Ascend NPUs had stable support for FP8 training and
inference. Yong reported that initial experiments had been conducted only on the Ascend
910B (A5) branch. Basic functionality was working, but comprehensive validation remained
incomplete due to limited hardware availability.

### 2. CI Strategy Across Hardware Platforms

Yong raised concerns that changes to the main repository could cause CI failures on
non-NVIDIA hardware, such as NPUs. Jiale Li confirmed that AMD and Intel support had
been merged into the main repository, while NVIDIA GPU CI remained a mandatory merge
check. The underlying NPU implementation (Macron/MindSpeed) differs from the main
repository, so compatibility requires continued monitoring and validation.

### 3. Connecting Autopilot with Benchmarking

Jiale Li noted that Autopilot's dynamic adjustments still lacked a unified final
evaluation criterion. He suggested integrating Autopilot with the benchmarking framework
under development so that it could use benchmarks to evaluate and optimize itself.
Binhang Yuan agreed, viewing this as part of improving the RSI loop.
