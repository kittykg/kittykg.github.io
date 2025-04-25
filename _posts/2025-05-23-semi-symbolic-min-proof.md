---
title: 'Revisiting the Semi-symbolic Node from pix2rule'
date: 2025-04-23
permalink: /posts/2025/04/semi-symbolic-min-proof
tags:
    - neuro-symbolic
    - pix2rule
    - semi-symbolic node
---

In this post, we include an old proof and idea we had back in 2022 on the
semi-symbolic node proposed by Nuri Cingillioglu and Alessandra Russo in
pix2rule: End-to-end Neuro-symbolic Rule Learning [CR21].

The pix2rule paper can be found [here](https://arxiv.org/abs/2106.07487).

## The bias term: max or min?

Say we have a layer of $N$ inputs and each $x_i$ is either 1 or -1. The layer
itself:

$$\begin{equation*}
    \sum_i^N w_i x_i + \beta = z
\end{equation*}$$

Conjunction condition: 1. all atom true, the conjunction is true. 2. one atom
false, the conjunction is false.

\begin{equation} \label{eq:1}
    \sum_i^N |w_i| + \beta = z
\end{equation}

\begin{equation} \label{eq:2}
    \sum_{i, i \neq j}^N |w_i| - |w_j| + \beta = -z
\end{equation}

Equation \ref{eq:1} + \ref{eq:2}:

$$\begin{align*}
    -2 \beta &= \sum_i^N |w_i| + \sum_{i, i \neq j}^N |w_i| - |w_j| \\
    -2 \beta &= 2 \sum_i^N |w_i| - 2 |w_j| \\
    \beta &= |w_j| - \sum_i^N |w_i|
\end{align*}$$

We can use this as a form of $\beta$ for more general cases.

Say that there are more than one atom in the conjunction being false, this means
that the conjunction should still be false. So the layer output should be less
than 0. Let $\beta = \alpha - \sum_i^N |w_i|$.

$$\begin{align}
    \sum_{i \text{ s.t. } w_i x_i > 0}^N |w_i| - \sum_{j \text{ s.t. } w_j x_j < 0}^N |w_j| + \beta &< 0 \nonumber \\
    \sum_{i \text{ s.t. } w_i x_i > 0}^N |w_i| - \sum_{j \text{ s.t. } w_j x_j < 0}^N |w_j| + \alpha - \sum_i^N |w_i| &< 0 \nonumber \\
    \alpha - 2 \sum_{j \text{ s.t. } w_j x_j < 0} |w_j| &< 0 \nonumber\\
    \alpha < 2 \sum_{j \text{ s.t. } w_j x_j < 0} |w_j| \label{eq:3}
\end{align}$$

Note that $\alpha - 2 \sum_{j \text{ s.t. } w_j x_j < 0} |w_j|$ can be see as
the output of a conjunctive layer in general.

Go back to the conjunction condition two, the minimum case would be there is
only one atom being false in the conjunction. So Equation \ref{eq:3} becomes:

\begin{equation}\label{eq:4}
    \alpha < 2 |w_j|
\end{equation}

So a suitable value of $\alpha$ for Equation \ref{eq:4} would be $\min_{i, w_i
\neq 0} |w_i|$. If $\min_{i, w_i \neq 0} |w_i|$ happen to be the same value of
$|w_j|$, we still have inequality $|w_j| < 2 |w_j|$. If $w_j = 0$, then we go
back to Equation \ref{eq:1} case, and knowing the output of the layer is
$\alpha - 2 \sum_{j \text{ s.t. } w_j x_j < 0} |w_j|$, we know that the output
would still be greater than 0. If we take $\alpha = \min_{i, w_i \neq 0} |w_i|$
and substitute it into Equation \ref{eq:3}, the inequality should always hold,
as we have verified the base case of only one negation, and adding more to the
R.H.S would not change the result of inequality. To conclude, a conjunctive
layer's bias should be

\begin{equation}
    \beta = \min_{i, w_i \neq 0} |w_i| - \sum_i^N |w_i|
\end{equation}

A counterexample for having $\beta = \max_i |w_i| - \sum_i^N |w_i|$ (at least
during training time) is like the following. Weights are as 3, 1, 1 and input
are as 1, -1, 1.

$$\begin{align*}
    &3 \cdot 1 + 1 \cdot (-1) + 1 \cdot 1 + \beta \\
    =& 3 - 1 + 1 + (3 - (3 + 1 + 1)) \\
    =& 1 \nless 0
\end{align*}$$

Although this should be resulting a negative since there is one atom being
false, the output layer is greater than 0. However, such problem shouldn't
happen if weights are 6 / -6. If the weights are not the same, choice of max and
min doesn't matter.

## Why not min?

The reason to use max is because the stability in training provided by the max
version. The bias term enforces a strong logical constraint to the node, and
from the proof above, we can see that the min version of bias constraints the
layer 'tighter' than max. While using min helps the node to lean further towards
classical logic (i.e. the importance of the weights are not taken into account),
the bias can be heavily dominated by the sum term and hinders the learning.

## Notes

We provide a pdf version of the same proof
[here](/files/semi-symbolic-min-proof.pdf).

This proof is also included as part of the appendix in our AAMAS 2025 paper,
Neural DNF-MT: A Neuro-symbolic Approach for Learning Interpretable and Editable
Policies [BDR25]. You can check the paper
[here](/publication/neural-dnf-mt-for-learning-interpretable-editable-policies).

## Citation

[CR21] N. Cingillioglu, A. Russo. 2021. pix2rule: End-to-end Neuro-symbolic Rule
Learning.

[BDR25] K. G. Baugh, L. Dickens, A. Russo. 2025. Neural DNF-MT: A Neuro-symbolic
Approach for Learning Interpretable and Editable Policies.
