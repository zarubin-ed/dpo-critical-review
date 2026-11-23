[English](README.md) | [Русский](README.ru.md)

# Critical Review of Direct Preference Optimization (DPO)

A critical analysis of **"Direct Preference Optimization: Your Language Model is Secretly a Reward Model"** (Rafailov et al., 2023).

This review examines the mathematical foundations of DPO, evaluates the authors' theoretical results and experimental conclusions, and proposes potential directions for further research.

**[Read the Review (PDF)](en/review.pdf)** | [LaTeX Source](en/review.tex)

## Review Overview

### 1. Theoretical Analysis

This section examines the mathematical foundations of DPO, focusing on the transition from policy optimization with a separate reward model to direct learning from preference data.

The main topics include:

- Derivation of the DPO loss function and analysis of its gradient.
- The theorem establishing equivalence classes of reward functions and their representation through policies.
- Limitations of the method's theoretical guarantees.
- An explanation of training stability through reward function normalization.

### 2. Critical Evaluation of Experiments

This section analyzes experiments on sentiment control, text summarization, and single-turn dialogue.

The discussion focuses on:

- Whether the experimental evidence sufficiently supports the claimed training stability and computational efficiency of DPO.
- The fairness of comparisons between DPO, PPO, and other preference-learning algorithms.
- The influence of the hyperparameter β and generation temperature.
- The reliability of using GPT-4 for automated response quality evaluation.

### 3. Novelty of the Results

This section examines the relationship between DPO and prior approaches, including AWR, ASAF, RRHF, and SLiC-HF.

It evaluates which elements of the approach were already established in earlier research and identifies the original contributions of the DPO paper.

## Proposed Research Directions

The second part of the review explores potential extensions and improvements to DPO.

**Generalizing the preference model.** Instead of relying on the Bradley–Terry model, the review proposes considering a broader class of preference models with stochastic response evaluation errors. The corresponding loss function is derived, and the properties of gradient weights are compared under logistic and Gaussian error distributions.

**Alternative regularizers.** The possibility of replacing KL divergence with another regularization term while preserving the central idea of DPO is explored. The potential effects of different regularizers on the diversity of generated responses are also discussed.

**Additional experiments.** Several experiments are proposed, including comparisons under equal computational budgets, investigations of gradient variance, analysis of the influence of β, and evaluation of how generation temperature affects response quality and diversity.

These experiments are proposed as directions for future research and **were not implemented as part of this review**.

## Original Paper

Rafailov R. et al. **Direct Preference Optimization: Your Language Model is Secretly a Reward Model.** 2023.

[arXiv:2305.18290](https://arxiv.org/abs/2305.18290)

## Author

Egor Zarubin  
Moscow Institute of Physics and Technology (MIPT)  
Applied Mathematics and Computer Science, 2026.

The English translation was prepared with the help of ChatGPT.
