---
title: 阅读文献：All-optical machine learning using diffractive deep neural networks
date: 2024-06-30 00:41:11
categories:
  - 深度神经网络(DNN)
tags:
  - 科研
  - 神经网络
---
原文链接 [All-optical machine learning using diffractive deep neural networks](https://www.science.org/doi/10.1126/science.aat8084)。
# 阅读文献：All-optical machine learning using diffractive deep neural networks

##似乎没有意义，训练是数值的，只有根据训练好的结构得出结果这最后一步是光的衍射。

## Introduction
介绍了深度神经网络及其应用：主流应用、解决逆成像问题( inverse imaging problems )

Here: 神经网络由多层的衍射表面组成，这些衍射表面协同工作，以光学方式执行网络可以统计学习的任意功能。leads to its design的学习部分在计算机上完成，推理和预测机制是全光的。叫做$D^2NN$。该神经网络可以使用几个透射或反射层，给定层要么透射，要么反射，代表一个人工神经元，通过光学衍射与其它神经元连接。

## Theory
由惠更斯-菲涅尔原理，给定层的每一个点作为次波源，每个点的透射或反射系数可以看作是偏置项（可以学习的参数，使用error back-propagation method）。数值训练之后，$D^2NN$的结构不变，即每一个点的反射、透射系数不变。