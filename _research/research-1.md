---
title: "An Inexact Fenchel Dual Gradient Algorithm for Distributed Optimization"
excerpt: "In this paper, we design a distributed algorithm for addressing constrained convex optimization over networks. The proposed algorithm is developed by substituting a projected gradient operation for a convex minimization step at each iteration of the Fenchel dual gradient (FDG) method, so that the high computational load of FDG can be significantly alleviated."
collection: research
---

<p>&nbsp;</p>

We consider that a set of agents $\mathcal{V} = \{1,\ldots,N\}$, cooperativly solve the following convex constrained optimization problem:


$$
\begin{array}{ll}
\operatorname{minimize}_{x \in \mathbb{R}^{d}} & \sum_{i \in \mathcal{V}} f_{i}(x) \\
\text { subject to } & x \in \bigcap_{i \in \mathcal{V}} X_{i}
\end{array}
$$
- $f_i$ is strongly convex and smooth.
- $X_i$ is closed and convex.



One of well-noted existing algorithms, Fenchel dual gradient (FDG) method, is able to solve such optimization, by applying a weighted gradient method to the Fenchel dual problem of the above problem. Convergence rate guarantees of FDG are also derived, which are highly scalable in terms of the network size. However, in order to evaluate the gradient of the Fenchel dual function, FDG requires each node to solve a constrained convex optimization problem per iteration, which could be very costly. 

Motivated by the above advantage and drawback of FDG, in this paper we propose an **Inexact Fenchel Dual Gradient (IFDG) algorithm** for constrained distributed convex optimization. Instead of computing the exact Fenchel dual gradient via solving a constrained convex optimization problem as FDG does, here we derive an *inexact* Fenchel dual gradient by applying a single projected gradient operation on the latest iterate. Such a substitute is able to lower the computational costs of FDG to a great extent. 



<p align="center">
  <img src='/images/research/IFDG/diff.png'>
</p>



Moreover, we show that IFDG achieves an $O(1/k)$ rate of convergence to the optimal solution if the local objective functions are strongly convex and smooth, and a linear rate if the problem is further assumed to be unconstrained. Finally, we validate the efficiency of IFDG in comparison with FDG with respect to convergence speed, accuracy, and running time.



<p align="center">
  <img src='/images/research/IFDG/result.png'>
</p>



## Reference:

1. He Wang and Jie Lu, "[An Inexact Fenchel Dual Gradient Algorithm for Distributed Optimization](https://ieeexplore.ieee.org/abstract/document/9264365)'',  in *IEEE International Conference on Control & Automation (ICCA)*, 2020. 