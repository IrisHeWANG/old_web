---
title: "Learning for Optimization: Decentralized Statistical Inference with Unrolled Graph Neural Networks"
excerpt: "In this paper, we investigate the decentralized statistical inference problem and propose a learning-based framework, which unrolls well-noted decentralized optimization algorithms into graph neural networks (GNNs). This method addresses the issues of model mismatch and improve convergence speed to a large extent. "
collection: research
---

<p>&nbsp;</p>

In this paper, we consider the decentralized statistical inference problem that a network of agents cooperatively recover a (structured) vector $x^*$ from private noisy samples measurements $y_i = f_i(x^*) + \epsilon_i$, where $f_i$ is a sampling function and $\epsilon_i$ is the measurement noise at agent $i$.



Existing optimizationbased algorithms suffer from issues of model mismatch and poor convergence speed, and thus their performance would be degraded, provided that the number of communication rounds is limited. This motivates us to propose a learning-based framework, which unrolls well-noted decentralized optimization algorithms (e.g., Prox-DGD and PG-EXTRA) into graph neural networks (GNNs). 



<p align="center">
  <img src='/images/research/GNN/model.png'>
</p>



By minimizing the recovery error via end-toend training, this learning-based framework resolves the model mismatch issue. Our convergence analysis (with PG-EXTRA as the base algorithm) reveals that the learned model parameters may accelerate the convergence and reduce the recovery error to a large extent. The simulation results demonstrate that the proposed GNN-based learning methods prominently outperform several state-of-the-art optimization-based algorithms in convergence speed and recovery error.



<p align="center">
  <img src='/images/research/GNN/result1.png'>
</p>



<p align="center">
  <img src='/images/research/GNN/result2.png'>
</p>




## Reference:

1. He Wang, Yifei Shen, Ziyuan Wang, Dongsheng Li, Jun Zhang, Khaled B. Letaief and Jie Lu, "[Decentralized Statistical Inference with Unrolled Graph Neural Networks](https://arxiv.org/abs/2104.01555)", accepted to *IEEE Conference on Decision and Control (CDC)*, 2021. [[Paper]](https://arxiv.org/pdf/2104.01555.pdf) [[Source Code]](https://github.com/IrisWangHe/Learning-based-DOP-Framework)

