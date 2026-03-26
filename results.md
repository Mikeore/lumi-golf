# Results

This document summarizes the current public-safe benchmark evidence behind LUMI-Arch.

The goal here is not to expose the full internal recipe of the system, but to show the strongest currently supported benchmark signals in a compact and verifiable form.

## Evaluation stance

The current public benchmark set focuses on three questions:

1. **Can a compact architecture show reliable rule generalization under constrained settings?**
2. **Can it generalize structural patterns beyond the exact forms seen during training?**
3. **Does the observed advantage remain after stronger baseline comparisons, including parameter-matched checks?**

The active public benchmark set currently consists of:

- `mod_arith_grokking`
- `bracket_structural_holdout`
- `dsl_distributive`

## Headline summary

Across the current active benchmark set, LUMI-Arch shows three recurring signals:

- **reliable compact-rule generalization**
- **strong structural OOD performance**
- **advantages that are not removed by simply scaling a comparison baseline to a similar parameter budget**

These results support the broader research hypothesis that compact models may benefit from stronger architectural bias toward efficient structured abstraction.

## Benchmark summary

| Benchmark | Public interpretation | Current signal |
|---|---|---|
| `mod_arith_grokking` | Reliability and speed of grokking-style generalization under constrained settings | LUMI-Arch shows stronger multi-seed reliability and earlier threshold crossing than baseline comparisons |
| `bracket_structural_holdout` | Structural out-of-distribution generalization under strong class imbalance | LUMI-Arch shows consistent balanced-accuracy superiority across confirmatory seeds |
| `dsl_distributive` | Structural OOD generalization on expression-tree detection | LUMI-Arch shows a strong mean gap over baseline, and the gap is not removed by a matched-baseline check |

## Public-safe benchmark notes

### 1. mod_arith_grokking

This benchmark is important because it tests more than final score. It tests whether a compact model reaches useful generalization **reliably** and **quickly** across seeds under a constrained setup.

The strongest current public conclusion is:

- LUMI-Arch reaches successful grokking-style behavior more reliably than the baseline family
- when the baseline does succeed, it does so less reliably and typically more slowly
- stronger baseline variants improve somewhat, but the core gap is not removed

This is currently interpreted as evidence of an architectural advantage in reliability and efficiency under the tested setting, not as a universal impossibility claim about the baseline.

### 2. bracket_structural_holdout

This benchmark was promoted from exploratory status to a formal benchmark because the gap held up under confirmatory reruns and because the primary metric was designed to avoid misleading conclusions from severe class imbalance.

The strongest current public conclusion is:

- LUMI-Arch consistently outperforms the baseline on balanced accuracy
- the benchmark stresses structural out-of-distribution generalization rather than shallow memorization
- this result is treated as part of the current formal benchmark record

### 3. dsl_distributive

This benchmark acts as a bridge from abstract structural tasks toward more expression-like symbolic structure.

The strongest current public conclusion is:

- LUMI-Arch shows a strong structural OOD advantage
- increasing baseline parameter count alone does not remove the observed gap
- the result supports the view that the strongest gains are not explained by scale alone

## Current public interpretation

At the present stage, the benchmark record supports the following public-safe interpretation:

- LUMI-Arch is a compact architecture research direction with strong evidence on structure-sensitive generalization
- the strongest current signals appear in rule-learning, structural OOD, and reliability under constrained settings
- simple baseline scaling does not fully explain the observed advantages on representative benchmarks

## What this does **not** claim

These results do **not** yet imply:

- that the architecture has been fully validated on large-scale natural-language language modeling
- that every possible baseline family has been exhausted
- that the public benchmark record exposes the complete internal mechanism behind the system
- that benchmark success alone is sufficient to establish broad real-world superiority

## Additional files

- [Claims and limits](./claims_and_limits.md)
- [Official evaluation summary (CSV)](./results/official_eval_summary.csv)

## Note

This file is intentionally written at the level of benchmark evidence and public interpretation. It is designed to communicate supported findings without disclosing the full implementation strategy of the underlying architecture.
