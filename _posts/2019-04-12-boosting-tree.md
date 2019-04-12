---
layout: post
title: 【Method】Boosting（二）Boosting Tree
categories: Analytics
---

## 原理

提升树（Boosting tree）是以分类树或回归树为基本分类器的提升方法。提升数被认为是统计学习中性能最好的方法之一。

提升方法实际采用加法模型（即基函数的线性组合）与前向分布算法。以决策树为基函数的提升方法称为提升树（boosting tree）。对分类问题决策树是二叉分类树，对回归问题决策树是二叉回归树。提升树模型可以表示为决策树的加法模型：

$$f_M(x) = \sum_{m=1}^M T(x;\theta_m)$$

其中，$$T(x,\theta_m)$$表示决策树；$$\theta_m$$为决策树的参数；M为树的个数。

