---
layout: post
title: 【Method】NLP前沿
categories: Anlaytics
---

## AutoML

## BERT, XLNet

## Interpretable Machine Learning

- [Google Brain - Been Kim Interpretable Machine Learning](http://people.csail.mit.edu/beenkim/papers/BeenK_FinaleDV_ICML2017_tutorial.pdf)
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


## Knowledge Graph