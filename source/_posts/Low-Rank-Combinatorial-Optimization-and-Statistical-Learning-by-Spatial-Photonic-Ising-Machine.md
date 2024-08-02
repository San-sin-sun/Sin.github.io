---
title: >-
  重读文献：Low-Rank Combinatorial Optimization and Statistical Learning by Spatial
  Photonic Ising Machine
date: 2024-07-01 18:34:16
categories:
  - 深度神经网络(DNN)
tags:
  - 科研
  - 神经网络
---
# 重读文献：Low-Rank Combinatorial Optimization and Statistical Learning by Spatial Photonic Ising Machine

## Introduction
Spational photonic Ising machine(SPIM) 可使用空间光调制解决大规模的Ising problem，快速计算哈密顿量。最初的SPIM只能解决秩为1的相互作用矩阵，后来解决了这个问题，但可扩展性下降。
什么是可扩展性？！
这里介绍了一个multicomponent computing model for SPIM来克服上面的限制，且适用高秩矩阵，不改变光学实现。
#### 相互作用矩阵的构造
将所有spin排成一列，$J_{i,j}$ 是第$i$ 个和第$j$ 个之间的相互作用，
#### 那我们做的模型的相互作用矩阵的秩是不是更大？可伸缩性怎么样呢？
证明了：具有满秩的相互作用的模型和普通玻尔兹曼机表达能力相当。但是在通常的低秩建模的假设中，低秩相互作用就足够了。
#### 但是我们的基本上是满秩的，而且没有因此降低速度
好像是$N-1$
注意到新导出的学习规则自然地对图像进行低秩学习，然而没有明确地施加低秩约束。
What's the meaning of "low-rank learning" and "low-rank constraints"?
## Optical computation of Ising Hamiltonian
以前的Mattis Model：J为秩为1的实对称矩阵
多组分模型：J为秩为不超过K的实对称矩阵，K不超过N。计算时间随K线性增加，但与N无关，继承了底层体系结构的可伸缩性。
## Combinatorial optimization with the multicomponent model
/
## Application to knapsack problems
举了0-1背包问题的例子，K=2。光学方法和数值方法得到的哈密顿量的典型时间演化类似。光学中吉布斯分布的温度略高，由于光学系统中的噪声。
## Statistical learning with the multicomponent model
/
## Learning MNIST digit images
K>=100,即可展示与满秩模型相当的表现。
#### 我们的需要K>=多少？
从多组分模型中采样的数字图像、学习行为。
## Discussion
矩阵的秩可以作为分类组合优化问题的index，因为该模型可以更快地解决较低秩的问题。
可以任意选择MCMC中的候选状态，且不损失计算速度。为特定的多组分SPIM设计MCMC程序重要，可能通过利用低阶特性和物理噪声。
如果SPIM硬件允许σ取非二进制的中间连续值，我们就可以实现具有丰富非线性动力学的连续值自旋系统。
综上所述，我们提出的SPIM多组件计算模型在不失去固有可扩展性的情况下，对组合优化和统计学习的各种问题具有更高的实际适用性。值得注意的是，该模型对玻尔兹曼机的低秩组合优化和低秩学习具有独特的亲和力。SPIM架构的这些意想不到的好处有望为非冯诺伊曼神经启发计算的未来发展做出贡献。
## So what's the multi-component model?
哈密顿量的计算方式不同，因此K可以取任何值。