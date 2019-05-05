---
layout: post
title: 【Method】深度学习（二）Attention Model
categories: Analytics
---

## 原理

当人在看一样东西的时候，我们当前时刻关注的一定是我们当前正在看的这样东西的某一个地方，换句话说，当我们目光移向别处时，注意力随着目光的移动也在转移，这意味着，当人们注意到某个目标或某个场景时，该目标内部以及该场景内每一处空间位置上的注意力分布是不一样的。

从Attention的作用角度出发，我们就可以从两个角度来分类Attention种类：Spatial Attention空间注意力（图片）和Temporal Attention时间注意力（序列）。更具实际的应用，也可以将Attention分为Soft Attention和Hard Attention。Soft Attention是所有的数据都会注意，都会计算出相应的注意力权值，不会设置筛选条件。Hard Attention会在生成注意力权重后筛选掉一部分不符合条件的注意力，让它的注意力权值为0，即可以理解为不再注意这些不符合条件的部分。

### Encoder-Decoder框架

目前绝大多数文献中出行的AM（Attention Model）模式想附着在Encoder-Decoder框架下的，当然，其实AM模型可以看做一种通用的思想，本身并不依赖于Encoder-Decoder模型，这点需要注意。

## 参考文献

- [Attention Model（注意力模型）](https://zhuanlan.zhihu.com/p/61816483)