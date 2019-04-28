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

这里，$$x \in R^n$$是输入，$$Y \in {0,1}$$是输出，$$w \in R^n$$和$$b \in R$$是参数，w称为权值向量，b称为偏置，$$w \bullet x$$为w和x的内积。

对于给定的输入实例x，按照上式可以求得$$P(Y=1 \mid x)$$和$$P(Y=0 \mid x)$$，逻辑斯蒂回归比较两个条件概率值的大小，将实例x分到概率值比较大的那一类。

有时为了方便，将权值向量和输入向量加以扩充，仍记作w，x，即$$w=(w^{(1)},w^{(2)},...,w^{(n)},b)^T$$，$$x=(x^{(1)},x^{(2)},...,x^{(n)},1)^T$$。这时，逻辑斯蒂回归模型如下：

$$P(Y=1 \mid x) = \frac{exp(w \bullet x)}{1+exp(w \bullet x)}$$

$$P(Y=0 \mid x) = \frac{1}{1+exp(w \bullet x)}$$

现在考查逻辑斯蒂回归模型的特点。一个事件的几率（odds）是指该事件发生的概率与该事件不发生概率的比值。如果事件发生的概率是p，那么该事件的几率是$$\frac{p}{1-p}$$，该事件的对数几率（log odds）或logit函数是

$$logit(p) = log \frac{p}{1-p}$$

对逻辑斯蒂回归而言，有上式得：

$$log \frac{P(Y=1 \mid x)}{1-P(Y=0 \mid x)} = w \bullet x$$

这就是说，在逻辑斯蒂回归模型中，输出$$Y=1$$的对数几率是输入x的线性函数。或者说，输出$$Y=1$$的对数几率是由输入x的线性函数表示的模型，即逻辑斯蒂回归。

换一个角度看，考虑对输入x进行分类的线性函数$$w \bullet x$$，其值域为实数域。注意，这里$$x \in R^{n+1}, w\in R^{n+1}$$。通过逻辑斯蒂回归模型定义可以将线性函数$$w \bullet x$$转化为概率：

$$P(Y=1 \mid x) = \frac{exp(w \bullet x)}{1+exp(w \bullet x)}$$

这时，线性函数的值越接近正无穷，概率值就越接近1；线性函数的值越接近负无穷，概率值就越接近0。这样的模型就是逻辑斯蒂回归模型。






## 参考文献

- 统计学习方法 李航 第6章