---
layout: post
title: 【Method】Text Similarity
categories: Analytics
---

文本之间的语义相似性在自然语言处理中起到重要作用，广泛应用于检索、文本聚类、文本摘要等场景中，并对最终应用效果起到决定性影响。

文本相似度主要可以分为以下两类：词汇级相似度(Lexical similarity)，语义级相似度(Semantic similarity)

## Lexical Similarity

### Character-based similarity measures

顾名思义，此类方法将文本看作最简单的字符串。而文本之间的相似度通过字符串之间的编辑距离进行衡量。多种衡量方法被提出：

- Longest Common SubString（LSC）：最大公有子串。
- Damerau-Levenshtein：包括插入、删除、替换距离。
- Jaro
- Jaro-Winkler
- Needleman-Wunsch
- Smith-Waterman
- N-gram

### Term-based similarity measures

此类方法将文本看作一系列单词的组合，即为词袋模型。基于该文本表示形式，有如下几种相似度衡量方法：

- Block Distance
- Cosine Similarity
- Dice's coefficient
- Euclidean distance
- Jaccard similarity
- Matching coefficient
- Overlap coefficient

缺点：在很多情况下，相近的语义往往用不同的词汇表示，例如，”开心“与”高兴“。此时基于字符串的比较方法是失效的。在采用此类方法之前，我们应该粗略统计词语出现的频率。如果大多数词语出现频率很低，则大部分情况下基于字符串的比较无法起到作用。

## Semantic Similarity

### Corpus-based similarity measures

此类方法将文本看作单词的组合，但是单词与单词之间的相似度不仅仅依靠字符串的比较。而是进一步依赖单词的上下文来计算单词内涵的语义。使得”开心“与”快乐“两词，虽然在字符串上不相似，但是在语义上相似。

- Normalized Google Distance (NGD)
- Normalized Information Distance (NID)
- Normalized Compression Distance (NCD)
- Hyperspace Analogue to Language (HAL)
- Latent Semantic similarity (LSA)
- Explicit Semantic Analysis (ESA)
- Pointwise Mutual Information - Information Retrieval (PMI-IR)
- Second-order Co-occurrence Pointwise Mutual Information (SCO-PMI)

### Embedding similarity measures

此方法特指使用深度学习的Embedding方法

- Word2Vec
- Glove

### Knowledge-based similarity

此类方法借助外部的知识库例如WordNet进行语义计算。

- Resnik similarity: Information Content (IC) of the most informative subsume
- Vector similarity: A vector is create for each word used in the Word Net glosses from a given corpus and then represents each concept with a vector that is the average of this co-occurrence vector.

## 参考文献

- [Wikipedia: Semantic similarity](https://en.wikipedia.org/wiki/Semantic_similarity)
- [徐健,张智雄,肖卓,邓昭俊.科技术语语义相似度计算方法研究综述[J].现代图书情报技术,2010(Z1):51-57.](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2010&filename=XDTQ2010Z1012&v=MDkyMThNMUZyQ1VSTE9mWStac0Z5RG5VNy9NUFNuZmY3RzRIOUdtcm85RVpvUjhlWDFMdXhZUzdEaDFUM3FUclc=)
- Pradhan N, Gyanchandani M, Wadhvani R. A Review on Text Similarity Technique used in IR and its Application[J]. International Journal of Computer Applications, 2015, 120(9).
- Gomaa W H, Fahmy A A. A survey of text similarity approaches[J]. International Journal of Computer Applications, 2013, 68(13): 13-18.
- Alvarez J E, Bast H. A review of word embedding and document similarity algorithms applied to academic text[D]. University OF Freiburg, 2017.