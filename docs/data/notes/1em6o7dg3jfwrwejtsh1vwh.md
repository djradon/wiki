
- https://arxiv.org/pdf/2402.00591
- authors: @nicolas-lazzari @stefano-de-giorgis @aldo-gangemi @valentina-presutti

## Abstract

This paper presents sandra, a neuro-symbolic reasoner combining vectorial representations with deductive reasoning. Sandra builds a vector space constrained by an ontology and performs reasoning over it. The geometric nature of the reasoner allows its combination with neural networks, bridging the gap with symbolic knowledge representations. Sandra is based on the Description and Situation (DnS) ontology design pattern, a formalization of frame semantics. Given a set of facts (a situation) it allows to infer all possible perspectives (descriptions) that can provide a plausible interpretation for it, even in presence of incomplete information. We prove that our method is correct with respect to the DnS model. We experiment with two different tasks and their standard benchmarks, demonstrating that, without increasing complexity, sandra (i) outperforms all the baselines (ii) provides interpretability in the classification process, and (iii) allows control over the vector space, which is designed a priori.


## Highlights

![](/assets/images/2024-07-02-12-02-15.png)
- " hence they provide two different perspectives from
which the situation can be interpreted"
  - isn't it more like they provide two different possible descriptions? why 