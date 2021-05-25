---
usemathjax: true
layout: post
title:  "Learning notes for CS7643"
date:   2021-05-25

---

# Conventions

scalar $s \in \mathcal{R}^1$, vector $v\in \mathcal{R}^m$,

what is the size of $\frac{\partial v}{\partial s}$?  Column vector $\mathcal{R}^{m\times 1}$

what is the size of $\frac{\partial s}{\partial v}$?  Row vector $\mathcal{R}^{1\times m}$

what is the size of $\frac{\partial vectorone}{\partial vectortwo}$? Matrix $\mathcal{R}^{vectoroneDimen \times vectortwoDimen}$; A matrix of partial derivatives is called a **Jacobian**.

what is the size of **partial derivative of a scalar loss w.r.t. matrix weights**? A matrix  

# Update Rule

This rule is used to update one **single** weight parameters.


$$
w_j \leftarrow w_j - \eta \frac{\partial L}{\partial w_j}
$$


The above rule can be "simplified"


$$
w_j \leftarrow w_j + 2\eta\sum_{k=1}^{All Instances}\delta_kx_{kj}
$$

where $\delta_k = y_k - w^Tx_k$, **one instance** loss

# Backpropagation

* This is an recrusive algo.
1. Local ability: we can compute: $\{\frac{\partial h^l }{\partial h^{l-1}},\frac{\partial h^l }{\partial W}\}$
2. We are given: $\frac{\partial L}{\partial h^l}$
3. We need to compute:$\{\frac{\partial L }{\partial h^{l-1}},\frac{\partial L }{\partial W}\}$

But why do we need store "local nodes outputs"?

For example, if we had **max** operation, we need strictly flow back though the path which has the maximum value.
