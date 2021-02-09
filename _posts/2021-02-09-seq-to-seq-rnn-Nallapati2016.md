---
layout: post
title: "Digest -- Abstractive text summarization using sequence-to-sequence RNNs and beyond"
date: 2021-02-09 10:18:00 -0500
categories: [Summarization, Abstractive]
tags: [rnn, seq-to-seq]
comments: true
---

[Abstractive text summarization using sequence-to-sequence RNNs and beyond](https://arxiv.org/abs/1602.06023)  {% cite nallapati2016abstractive %}.

## Summary
This paper uses the sequence-to-sequence RNN framework with attention as the baseline and proposes a model that is specially designed to tackle the unique patterns of abstractive text summarization. Their model is able to model key-words, to capture the hierarchy of sentence-to-word structure, and to deal with OOV words in summarization. Another contribution of this paper is that they transform the CNN/Daily Mail datasets from a question-answering dataset to a dataset for text summarization, which greatly facilitate later research work.

- How did they use model architectures to tackle summarization specific issues?
- What is the training objective?
- What problems remain unsolved?

### Model Architecture
In summarization, there are several challenges:
1. identify the key concepts and key entities
2. model rare or unseen words, ex. the name of a particular product
3. capture the document hierarchy, namely, a document is made up of sentences, which are made up of words.

To tackle the above mentioned challenges, the authors proposed several strategies corresponding.
1. Incorporate the linguistic features in the embedding vectors, such as NER, TF, and IDF.
2. Use Generator-Pointer network, where generator is used for generating words in the vocabulary while pointer intends to copy words directly from the source text. This design is further improved later by  {% cite see2017get %}.
3. Use hierarchical attention to model the hierarchy of documents.

The main idea of the three strategies is fully illustrated in the diagrams as below.

![feature-rich-encoder]({{site.baseurl}}/assets/img/posts/20210209-abstract-fig1.png)

![generator-pointer]({{site.baseurl}}/assets/img/posts/20210209-abstract-fig2.png)

![hierarchy]({{site.baseurl}}/assets/img/posts/20210209-abstract-fig3.png)

### Training Objective
The training objective is the conditonal log-likelihood plus additional regularization penalties.

![objective]({{site.baseurl}}/assets/img/posts/20210209-abstract-objective.png)

where y and x are the summary and document words respectively, and $g_i$ is an indicator function that is set to 0 whenever the word at position $i$ in the summary is OOV w.r.t. the decoder vocabulary.

### Unsolved problems


<!-- ## Related topics to read
-  -->

## References

<!-- {% cite  %} -->

{% bibliography --cited %}
