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

- Normalized Google Distance (NGD)
- Normalized Information Distance (NID)
- Normalized Compression Distance (NCD)
- Latent Semantic similarity (LSA)

### Knowledge-based similarity

- Resnik similarity
- Vector similarity

## 参考文献

- [Wikipedia: Semantic similarity](https://en.wikipedia.org/wiki/Semantic_similarity)
- [徐健,张智雄,肖卓,邓昭俊.科技术语语义相似度计算方法研究综述[J].现代图书情报技术,2010(Z1):51-57.](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2010&filename=XDTQ2010Z1012&v=MDkyMThNMUZyQ1VSTE9mWStac0Z5RG5VNy9NUFNuZmY3RzRIOUdtcm85RVpvUjhlWDFMdXhZUzdEaDFUM3FUclc=)
- Pradhan N, Gyanchandani M, Wadhvani R. A Review on Text Similarity Technique used in IR and its Application[J]. International Journal of Computer Applications, 2015, 120(9).
- Gomaa W H, Fahmy A A. A survey of text similarity approaches[J]. International Journal of Computer Applications, 2013, 68(13): 13-18.