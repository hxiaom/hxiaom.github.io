---
layout: post
title: 【Method】数据标准化/归一化
categories: Analytics
---

## 原理 

在机器学习算法的目标函数(例如SVM的RBF内核或线性模型的l1和l2正则化)，许多学习算法中目标函数的基础都是假设所有的特征都是零均值并且具有同一阶数上的方差。如果某个特征的方差比其他特征大几个数量级，那么它就会在学习算法中占据主导位置，导致学习器并不能像我们说期望的那样，从其他特征中学习。

从经验上说，归一化是让不同维度之间的特征在数值上有一定比较性，可以大大提高分类器的准确性。

对于线性model来说，数据归一化后，最优解的寻优过程明显会变得平缓，更容易正确的收敛到最优解。

## 方法

sklearn的preprocessing提供了可以满足需求的归一化方法：

### StandardScaler

标准化数据通过减去均值然后除以方差（或标准差），这种数据标准化方法经过处理后数据符合标准正态分布，即均值为0，标准差为1，转化函数为：

x =(x - 𝜇)/𝜎

适用于：如果数据的分布本身就服从正态分布，就可以用这个方法。

通常这种方法基本可用于有outlier的情况，但是，在计算方差和均值的时候outliers仍然会影响计算。所以，在出现outliers的情况下可能会出现转换后的数的不同feature分布完全不同的情况。

如下图，经过StandardScaler之后，横坐标与纵坐标的分布出现了很大的差异，这可能是outliers造成的。

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
scaled_df = scaler.fit_transform(data)
```

### MinMaxScaler

将特征缩放至特定区间,将特征缩放到给定的最小值和最大值之间，或者也可以将每个特征的最大绝对值转换至单位大小。这种方法是对原始数据的线性变换，将数据归一到[0,1]中间。转换函数为:

x = (x-min)/(max-min)

这种方法有个缺陷就是当有新数据加入时，可能导致max和min的变化，需要重新定义。

敲黑板，这种方法对于outlier非常敏感，因为outlier影响了max或min值，所以这种方法只适用于数据在一个范围内分布的情况

```python
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
scaled_df = scaler.fit_transform(data)
```

### RobustScaler

如果你的数据包含许多异常值，使用均值和方差缩放可能并不是一个很好的选择。这种情况下，你可以使用 robust_scale 以及 RobustScaler 作为替代品。它们对你的数据的中心和范围使用更有鲁棒性的估计。

This Scaler removes the median（中位数） and scales the data according to the quantile range(四分位距离，也就是说排除了outliers)

```python
from sklearn.preprocessing import RobustScaler
scaler = RobustScaler()
scaled_df = scaler.fit_transform(data)
```

### Normalizer

```python
from sklearn.preprocessing import Normalizer
scaler = Normalizer()
scaled_df = scaler.fit_transform(data)
```

## 参考文献

- [机器学习数据预处理——标准化/归一化方法](https://www.cnblogs.com/bjwu/p/8977141.html)
- [Feature Scaling with scikit-learn](http://benalexkeen.com/feature-scaling-with-scikit-learn/)