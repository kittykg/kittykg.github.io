---
title: "Neuro-symbolic Rule Learning in Real-world Classification Tasks"
collection: publications
permalink: /publication/neuro-symbolic-rule-learning-in-real-world-classification-tasks
excerpt: 'Neuro-symbolic rule learning with **neural DNF-based** models in
real-world multi-class and multi-label classification tasks.'
date: 2023-03-27
venue: ' AAAI 2023 Spring Symposium on Challenges Requiring the Combination of Machine Learning and Knowledge Engineering (AAAI-MAKE 2023)'
paperurl: 'https://ceur-ws.org/Vol-3433/paper12.pdf'
citation: 'K. G. Baugh, N. Cingillioglu, and A. Russo, “Neuro-symbolic Rule Learning in Real-world Classification Tasks,” in Proceedings of the AAAI 2023 Spring Symposium on Challenges Requiring the Combination of Machine Learning and Knowledge Engineering (AAAI-MAKE 2023), A. Martin, H.-G. Fill, A. Gerber, K. Hinkelmann, D. Lenat, R. Stolle, and F. van Harmelen, Eds., CEUR Workshop Proceedings, 2023.'
---

Neuro-symbolic rule learning with **neural DNF-based** models in real-world
multi-class and multi-label classification tasks.

[Download from AAAI-MAKE 2023 program here]('https://proceedings.aaai-make.info/AAAI-MAKE-PREPRINTS-2023/Paper_6465.pdf')

[Download from CEUR Workshop Proceedings here](https://ceur-ws.org/Vol-3433/paper12.pdf)

[Download from arXiv here](https://arxiv.org/abs/2303.16674)


Bibtex for AAAI-MAKE 2023 proceedings

```
@inproceedings{ns-classifications,
  title        = {Neuro-symbolic Rule Learning in Real-world Classification Tasks},
  year         = {2023},
  author       = {Baugh, Kexin Gu and Cingillioglu, Nuri and Russo, Alessandra},
  booktitleaddon    = {Proceedings of the AAAI 2023 Spring Symposium on Challenges Requiring the Combination of Machine Learning and Knowledge Engineering (AAAI-MAKE 2023)},
  editor       = {Martin, Andreas and Fill, Hans-Georg and Gerber, Aurona and Hinkelmann, Knut and Lenat, Doug and Stolle, Reinhard and van Harmelen, Frank},
  volume       = {Vol-3433},
  venue        = {Hyatt Regency, San Francisco Airport, California, USA},
  publisher    = {CEUR Workshop Proceedings},
  url          = {https://ceur-ws.org/Vol-3433/paper12.pdf},
}
```

Bibtex for arxiv pre-print

```
@misc{aaai-make-2023-6465,
    title={Neuro-symbolic Rule Learning in Real-world Classification Tasks}, 
    author={Kexin Gu Baugh and Nuri Cingillioglu and Alessandra Russo},
    year={2023},
    eprint={2303.16674},
    archivePrefix={arXiv},
    primaryClass={cs.LG}
}
```

### Abstract

Neuro-symbolic rule learning has attracted lots of attention as it offers better interpretability than pure neural models and scales better than symbolic rule
learning. A recent approach named pix2rule proposes a neural Disjunctive Normal
Form (neural DNF) module to learn symbolic rules with feed-forward layers.
Although proved to be effective in synthetic binary classification, pix2rule has
not been applied to more challenging tasks such as multi-label and multi-class
classifications over real-world data. In this paper, we address this limitation
by extending the neural DNF module to (i) support rule learning in real-world
multi-class and multi-label classification tasks, (ii) enforce the symbolic
property of mutual exclusivity (i.e. predicting exactly one class) in
multi-class classification, and (iii) explore its scalability over large inputs
and outputs. We train a vanilla neural DNF model similar to pix2rule’s neural
DNF module for multi-label classification, and we propose a novel extended model
called neural DNF-EO (Exactly One) which enforces mutual exclusivity in
multi-class classification. We evaluate the classification performance,
scalability and interpretability of our neural DNF-based models, and compare
them against pure neural models and a state-of-the-art symbolic rule learner
named FastLAS. We demonstrate that our neural DNF-based models perform similarly
to neural networks, but provide better interpretability by enabling the
extraction of logical rules. Our models also scale well when the rule search
space grows in size, in contrast to FastLAS, which fails to learn in multi-class
classification tasks with 200 classes and in all multi-label settings.
