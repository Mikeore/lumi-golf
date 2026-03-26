# LUMI-Golf

LUMI-Golf is an exploratory branch of my independent LUMI research project, adapted for the OpenAI Parameter Golf challenge.

LUMI is a personal research project focused on compact, compression-oriented, structure-biased models. In my current small-scale experiments, I have observed strong results on structure-generalization tasks, including:
- reliable grokking behavior on modular arithmetic across multiple seeds
- consistent superiority on a structural holdout benchmark under out-of-distribution generalization

This repository is **pre-submission** and focused on building a separate Parameter Golf-oriented branch rather than submitting my current LUMI project directly.

## Theoretical direction

LUMI-Golf is derived from LUMI-Arch, an independent research direction centered on a simple hypothesis:

> small models can become more capable not only through better data, but also through stronger compression-oriented inductive bias.

Instead of treating scale alone as the main path to intelligence, LUMI focuses on compact, structure-biased modeling. The guiding idea is that models that compress structure well may also generalize rules more reliably under small-model constraints.

In my current research workflow, this direction has already shown encouraging evidence on synthetic structure-generalization tasks:
- reliable grokking-style behavior on modular arithmetic
- consistent superiority on a structural holdout benchmark under out-of-distribution generalization

LUMI-Golf does **not** directly expose the full LUMI implementation. It is a separate exploratory branch intended to test whether the underlying ideas — compression-oriented modeling, compact structure-aware representations, and parameter-efficient small-model design — can transfer to the Parameter Golf setting.

## Current evidence from LUMI

The broader LUMI research project has already produced promising small-scale results relevant to this direction:

- strong modular arithmetic grokking behavior across multiple seeds
- a structural holdout benchmark with consistent balanced-accuracy gains over a baseline
- evidence that compact, structure-biased models can show reliable advantages on rule generalization under constrained settings

These results do not yet constitute a direct Parameter Golf submission. Instead, they motivate building a dedicated exploratory branch for compact language-model experiments under the challenge constraints.

## Current goal

The goal is to test whether compact structure-aware inductive biases, compression-oriented design choices, and efficient small-model ideas can transfer to the Parameter Golf setting under strict artifact-size constraints.
## Status

- exploratory
- non-record direction first
- building toward a future Parameter Golf submission
