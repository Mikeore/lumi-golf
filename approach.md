# Approach

This repository is an exploratory Parameter Golf branch derived from my independent LUMI-Arch research.

LUMI-Arch is a compression-oriented, multi-scale variant of linear attention for compact language-model research. It is not presented here as a finished general-purpose LLM, but as an architecture research direction aimed at improving structure-sensitive generalization under small-model constraints.

## Core idea

The central hypothesis is simple:

> small models may become more capable not only through scale, but through stronger compression-oriented inductive bias and structure-aware sequence representations.

Instead of treating scale alone as the main path to capability, LUMI-Arch emphasizes compact, structure-aware sequence modeling. The motivating idea is that models that compress structure across multiple scales may generalize rules more reliably under constrained parameter budgets.

## Why this may matter

In the broader LUMI-Arch workflow, these ideas have already shown promising behavior on small structure-generalization tasks, including:

- reliable grokking-style behavior on modular arithmetic,
- strong performance on structural out-of-distribution benchmarks,
- parameter-matched checks where the baseline still does not close the gap.

These results do not yet constitute a direct Parameter Golf submission. They are the reason this exploratory branch exists.

## Parameter Golf direction

I do not plan to submit the current LUMI-Arch research code directly. Instead, the goal of this repository is to test whether the most relevant underlying ideas can transfer into a compact language-model setting shaped by strict artifact-size constraints.

The specific direction is to explore whether:
- compact structure-aware representations,
- compression-oriented design choices,
- and parameter-efficient small-model techniques

can become useful ingredients for a future Parameter Golf-oriented implementation.

## Scope

This repository is intentionally limited in scope.

It is meant to:
- explain the architectural direction at a high level,
- document benchmark evidence,
- and support future compact LM / Parameter Golf style experimentation.

It is **not** meant to expose the complete implementation details of the underlying LUMI-Arch system.

## Current stage

- pre-submission / exploratory
- public-safe research companion
- non-record direction first
- compact LM transfer hypothesis under evaluation
