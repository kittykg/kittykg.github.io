---
title: "Disentangling Neural Disjunctive Normal Form Models"
collection: publications
permalink: /publication/disentangling-ndnf-models
excerpt: 'Disentangling Neural Disjunctive Normal Form Models'
date: 2025-09-08
venue: '19th International Conference on Neurosymbolic Learning and Reasoning (NeSy 2025)'
paperurl: 'https://arxiv.org/abs/2507.10546'
citation: 'Kexin Gu Baugh, Vincent Perreault, Matthew Baugh, Luke Dickens,
Katsumi Inoue, and Alessandra Russo. 2025. Disentangling Neural Disjunctive
Normal Form Models. NeSy 2025, Santa Cruz, California, USA. Sep 8-10, 2025.'
---

[Arxiv Preprint](https://arxiv.org/abs/2507.10546)

[GitHub Repo](https://github.com/kittykg/disentangling-ndnf-classification)

Arxiv preprint BibTeX:

```bibtex
@misc{baugh2025disentanglingneuraldisjunctivenormal,
      title={Disentangling Neural Disjunctive Normal Form Models},
      author={Kexin Gu Baugh and Vincent Perreault and Matthew Baugh and Luke Dickens and Katsumi Inoue and Alessandra Russo},
      year={2025},
      eprint={2507.10546},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2507.10546},
}
```

### Abstract

Neural Disjunctive Normal Form (DNF) based models are powerful and interpretable
approaches to neuro-symbolic learning and have shown promising results in
classification and reinforcement learning settings without prior knowledge of
the tasks. However, their performance is degraded by the thresholding of the
post-training symbolic translation process. We show here that part of the
performance degradation during translation is due to its failure to disentangle
the learned knowledge represented in the form of the networks' weights. We
address this issue by proposing a new disentanglement method; by splitting nodes
that encode nested rules into smaller independent nodes, we are able to better
preserve the models' performance. Through experiments on binary, multiclass, and
multilabel classification tasks (including those requiring predicate invention),
we demonstrate that our disentanglement method provides compact and
interpretable logical representations for the neural DNF-based models, with
performance closer to that of their pre-translation counterparts.
