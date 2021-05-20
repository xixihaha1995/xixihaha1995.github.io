---
usemathjax: true
layout: post
title:  "Cross Entropy Introduction"
date:   2021-05-20 10:00:36 +0000

---

# Equation

$$
Information = -log(P(x))
$$

$$
Entropy\quad H(X) = -\sum_i p_i log(p_i)
$$

where $p_i$ is probability that the system in the $i$th state.

For cross-entropy/distance from approximation distribution to target distribution/similarity between target distribution P and approximation distribution Q


$$
CrossEntropy(P,Q)\quad H(P,Q) = -\sum_i P_i log(Q_i)
$$
where $P_i$ is the probability of the event i in P, $Q_i$ is the probability of event x in Q, $log$ is the base 2 logarithm.

