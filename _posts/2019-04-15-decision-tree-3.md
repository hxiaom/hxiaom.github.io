---
layout: post
title: 【Method】决策树（三）决策树剪枝&CART算法
categories: Analytics
---

## 原理

### 决策树的剪枝

在决策树学习中将已生成的树进行简化的过程称为剪枝（pruning）。

决策树的剪枝往往通过极小化决策树整体的损失函数（loss function）或代价函数（cost function）来实现。设树T的叶结点个数为$$\mid T \mid$$，t是树T的叶结点，该叶结点有$$N_t$$个样本点，其中k类的样本点有$$N_{tk}$$个，k=1,2,...,K，$$H_t(T)$$为叶结点t上的经验熵，$$\alpha \geq 0$$为参数，则决策树学习的损失函数可以定义为

$$C_\alpha(T)=\sum_{t=1}^{\mid T \mid} N_t H_t(T)+\alpha \mid T \mid$$

其中经验熵为

$$H_t(T)=-\sum_k \frac{N_{tk}}{N_t} log \frac{N_{tk}}{N_t}$$

在损失函数中，将

$$C(T) = \sum_{t=1}^{\mid T \mid} N_t H_t(T) = -\sum_{t=1}^{\mid T \mid} \sum_{k=1}^K N_{tk} log \frac{N_{tk}}{N_t}$$

这时有

$$C_\alpha(T)=C(T)+ \alpha \mid T \mid$$

其中，C(T)表示模型对训练数据的预测误差，即模型与训练数据的拟合程度，$$\mid T \mid$$表示模型复杂度，参数$$\alpha \geq 0$$控制两者之间的影响。较大的$$\alpha$$促使选择较简单的模型（树），较小的$$\alpha$$促使选择较复杂的模型（树）。$$\alpha=0$$意味着只考虑模型与训练数据的拟合程度，不考虑模型的复杂度。

剪枝，就是当$$\alpha$$确定时，选择损失函数最小的模型，即损失函数最小的子树。当$$\alpha$$确定时，子树越大，往往与训练数据的拟合越好，但是模型的复杂度就越高；相反，子树越小，模型的复杂度就越低，但是往往与训练数据的拟合不好。损失函数正好表示了对两者的平衡。