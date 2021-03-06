---
layout: post
title: 【Method】Naive Bayes
categories: Analytics
---

## 原理

朴素贝叶斯（naive Bayes）法是基于贝叶斯定理与特征条件独立假设的分类方法。对于给定的训练数据集，首先基于特征条件独立假设学习输入/输出的联合概率分布；然后基于此模型，对给定的输入x，利用贝叶斯定理求出后验概率最大的输出y。朴素贝叶斯法实现简单，学习与预测的效率都很高，是一种常用的方法。

朴素贝叶斯法与贝叶斯估计（Bayesian estimation）是不同的概念。

设输入空间$$X \subseteq R^n$$为n维向量的集合，输出空间为类标记集合$$Y={c_1,c_2,...,c_k}。输入为特征向量$$x \in X$$，输出为类标记（class label）$$y \in Y$$。X是定义在输入空间X上的随机向量，Y是定义在输出空间Y上的随机变量。$$P(X,Y)$$是X和Y的联合概率分布。训练数据集

$$T={(x_1,y_1), (x_2,y_2),...,(x_N, y_N)}$$

由P(X,Y)独立同分布产生。

朴素贝叶斯法通过训练数据集学习联合概率分布P(X,Y)。具体地，学习以下先验概率分布及条件概率分布。先验概率分布

$$P(Y=c_k),k=1,2,...,K$$

条件概率分布

$$P(X=x \mid Y=c_k) = P(X^{(1)} = x^{(1)},...,X^{(n)}=x^{(n)} \mid Y=c_k), k=1,2,...,K$$于是学习到联合概率分布P(X,Y)。

条件概率分布$$P(X=x \mid Y=c_k)$$有指数级数量的参数，其估计实际是不可行的。事实上，假设$$x^{(j)}$$可取值有$$S_j$$个，$$j=1,2,...,n$$，Y可取值有K个，那么参数个数为$$K \prod_{j=1}^n S_j$$

朴素贝叶斯法对条件概率分布作了条件独立性的假设。由于这是一个较强的假设，朴素贝叶斯法也由此得名。具体地，条件独立假设是

$$\begin{align}
P(X=x \mid Y=c_k) &= P(X^{(1)} = x^{(1)},...,X^{(n)}=x^{(n)} \mid Y=c_k) \\
&= \prod_{j=1}^n P(X^{(j)} = x^{(j)} \mid Y = c_k)\\
\end{align}$$

朴素贝叶斯法实际上学习到生成数据的机制，所以属于生成模型。条件独立假设等于是说用于分类的特征在类确定的条件下都是条件独立的。这一假设使朴素贝叶斯变得简单，但有时会牺牲一定的分类准确率。

朴素贝叶斯法分类时，对给定的输入x，通过学习到的模型计算后验概率分布$$P(Y=c_k \mid X=x)$$，将后验概率最大的类作为x的类输出。后延概率计算根据贝叶斯定理进行：

$$P(Y=c_k \mid X=x) = \frac{P(X=x \mid Y=c_k)P(Y=c_k)}{\sum_k P(X=x \mid Y=c_k)P(Y=c_k)}$$

将条件独立假设代入上式有，

$$P(Y=c_k \mid X=x) = \frac{P(Y=c_k) \prod_j P(X^{(j)} = x^{(j)} \mid Y=c_k)}{\sum_k P(Y=c_k) P(X^{(j)} = x^{(j)} \mid Y=c_k)}$$

这是朴素贝叶斯分类的基本公式，于是，朴素贝叶斯分类器可表示为

$$y=f(x)=arg max_{c_k} \frac{P(Y=c_k) \prod_j P(X^{(j)} = x^{(j)} \mid Y=c_k)}{\sum_k P(Y=c_k) P(X^{(j)} = x^{(j)} \mid Y=c_k)}$$

注意到，上式中分母对所有$$c_k$$都是相同的，所以，

$$y= arg max_{c_k} P(Y=c_k) \prod_j P(X^{(j)} = x^{(j)} \mid Y=c_k)$$

### 后验概率最大化的含义

朴素贝叶斯法将实例分到后验概率最大的类中。这等价于期望风险最小化。

### 极大似然估计

在朴素贝叶斯法中，学习意味着估计$$P(Y=c_k)$$和$$P(X^{(j)}=x^{(j)} \mid Y=c_k)$$。可以应用极大似然估计法估计相应的概率。先验概率$$P(Y=c_k)$$的极大似然估计是

$$P(Y=c_k) = \frac{\sum_{i=1}^N I(y_i=c_K)}{N}, k=1,2,...,K$$

设第j个特征$$x^{(j)}$$可能取值的集合为$${a_{j1}, a_{j2},...,a_{jS_j}}$$，条件概率$$P(X^{(j)}=a_{jl} \mid Y=c_k)$$的极大似然估计是

$$P(X^{(j)} = a_{jl} \mid Y =c_k) = \frac{\sum_{i=1}^N I(x_i^{(j)} = a_{jl},y_i=c_k)}{\sum_{i=1}^N I(y_i=c_k)}$$

$$j=1,2,...,n; l=1,2,...,S_j; k=1,2,...,K$$

其中，$$X_i^{(j)}$$是第i个样本的第j个特征；$$a_{jl}$$是第j个特征可能取的第l个值；I为指示函数。

### 朴素贝叶斯算法

输入：训练数据$$T={(x_1,y_1),(x_2,y_2),...,(x_N,y_N)}$$，其中$$x_i=(x_i^{(1)}, x_i^{(2)},...,x_i^{(n)})^T$$，$$x_i^{(j)}$$是第i个样本的第j个特征，$$x_i^{(j)} \in {a_{j1}, a_{j2}, ..., a_{jS_l}}$$，$$a_{jl}$$是第j个特征可能取的第l个值，$$j=1,2,...,n; l=1,2,...,S_j; k=1,2,...,K$$；实例x；

输出：实例x的分类

(1) 计算先验概率及条件概率

$$P(Y=c_k) = \frac{\sum_{i=1}^N I(y_i=c_K)}{N}, k=1,2,...,K$$

$$P(X^{(j)} = a_{jl} \mid Y =c_k) = \frac{\sum_{i=1}^N I(x_i^{(j)} = a_{jl},y_i=c_k)}{\sum_{i=1}^N I(y_i=c_k)}$$

$$j=1,2,...,n; l=1,2,...,S_j; k=1,2,...,K$$

(2) 对于给定的实例$$x=(x^{(1)}, x^{(2)},...,x^{(n)})^T$$，计算

$$P(Y=c_k) \prod_j P(X^{(j)} = x^{(j)} \mid Y=c_k), k=1,2,...,K$$

(3) 确定实例x的类

$$y = arg max_{c_k} P(Y=c_k) \prod_j P(X^{(j)} = x^{(j)} \mid Y=c_k)$$

### 贝叶斯估计

用极大似然估计可能会出现所要估计的概率值为0的情况。这时会影响到后验概率的计算结果，使分类产生偏差。解决这一问题的方法是采用贝叶斯估计。具体地，条件概率的贝叶斯估计是

$$P_\lambda(X^{(j)} = a_{jl} \mid Y =c_k) = \frac{\sum_{i=1}^N I(x_i^{(j)} = a_{jl},y_i=c_k) + \lambda}{\sum_{i=1}^N I(y_i=c_k) + S_j \lambda}$$

式子中$$\lambda \geq 0$$。等价于在随机变量各个取值的频数上赋予一个正数$$\lambda >0$$。当$$lambda=0$$时，就是极大似然估计。常取$$\lambda=1$$，这时称为拉普拉斯（Laplace smoothing）。显然，对任何$$l=1,2,...,S_j, k=1,2,...,K$$，有

$$P(X^{(j)} = a_{jl} \mid Y =c_k) >0$$

$$\sum_{l=1}^{S_j}P(X^{(j)} = a_{jl} \mid Y =c_k)=1$$

表明贝叶斯估计确为一种概率分布。同样，先验概率的贝叶斯估计是

$$P_\lambda(Y=c_k) = \frac{\sum_{i=1}^N I(y_i=c_k) + \lambda}{N+K\lambda}$$