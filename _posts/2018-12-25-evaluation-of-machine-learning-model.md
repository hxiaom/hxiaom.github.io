---
layout: post
title: Evaluation of Machine Learning Model
categories: Analytics
---

* TOC
{:toc}

## 1. Classification Metrics

所有衡量方式结果好坏都取决于具体的问题，同该类问题最前沿方法进行比较。

### 1.1 Precision

直观理解：希望找出的都是对的

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/5b7d5cd5010efe2ef51e7731f2124a2156830fbe)

经验值：

### 1.2 Recall

直观理解：希望对的尽可能的被找出

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/43a4548e95fde15433d8e3cd3c80ced433f54abe)

经验值：


### 1.3 F1-score

直观理解：综合Precision和Recall两个目标

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/057ffc6b4fa80dc1c0e1f2f1f6b598c38cdd7c23)


## 2. Regression Metrics

### 2.1 ME (Mean Error)

直观理解：平均误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/ecf876e1201ae41e5924cc11bcc6d557e454fc4f)

### 2.2 MAE (Mean absolute error)

直观理解：平均绝对误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/3ef87b78a9af65e308cf4aa9acf6f203efbdeded)

### 2.3 MPE (Mean percentage error)

直观理解：平均百分比误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/f2e99f3dac6ee7a098fdb342b5cbe8273d35f01d)

### 2.4 MAPE (Mean absolute percentage error)

直观理解：平均绝对百分比误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/4cf2158513b0345211300fe585cc88a05488b451)

### 2.5 sMAPE (Symmetric mean absolute percentage error)

直观理解：对称平均绝对百分比误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e5eab10e691bead6d1d175a370546db3f4371507)


### 2.6 MSE (Mean squared error)

直观理解：均方误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e258221518869aa1c6561bb75b99476c4734108e)

### 2.7 RMSE (Root Mean Square Error)

直观理解：均方根误差

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/eeb88fa0f90448e9d1a67cd7a70164f674aeb300)
