---
layout: post
title: 【Method】Transfer Learning
categories: Analytics
---

## Motivation

In certain scenarios, obtaining training data that matches the feature space and predicted data distribution characteristics of the test data can be difficult, expensive or easily outdated.

An assumption of traditional machine learning methodologies is the training data and testing data are taken from the same domain, such that the input feature space and data distribution characteristics are the same. However, in some real-world machine learing scenarios, this assumption does not hold. For example, we sometimes have a classfification task in one domain of interest, but we only have sufficient training data in another domain of interest, where the latter data may be in a different feature space or follow a different data distribution.

The study of Transfer learning is motivated by the fact that people can intelligently apply knowledge learned previously to solve new problems faster or with better solutions.

## Definition

Transfer learning is used to improve a learner from one domain by transferring information from a related domain.

Transfer learning: Given a source domain $$D_S$$ with a corresponding source task $$T_S$$ and a target domain $$D_T$$ with a corresponding task $$T_T$$, transfer learning is the process of improving the target predictive function $$f_T(.)$$ by using the related infromation from $$D_S$$ and $$T_S$$, where $$D_S \neq D_T$$ or $$T_S \neq T_T$$

Given the definition of transfer learning, since $$D_S = {X_S, P(X_S)}$$ and $$D_T = {X_T, P(X_T)}$$, the condition where $$D_S \neq D_T$$ means that $$X_S \neq X_T$$ and/or $$P(X_S) \neq P(X_T)$$. The case where $$X_S \neq X_T$$ with respect to transfer learning is defined as heterogeneous transfer learning. The case where $$X_S = X_T$$ with respect to transfer learning is defined as homogeneous transfer learning.

## Categorization

### Inductive transfer learning.

In the inductive transfer learning setting, the target task is different from the source task, no matter when the source and target domains are the same or not.

### Transductive transfer learning

In the transductive transfer learning setting, the source and target tasks are the same, while the source and target domains are different.

### Unsuperivsed transfer learning

In the unsuperivsed transfer learning setting, similar to inductive transfer learning setting, the target task is different from but related to the source task. However, the unsupervised transfer learning focus on solving unsupervised learning tasks in the target domain, such as clustering, dimensionality reduction, and density estimation. In this case, there are no labeled data available in both source and target domains in training.


## Reference

- Weiss, Karl, Taghi M. Khoshgoftaar, and Ding Ding Wang. A Survey of Transfer Learning. Journal of Big Data. Vol. 3. Springer International Publishing, 2016. https://doi.org/10.1186/s40537-016-0043-6.
- Pan, Sinno Jialin, and Qiang Yang. “A Survey on Transfer Learning.” IEEE Transactions on Knowledge and Data Engineering 22, no. 10 (2010): 1345–59. https://doi.org/10.1109/TKDE.2009.191.