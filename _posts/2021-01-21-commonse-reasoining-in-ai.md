---
layout: post
title: "Digest -- Commonsense reasoning and commonsense knowledge in artificial intelligence"
date: 2021-01-21 10:18:00 -0500
categories: [NLP, MRC]
tags: [survey, commonsense]
comments: true
---

[Commonsense reasoning and commonsense knowledge in artificial intelligence]()  {% cite davis2015commonsense %}.

## Summary
This is a very good review paper on commonsense knowledge published on 2015. It was cited by many commonsense related papers. It covers the importance of commonsense knowledge, the objectives, the difficulties, current(by then) approaches and future directions. The illustraing examples are very helpful to enhance readers' understanding. It is worth special attention to the challenges part.

### Commonsense in Intelligent Tasks
- NLP, especially reference resolution
- CV, such as recognize objects just by context. (recognize a table even we only see the table cloth.)
- Robotics, how to make sensible actions

### Successes in Automated Commonsense Reasoning
- taxonomic reasoning: (1) can use transitivity of categories and inheritance of properties; (2) not hard for straightforward taxonomy structure, but can be problematic when categories overlap; (3) used in Web mining systems.
- temporal reasoning: can be reduced to solving systems of linear inequalities. The main difficulty lies in the interpretation of time (or assigning timestamps to events) in NLP, in that it is context dependent.
- Action and change: has applications similar to recipeQA, and limited success in text.
- Qualitative reasoning: reason the direction of change in interrelated quantities, ex. pressure will go up if the temperature goes up in a closed container.

### Challenges in Automating Commonsense Reasoning
1. lack of a complete understanding of some domains, ex. psychology, biology, social instutions.
2. intuitive situations can be logically complex, ex. understand the behaviour and intention of a character in movies.
3. plausible reasoning. Commonsense reasoning might be stochastic in nature.
4. the long-tail issue: some categories show up rarely.
    - the margin profit for building a KB would then be large.
    - in my opinion, the long-tail issue depends on the abstraction level, which in turn is also difficult to set up consistently in a KB.
5. difficulty to discern the proper level of abstraction
6. projects that requires longer time to see the payoffs are usually less appealing. (What an insight!)

### Objectives
I pick up the ones that I feel are applicable to NLP here.
- Plausible inference
- Range of reasoning modes, such as explanation, gen- eralization, abstraction, analogy, and simulation. This can be a direction to work on.
- Analysis of fundamental domains, such as intuive physics and intuitive psychology.
- Cognitive modeling. Utilize the theories of how human do commonsense reasoning.

### Approaches and Techniques
To build a KB
1. mathematically grounded
2. use KB from informal sources, such as stories and anecdotes
3. Web mining. The issue is severe confusions and inconsistencies.
4. Crowd sourcing. Again, inconsistency.

### Future Directions
1. integrate mathematical logic with Web mining.
2. investigate how facts gathered from Web mining can con- strain the development of mathemati- cally grounded theories.
3. consider other modes of reasoning: analogy, fram-based reasoning, abstraction, conjecture, explanation.
4. use cognitive science.


## Related topics to read
- [ACL 2020 Commonsense Tutorial (T6)](https://homes.cs.washington.edu/~msap/acl2020-commonsense/)
- description logic, an extension of baisc inheritance structure
- [Deep Learning: A Critical Appraisal](https://arxiv.org/pdf/1801.00631.pdf)
- frame-based reasoning
- cognitive science, ex. Think: fast and slow.

## References

<!-- {% cite  %} -->

{% bibliography --cited %}
