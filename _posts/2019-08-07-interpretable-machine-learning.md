---
layout: post
title: Interpretable Machine Learning
categories: Analytics
---

## What is interpretability?

To interpret means to give or provide the meaning or to explain and present in understandable terms some concepts.

interpretability is defined as the ability to explain or to provide the meaning in understandable terms to a human.

an explanation is an “interface” between humans and a decision maker that is at the same time both an accurate proxy of the decision maker and comprehensible to humans.

Dimensions of interpretability:

- Global and local interpretability
- Time limitation
- Nature of user expertise

an interpretable model can be required either to reveal findings in data that explain the decision, or to explain hwo the black box itself works.

A more applicative nature aimed at explainiing why a certain decision have been returned for a paticular input, or a more theoretical nature aimed at explaining the logic behind the whole obscure model.

## Background

- General Data Protection Regulation (GDPR)

## Why interpretable?

The need for interpretability stems from an incompleteness in the problem formalization, creating a fundamental barrier to optimization and evaluation.

esspecially for downstream task.

- Praticle value. 
    - decision support. 
        - trust and acceptance
        - human understanding
    - accountability
    - safety. unknown mistake. treat cat as dog.
        - deep neural networks have been shown tobe easily fooled into misclassifying input.
    - industrial liability
    - causality
    - transferability
    - informativeness
- ethical value. 
    - open and transparent
    - data contain human biases and prejudices

## Evaluation

- Application-grounded Evaluation: Real humans, real tasks
    - Herman notes that we should be wary of evaluateing interpretable systems using merely human evaluations of interpretability, because human evaluations imply a strong and specific bias towards simpler descriptions. He cautions that reliance on human evaluations can lead researchers to create persuasive systems rather than transparent systems.
- Human-grounded Metrics: Real humans, simplified tasks
- Functionally-grounded Evaluation: No humans, proxy tasks

## Explanator

- Decision Tree or Single Tree
- Decision Rules or Rule Based Explanator
- Linear Regression
- Logistic Regression
- GLM, GAM and more
- Rule Fit
- Features Importance
- Saliency Mask
    - layer-wise relevance propagation
- Sensitivity Analysis
- Partial Dependence Plot
- Prototype Selection
- Activation Maximization


## Interpretable Data for Interpretable Models



## Open the black box problems

- Black box explanation
    - Model explanation
        - Activation maximization
        - Role of Layers
        - Role of Individual Units
        - Role of Representation Vectors
    - Outcome explanation
        - Linear Proxy Models
        - Decision Trees
        - Automatic-Rule Extraction
        - Salience Mapping
    - Model inspection
- Transparent box design
    - Attention Networks
    - Disentabgled Representations
    - Generated Explanations

Explanations of the operation of deep networks have focused on either explaining the processing of the data by a network, or explaining the representation of data inside a network. An explanation fo processing answers "Why does this particular input lead to that particular output?" and is analogous to explaining the execution trace of a program. An explanation about representation answers "What information does the network contain?" and can be compared to explaining the internal data structures of a program.



## Reference

- Guidotti, Riccardo, Anna Monreale, Salvatore Ruggieri, Franco Turini, Fosca Giannotti, and Dino Pedreschi. “A Survey of Methods for Explaining Black Box Models.” ACM Computing Surveys 51, no. 5 (2018): 1–42. https://doi.org/10.1145/3236009.
- Doshi-Velez, Finale, and Been Kim. “Towards A Rigorous Science of Interpretable Machine Learning,” no. Ml (2017): 1–13. http://arxiv.org/abs/1702.08608.
- Lipton, Zachary C. “The Mythos of Model Interpretability.” Communications of the ACM 61, no. 10 (2018): 36–43. https://doi.org/10.1145/3233231.
- 