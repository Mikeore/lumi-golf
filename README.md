# LUMI-Golf

LUMI-Golf is an exploratory compact language-model research branch derived from my independent LUMI-Arch work.

LUMI-Arch is a compact architecture research direction centered on a simple but demanding idea: small models may become more capable not only through scale, but through architectural bias that encourages efficient structured abstraction. Rather than treating capability as a direct consequence of size alone, this direction explores whether compact models can gain stronger generalization by learning to preserve and compress useful structure.

This repository is intentionally **public-safe**:
- it describes the research direction at a high level,
- it shares benchmark specifications and aggregated evidence,
- it does **not** expose the full implementation details of the underlying architecture.

## Why this branch exists

The broader LUMI-Arch workflow has already produced encouraging evidence on small-scale structure-generalization tasks.

Across multiple compact benchmarks, the current research direction has shown:
- reliable rule-generalization behavior under constrained settings,
- strong performance on structural out-of-distribution evaluation,
- and benchmark wins that are not removed by simply scaling a comparison baseline to a similar parameter budget.

These results do **not** yet constitute a direct Parameter Golf submission. Instead, they motivate a separate branch dedicated to compact language-model exploration under artifact-size pressure.

## What this repository is for

This repository exists to serve as a public-facing research companion for that direction.

Its goals are to:
- document current benchmark evidence,
- describe the research hypothesis at a safe level,
- clarify what is currently supported versus unresolved,
- and support future compact-model explorations, including Parameter Golf style experiments.

It is **not** intended to be a full release of the underlying LUMI-Arch implementation.

## Current evidence

At the current stage, the strongest public signals motivating this branch are:

### 1. Reliable rule-generalization under constrained settings
The research direction has already shown strong behavior on compact symbolic tasks where reliable generalization matters more than raw memorization.

### 2. Structural OOD strength
The model family has shown consistent superiority on structural holdout style benchmarks where evaluation requires generalizing beyond the exact structures seen during training.

### 3. Robustness against simple parameter-count explanations
In representative comparisons, increasing baseline parameter count alone does not remove the observed gap, suggesting that the strongest gains are not explained by scale alone.

## Current status

- exploratory public branch
- benchmark evidence documented
- implementation details intentionally limited
- compact LM transfer hypothesis under active evaluation
- non-record direction first

## Repository guide

- [Results summary](./results.md)
- [Claims and limits](./claims_and_limits.md)
- [Official evaluation summary (CSV)](./results/official_eval_summary.csv)

## Note

This repository is designed to communicate the direction, evidence, and evaluation stance of the project without publishing the full internal recipe behind the underlying architecture.
