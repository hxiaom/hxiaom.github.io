---
layout: post
title: 【Method】Text Similarity
categories: Analytics
---

文本之间的语义相似性在自然语言处理中起到重要作用，广泛应用于检索、文本聚类、文本摘要等场景中，并对最终应用效果起到决定性影响。

文本相似度主要可以分为以下三类：基于字符串的相似度（String-based similarity）、基于词汇的相似度（Corpus-based similarity）和基于知识的相似度（Knowledge-based similarity）。以下分别介绍这三类相似度计算方法。

## String-based Similarity

缺点：在很多情况下，相近的语义往往用不同的词汇表示，例如，”开心“与”高兴“。此时基于字符串的比较方法是失效的。在采用此类方法之前，我们应该粗略统计词语出现的频率。如果大多数词语出现频率很低，则大部分情况下基于字符串的比较无法起到作用。

## Corpus-based Similarity

## Knowledge-based Similarity

## 参考文献

- [Wikipedia: Semantic similarity](https://en.wikipedia.org/wiki/Semantic_similarity)
- [徐健,张智雄,肖卓,邓昭俊.科技术语语义相似度计算方法研究综述[J].现代图书情报技术,2010(Z1):51-57.](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2010&filename=XDTQ2010Z1012&v=MDkyMThNMUZyQ1VSTE9mWStac0Z5RG5VNy9NUFNuZmY3RzRIOUdtcm85RVpvUjhlWDFMdXhZUzdEaDFUM3FUclc=)
- Pradhan N, Gyanchandani M, Wadhvani R. A Review on Text Similarity Technique used in IR and its Application[J]. International Journal of Computer Applications, 2015, 120(9).
- Gomaa W H, Fahmy A A. A survey of text similarity approaches[J]. International Journal of Computer Applications, 2013, 68(13): 13-18.