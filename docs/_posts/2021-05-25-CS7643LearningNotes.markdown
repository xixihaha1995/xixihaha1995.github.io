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

