# LUMI-Golf

LUMI-Golf is an exploratory compact language-model branch derived from my independent LUMI-Arch research.

LUMI-Arch is a compression-oriented, multi-scale variant of linear attention for compact language-model research. The working hypothesis is that small models may gain stronger generalization not only from scale, but from architectural inductive bias that favors compression and structured abstraction across multiple scales.

This repository is intentionally public-safe:
- it describes the research direction and benchmark evidence,
- it shares benchmark specifications and aggregated results,
- it does not expose the full implementation details of the underlying architecture.

## Why this branch exists

The current LUMI-Arch research workflow has already produced encouraging small-scale evidence:

- **mod_arith_grokking**: multi-seed reliability and speed advantage under a weight-decay-driven grokking setting
- **bracket_structural_holdout**: formal benchmark showing consistent balanced-accuracy superiority under structural out-of-distribution evaluation
- **dsl_distributive**: formal benchmark showing strong structural OOD generalization on expression-tree detection

These results motivated a separate branch for compact-model and artifact-efficient exploration.

## Current public evidence

### 1) mod_arith_grokking

- LUMI-Arch groks reliably across seeds under the official wd=1.0 setting.
- Baseline sometimes improves, but is much less reliable and slower.
- A parameter-matched baseline still does not remove the gap.

### 2) bracket_structural_holdout

- LUMI-Arch consistently outperforms Baseline on balanced accuracy across confirmatory seeds.
- This benchmark is treated as a formal benchmark rather than an exploratory candidate.

### 3) dsl_distributive

- LUMI-Arch consistently outperforms Baseline on a structural OOD expression-tree benchmark.
- The matched-baseline check does not remove the gap.

## What this repository is for

This repository is not a direct release of the full LUMI-Arch implementation. Instead, it is a public-facing research companion used to:

- document benchmark specifications,
- publish aggregated evidence,
- state what is currently supported vs. what remains unresolved,
- prepare future compact-model / Parameter Golf style explorations.

## Current status

- exploratory public branch
- benchmark evidence documented
- implementation details intentionally limited
- suitable as a research overview / challenge companion repository

## Additional notes

- [Results summary](./results.md)
- [Claims and limits](./claims_and_limits.md)
- [Official evaluation summary (CSV)](./results/official_eval_summary.csv)
