---
layout: post
title: 【Method】Logistic regression
categoreis: Analytics
---

## 原理

逻辑斯蒂回归（logistic regression）是统计学习中的经典分类方法。

### 逻辑斯蒂分布

逻辑斯蒂分布（logistic distribution）设X是连续随机变量，X服从逻辑斯蒂分布是指X具有下列分布函数和密度函数：

$$F(x)=P(X \leq x) = \frac{1}{1+e^{-(x-\mu)/ \gamma}}$$

$$f(x)=F'(x)=\frac{e^{-(x-\mu)/ \gamma}}{\gamma(1+e^{-(x-\mu)/ \gamma})^2}$$

逻辑斯蒂分布的密度函数法f(x)和分布函数F(x)的图形如下图所示。分布函数属于逻辑斯蒂函数，其图形是一条S形曲线（sigmoid curve）。该曲线以点$$(\mu, \frac{1}{2})$$为中心对称，即满足

$$F(-x+\mu)-\frac{1}{2} = -F(x+\mu)+\frac{1}{2}$$

![](/img/2019-04-28-logistic-regression.gif)

曲线在中心附近增长速度较快，在两端增长速度较慢。形状参数$$\gamma$$的值越小，曲线在中心附近增长得越快。

### 二项逻辑斯蒂回归模型

二项逻辑斯蒂回归模型（binomial logistic regression model）是一种分类模型，由条件概率分布$$P(Y \mid X)$$表示，形式为参数化的逻辑斯蒂分布。这里，随机变量X取值为实数，随机变量Y取值为1或0。我们通过监督学习的方法来估计模型参数。

逻辑斯蒂回归模型：二项逻辑斯蒂回归模型是如下的条件概率分布：

$$P(Y=1 \mid x) = \frac{exp(w \bullet x + b)}{1+exp(w \bullet x + b)}$$

$$P(Y=0 \mid x) = \frac{1}{1+exp(w \bullet x + b)}$$





## 参考文献

- 统计学习方法 李航 第6章