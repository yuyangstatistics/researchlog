---
layout: post
title: "Digest -- Deep Learning: A Critical Appraisal"
date: 2021-01-22 14:04:00 -0500
categories: [DL]
tags: [critics]
comments: true
---

[Deep Learning: A Critical Appraisal](https://arxiv.org/abs/1801.00631)  {% cite marcus2018deep %}.

## Summary
Gary Marcus is a professor in Psychology and Neural Science at New York University. He is also the author of {% cite davis2015commonsense %}. In this paper, he reflected on the current issues of Deep Learning and emphasized that DL is not a universal tool and we need to know what it is and is not and good for. 

### Limits on the scope of deep learning

- **Generalization** comes in two flavors, interpolation between known examples, and extrapolation, which requires going beyond a space of known training examples.

- Deep learning works best for classification problems with sufficient data samples in stable domains where examples are mapped in a constant way onto a limited set of categories.
- Deep learning currently lacks a mechanism for learning abstractions through explicit, verbal definition.
- Many adversarial studies show that deep learning solutions are often extremely superficial.
- Language has a hierarchical structure, which deep learning so far has no natural way to deal with. This is a good point and might be helpful to model design. And a related question: can PCE learn the hierarchical structure?
- Other issues: Open-ended inference, transparency, integration with prior knowledge, causation vs. correlation (even statistical techniques have limits in this.), an assumption of stable domains, not credible and no sound guarantees about performance.


### Future Direction
Integrate symbolic systems, which excels at inference and abstraction, with deep learning, which excels at perceptual classification.

 
## Related topics to read
- symbolic systems, representations of abstract relationships.
- convolution, translational invariance
- hierarchical structure in natural language. A paper showing the incapability of RNN: {% cite lake2018generalization %}.

## References

<!-- {% cite  %} -->

{% bibliography --cited %}
