---
title: "Neural DNF-MT: A Neuro-symbolic Approach for Learning Interpretable and Editable Policies"
collection: publications
permalink: /publication/neural-dnf-mt-for-learning-interpretable-editable-policies
excerpt: 'Neural DNF-MT: A Neuro-symbolic Approach for Learning Interpretable and Editable Policies'
date: 2025-05-19
venue: '24th International Conference on Autonomous Agents and Multiagent Systems (AAMAS 2025)'
paperurl: 'https://dl.acm.org/doi/10.5555/3709347.3743538'
citation: 'Kexin Gu Baugh, Luke Dickens, and Alessandra Russo. 2025. Neural DNF-MT:
A Neuro-symbolic Approach for Learning Interpretable and Editable
Policies. In Proc. of the 24th International Conference on Autonomous Agents
and Multiagent Systems (AAMAS 2025), Detroit, Michigan, USA, May 19 – 23,
2025, IFAAMAS.'
---

[AAMAS 2025 Proceedings](https://dl.acm.org/doi/10.5555/3709347.3743538)

[Full paper with Appendix on arxiv](https://arxiv.org/abs/2501.03888)

[GitHub Repo](https://github.com/kittykg/neural-dnf-mt-policy-learning)

[Poster](https://github.com/kittykg/neural-dnf-mt-policy-learning/blob/main/figures/poster.pdf)

[5-min intro video](https://www.youtube.com/watch?v=6_MFEDeN1cQ)

Bibtex

```bibtex
@inproceedings{10.5555/3709347.3743538,
  author    = {Baugh, Kexin Gu and Dickens, Luke and Russo, Alessandra},
  title     = {Neural DNF-MT: A Neuro-symbolic Approach for Learning Interpretable and Editable Policies},
  year      = {2025},
  isbn      = {9798400714269},
  publisher = {International Foundation for Autonomous Agents and Multiagent Systems},
  address   = {Richland, SC},
  abstract  = {Although deep reinforcement learning has been shown to be effective, the model's black-box nature presents barriers to direct policy interpretation. To address this problem, we propose a neuro-symbolic approach called neural DNF-MT for end-to-end policy learning. The differentiable nature of the neural DNF-MT model enables the use of deep actor-critic algorithms for training. At the same time, its architecture is designed so that trained models can be directly translated into interpretable policies expressed as standard (bivalent or probabilistic) logic programs. Moreover, additional layers can be included to extract abstract features from complex observations, acting as a form of predicate invention. The logic representations are highly interpretable, and we show how the bivalent representations of deterministic policies can be edited and incorporated back into a neural model, facilitating manual intervention and adaptation of learned policies. We evaluate our approach on a range of tasks requiring learning deterministic or stochastic behaviours from various forms of observations. Our empirical results show that our neural DNF-MT model performs at the level of competing black-box methods whilst providing interpretable policies.},
  booktitle = {Proceedings of the 24th International Conference on Autonomous Agents and Multiagent Systems},
  pages     = {252–260},
  numpages  = {9},
  keywords  = {neuro-symbolic learning, neuro-symbolic reinforcement learning},
  location  = {Detroit, MI, USA},
  series    = {AAMAS '25}
}
```

### Abstract

Although deep reinforcement learning has been shown to be effective, the model's
black-box nature presents barriers to direct policy interpretation. To address
this problem, we propose a neuro-symbolic approach called neural DNF-MT for
end-to-end policy learning. The differentiable nature of the neural DNF-MT model
enables the use of deep actor-critic algorithms for training. At the same time,
its architecture is designed so that trained models can be directly translated
into interpretable policies expressed as standard (bivalent or probabilistic)
logic programs. Moreover, additional layers can be included to extract abstract
features from complex observations, acting as a form of predicate invention. The
logic representations are highly interpretable, and we show how the bivalent
representations of deterministic policies can be edited and incorporated back
into a neural model, facilitating manual intervention and adaptation of learned
policies. We evaluate our approach on a range of tasks requiring learning
deterministic or stochastic behaviours from various forms of observations. Our
empirical results show that our neural DNF-MT model performs at the level of
competing black-box methods whilst providing interpretable policies.
