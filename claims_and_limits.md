# Claims and limits (public-safe)

This file separates what the current evidence supports from what would be too strong to claim publicly at this stage.

## What the current evidence supports

### 1) LUMI has benchmark-level evidence, not just anecdotes
The project now has multiple active benchmarks with formal or frozen evaluation rules, rather than a single isolated successful run.

### 2) LUMI shows strong small-model structure-generalization behavior
The strongest current public-safe support comes from:
- modular arithmetic grokking reliability,
- bracket-based structural OOD evaluation,
- distributive-pattern detection on deeper unseen expression trees.

### 3) The current advantage is not explained by parameter count alone
A parameter-matched baseline was tested and did not remove the observed advantage on the representative G5-0 checks.

### 4) The evidence is strongest for reliability, structural OOD, and compressed small-model generalization
The public evidence currently supports claims about:
- reliability of grokking-style behavior,
- structural generalization under distribution shift,
- benchmarked superiority under constrained small-model conditions.

---

## What should **not** be claimed yet

### 1) “LUMI solves general language modeling”
Not supported by the current evidence.

### 2) “LUMI beats all baseline families in all regimes”
Not supported. The current claims are benchmark-specific.

### 3) “The exact internal mechanism is fully proven”
The evidence supports an architectural advantage, but not a complete mechanistic proof.

### 4) “The system is already record-ready for open competitions”
Not yet. The current public branch is exploratory and public-safe.

### 5) “The baseline is fundamentally incapable”
This is too strong. In at least one setting, Baseline can occasionally improve; the stronger supported statement is that LUMI is more reliable and/or faster under the tested regime.

---

## Public-safe wording guide

### Safe phrasing
- “shows a consistent advantage”
- “supports a structure-generalization advantage”
- “improves reliability under the tested regime”
- “the gap is not removed by a parameter-matched baseline”
- “promising evidence”
- “public-safe benchmark evidence”

### Avoid for now
- “proves intelligence”
- “beats all Transformers”
- “impossible for baseline”
- “universally superior”
- “fully solved”

---

## Disclosure policy

This repository intentionally publishes:
- benchmark specifications,
- aggregated benchmark results,
- high-level research framing,
- claims and limits.

This repository intentionally does **not** publish:
- the full implementation-sensitive architecture details,
- full training recipes,
- checkpoint releases,
- implementation-critical internal ablations.

---

## Current public-facing summary

The strongest public-safe summary at the moment is:

> LUMI is an independent compact-model research direction that has shown consistent benchmark evidence for reliable grokking-style behavior and structural out-of-distribution generalization, with gaps that are not removed by a simple parameter-matched baseline.

That summary is strong enough to be meaningful, while remaining narrower than claims that would require a broader language-model evaluation program.
