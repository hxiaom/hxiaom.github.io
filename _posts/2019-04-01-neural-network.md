---
layout: post
title: 【Method】深度学习（二）深度前馈网络
categories: Analytics
---

## 原理

深度前馈网络（deep feedforward network），也叫作前馈神经网络（feedforward neural network）或者多层感知机（multilayer perceptron, MLP），是典型的深度学习模型。前馈网络的目标是近似某个函数$$f^*$$。例如，对于分类器，$$y=f^*(x)$$将输入x映射到一个类别y。前馈网络定义了一个映射$$y=f(x;\theta)$$，并且学习参数$$]theta$$的值，使它能够得到最佳的函数近似。