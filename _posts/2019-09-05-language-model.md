---
layout: post
title: 【Method】Word Embedding
categories: Analytics
---

## Definition

A statistical language model is a probability distribution over sequences of words. Given such a sequence, say of length m, it assigns a probability $$P(w_{1},\ldots ,w_{m})$$ to the whole sequence.

As the core component of Natural Language Processing (NLP) system, Language Model (LM) can provide word representation and probability indication of word sequences.

Neural Network Language Models (NNLMs) overcome the curse of dimensionality and improve the performance of tranditional LMs.

## Classic Neural Network Language Models

### One-hot encoder

### Bag-of-word Model

- TF-IDF

### FFNN Language Models

- autoencoder network (GAN)

- Feedforward Neural Network Language Models
- word2vec
    - CBOW
    - Skip-gram



### RNN Language Models

### LSTM-RNN Language Models

## Improved Techniques

### Techniques for Reducing Perplexity

- Character-Aware Models
- Factored Models
- Bidirectional Models
- Caching
- Attention
    - Transformer: first transduction model relying entirely on self-attention to compute representations of its input and output without using sequence-aligned RNNs or convolution.
    - BERT

### Speed-up Techniques on Large Corpora

- Hierarchical Softmax
- Sampling-based Approximations



## Reference

- [Wikipedia: language model](https://en.wikipedia.org/wiki/Language_model)
- Jing, Kun, and Jungang Xu. “A Survey on Neural Network Language Models,” 2012.
- Vaswani, Ashish, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, and Illia Polosukhin. “Attention Is All You Need.” Advances in Neural Information Processing Systems 2017-Decem, no. Nips (2017): 5999–6009.
- [快速解读Google BERT模型 + Word Embedding](https://www.youtube.com/watch?v=Po38Dl-XDd4)