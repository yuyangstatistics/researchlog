---
layout: post
title: "Digest -- Recent advances in natural language inference: A survey of benchmarks, resources, and approaches"
date: 2021-01-20 16:34:00 -0500
categories: [NLP, MRC]
tags: [paper, mrc]
comments: true
---

[Recent advances in natural language inference: A survey of benchmarks, resources, and approaches](https://arxiv.org/abs/1904.01172)  {% cite storks2019recent %}.

## Summary
This is a really good review paper in NLI. It mainly covers language understanding tasks and benchmarks where we need to **use some external knowledge or advanced reasoning beyond linguistic context**. The idea that we can better guide researchers to focus on truly understand the reasoning by designing smarter benchmarks is inspiring. This paper gives an overview of existing benchmarks and what problems they are trying to solve, as well as existing knowledge resources and inference approaches. It also provides examples from the benchmark datasets, which can give beginners some basic idea. It can serve as a pretty good reference for resources looking up. Several issues raised in this paper are worth attention, such as the unexplainability of recent approaches and the statistical biases found in benchmark datasets.

### Benchmarks and Tasks
Five major tasks require external knowledge and complex reasoning: reference resolution, question answering, textual entailment, plausible inference, and intuitive psychology. It seems to me that the difference between textual entailment and plausible inference is that text entailment judges the correctness of hypothese and focuses on reasoning, while plausible inference finds the event that is the most likely to happen according to commonse knowledge. 

The authors also call attention for the superficial correlation biases in the datasets, for example, the gender bias. Mutual information method {% cite gururangan2018annotation %} and adversarial filtering process {% cite zellers2018swag %} may be helpful for such biases. 

### Knowledge Resources
Linguistic knowledge includes annotated corpora, frame semantics resources, lexical resources, and pre-trained semantic vectors.

Common and commonsense knowledge resources are mostly in the form of knowledge base and knowledge graph. To clarify, common knowledge refers to well-known facts about the world that are often explicitly stated, while commonsense knowledge, on the other hand, is considered obvious to most humans, and not likely to be explicitly stated {% cite cambria2011isanette %}.

### Learning and Inference Approaches
Three main neural approaches are brought up: attention mechanism, memory augmentation, and contextual models and representations. 

It points out that attention mechanism works well mainly on capturing the alignment between an input and an output, and capturing long-term dependencies. One thing to note is some RNN models with attention will perform worse since there is no such alignment. This reminds us to keep in mind what a structure is actually learning before stacking them altogether. 

Memory augmentation methods, such as memory networks, are new to me and requires further reading.

One interesting point about using external knowledge is mentioned: {% cite mihaylov2018can %} find that their adding of facts from ConceptNet causes distraction which reduces performance, suggesting that the technique for selecting the appropriate relations is important to reduce distraction. 

### Future Directions
The directions are mostly for designing datasets, still, I get some motivations.

Despite the good performance of current models, we don't know whether or not they are actually performing reasoning. The authors think the benchmarks should differentiate between types of reasoning and take that into evaluations. 

> A competence-centric evaluation, while important for pushing the state of the art, can also lead to a less productive path if not treated carefully.

The authors suggest that we put more attention on a good understanding of model behaviors (anything insightful? what is the model actually learning?), computational efficiency, and generalization ability (inference on new tasks with minimal training). 

## Questions
1. How to use common or commonsense knowledge in creating a benchmark dataset?
2. What are the existing types of reasoning?

## Related topics to read
- mutual information
- ConceptNet
- BERT is indeed learning and exploiting statistical biases in certain benchmarks {% cite niven2019probing %} .
- distributional representation of words {% cite ferrone2020symbolic %}.
- types of reasoning {% cite davis2015commonsense %}


## References

<!-- {% cite  %} -->

{% bibliography --cited %}
