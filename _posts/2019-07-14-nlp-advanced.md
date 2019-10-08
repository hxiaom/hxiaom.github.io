---
layout: post
title: 【Method】NLP前沿
categories: Analytics
---

## AutoML

## Pre-trained Model (Transfer learning)

- BERT
- XLNet

## Continual Learning



## Interpretable Machine Learning

- [Google Brain - Been Kim Interpretable Machine Learning](http://people.csail.mit.edu/beenkim/papers/BeenK_FinaleDV_ICML2017_tutorial.pdf) [Paper](https://arxiv.org/abs/1702.08608)
    - Interpretability is NOT about understanding all bits and bytes of the model for all data points (we cannot).
    - It’s about knowing enough for your downstream tasks.
    - Interpretation is the process of giving explanations To Humans
    - Why and When Interpretatioin?
        - Fundamental underspecification in the problem
            - Legal/Ethics: We're legally required to provide an explanation and/or we don't want to discriminate against particular groups
        - What is NOT underspecification?
            - Underspecification is not uncertainty
            - interpretability is not privacy, accountablility, trust, and causality
                - Interpretability can help with them when we cannot formalize these ideas 
                - But once formalized, you may not need interpretability.
    - When we may not want interpretability?
        - No significant consequences or when predictions are all you need. 
        - Sufficiently well-studied problem 
        - Prevent gaming the system - mismatched objectives
    - How can we do this?
        - Before building any model
            - Visualization
            - Exploratory data analysis
        - Building a new model
            - Rule-based, per-feature-based
            - Case-based
            - Sparsity
            - Monotonicity
        - After building a model
            - Sensitivity analysis, gradient-based methods
            - mimic/surrogate models
            - Investigation on hidden layers
    - What is the best interpretability method for me? How can we measure 'good' explantions?
        - You know it when you see it
        - Function-based
            - a variety of synthetic and standard benchmarks e.g, UCI datasets, imagenet
            - How sparse are the features?
            - Does it look reasonable?
            - may not solve real need
        - Application-based
            - Backing up claims. e.g., performance on a cool medical dataset, winning Go games.
            - How much did we improve patient outcomes?
            - Do scientists find the explanations useful?
            - Does providing interpretability assist with a down-stream task, such as increasing fairness, safety, scientific discovery, or productivity? (HCI research)
            - hard to compare work A to B
        - Cognition-based
            - What factor should change to change the outcome?
                - Problem-related Factors
                    1. Global vs. Local
                    2. Time budget
                    3. Severity of underspecification
                - Method-related factors
                    4. Cognitive chunks
                    5. Audience training
            - What are the discriminative features? 
                - Humans capacity as function of factors, Set of factors that carries over well to application.

## Knowledge Graph

- 语义关系
- 自动构建

## Attention model

## Deep Reinforcement Learning

## GANs