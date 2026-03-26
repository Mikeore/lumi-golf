# Results (public-safe summary)

This file summarizes the current **public-safe** benchmark evidence for LUMI.  
It reports benchmark-level outcomes and aggregated comparisons without exposing the full internal implementation.

## Official benchmark set

The current active benchmark set contains three tasks:

1. `mod_arith_grokking`
2. `bracket_structural_holdout`
3. `dsl_distributive`

`boolean_logic` is frozen and `bracket_stack` is retired.

---

## 1) mod_arith_grokking

### Setup
- Task: modular arithmetic
- Key public condition: `weight_decay=1.0`
- Main question: whether the model enters a reliable grokking regime under constrained small-model training

### Main result
- **LUMI**: groks in **4/4 seeds**
- **Baseline**: groks in **1/4 seeds**
- When Baseline does grok, it is substantially slower.
- A **parameter-matched baseline** still does not reproduce the same reliability.

### Public interpretation
The current evidence supports a **reliability and speed advantage** for LUMI under this benchmark.
The result should not be phrased as “Baseline is impossible,” but rather as:
- LUMI groks **more reliably**
- LUMI reaches the threshold **faster**
- the gap is **not removed** by simple parameter matching

---

## 2) bracket_structural_holdout

### Setup
- Structural OOD bracket benchmark
- Sampled-safe generation
- Train/test split emphasizes longer unseen structures at test time
- Primary metric: **test balanced accuracy**

### Confirmatory result
- **LUMI mean balanced accuracy**: **0.783**
- **Baseline mean balanced accuracy**: **0.632**
- **Mean delta**: **+0.151**

### Supporting evidence
- Formal confirmatory rerun completed
- Balanced-accuracy gate passed
- F1 and precision differences support the interpretation that LUMI is not simply overpredicting the positive class

### Public interpretation
This benchmark now serves as a **formal structural OOD benchmark** showing that LUMI retains a consistent advantage when evaluation moves beyond raw accuracy and toward imbalance-aware structural generalization.

---

## 3) dsl_distributive

### Setup
- Fully parenthesized binary arithmetic expressions
- Binary classification: whether a distributive-pattern subtree exists anywhere in the expression tree
- Train depth: 2–4
- Test depth: 5–7
- Primary metric: **test balanced accuracy**

### Main result
- **LUMI mean balanced accuracy**: **0.976**
- **Baseline mean balanced accuracy**: **0.750**
- **Mean delta**: **+0.226**

### Additional evidence
- All official seeds pass the benchmark gate
- The validation-to-test drop is much smaller for LUMI than for Baseline
- A parameter-matched baseline does not remove the gap

### Public interpretation
This benchmark is the clearest current bridge from synthetic structure tasks toward a more code-like expression-tree setting.  
It provides public-safe evidence that the current LUMI direction supports **structural OOD generalization** beyond trivial memorization.

---

## Parameter-matched baseline check (G5-0)

A parameter-matched baseline was tested to address the earlier confound that the original LUMI model had more parameters than the baseline.

### Public result
- `dsl_distributive`: the matched baseline does **not** reduce the gap
- `mod_arith_grokking`: the matched baseline still does **not** reproduce LUMI’s grokking reliability

### Public interpretation
The current evidence supports the claim that the observed advantage is **not explained by parameter count alone**.

---

## Public conclusion

Across the current benchmark set, the strongest public-safe claim is:

> LUMI shows consistent advantages on small-model structure generalization, including reliable grokking behavior and structural out-of-distribution performance, and these advantages are not removed by a simple parameter-matched baseline.

## What this summary intentionally does not include

To avoid exposing implementation-sensitive details, this public summary does not include:
- the full internal architecture specification,
- the full training recipe,
- implementation-critical ablation logic,
- full checkpoint or code release.
