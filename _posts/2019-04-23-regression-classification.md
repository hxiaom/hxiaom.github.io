---
layout: post
title: 【Method】分类与回归
categories: Analytics
---

## 原理

输入变量与输出变量均为连续变量的预测问题是回归问题；
 
输出变量为有限个离散变量的预测问题成为分类问题；

Supervised learning problems are categorized into "regression" and "classification" problems. In a regression problem, we are trying to predict results within a continuous output, meaning that we are trying to map input variables to some continuous function. In a classification problem, we are instead trying to predict results in adiscrete output. In other words, we are trying to map input variables into discrete categories.

“回归”一词最早被高尔顿提出。高尔顿最著名的发现之一是他发现了父亲的身高和儿子的身高之间存在着某种给定的关系，他通过进一步的研究发现了：事实上子辈的平均身高是其父辈平均身高以及他们所处族群平均身高的加权平均和。

他把这种趋势平均化的现象写到了自己1886年的论文中。论文的全名叫：Regression towards Mediocrity in Hereditary Stature. 这篇论文当年被发在了大不列颠以及爱尔兰人类研究学院期刊上。我们现今把论文中的这种“回归”现象称为：均值回归或者平庸回归（reversion to the mean/reversion to mediocrity）。背后的意义是说：哪怕单看一组父亲和孩子的身高，两个人的身高可能差异很大，但是从整个人群上来看，父亲和孩子的身高分布应该是很相近的。

C.R.Rao等在Linear Models and Generalizations: Least Squares and Alternatives中解释道 the literature meaning of REGRESSION is " to move in the backward direction"，看以下两个陈述：

S1: model generates data or

S2: data generates model.

Rao认为很明显陈述S1才是对的，因为模型实际上本来就是存在的只不过我们不知道(model exists in nature but is unknown to the experimenter)，

先有模型所以我们知道X就能得到Y：先有模型 -> 有了X就有Y（S1）

而“回归”的意思就是我们通过收集X与Y来确定实际上存在的关系模型：收集X与Y -> 确定模型

（S2）与S1相比，S2就是一个“回到”模型的过程，所以就叫做“regression”。


## 参考文献

- [机器学习 Andrew Ng](https://www.coursera.org/learn/machine-learning/home/welcome)
- [回归分析中的“回归”是什么意思？](https://www.zhihu.com/question/30123729/answer/554278766)