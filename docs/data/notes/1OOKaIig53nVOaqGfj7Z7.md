
## Description

- @chatgpt.4o: "a predicate is the position in the triple, and a property is the resource that occupies that position."
- properties: predicates or attributes
  - but it's a fuzzy line. [[book.demystifying-owl-for-the-enterprise]] says dates are attributes, like "created", because it's a literal... but you can (and [[gd]] does) represent dates and times as entities
- one of the biggest mistake of RDF: predicates are ??
  - 2021-11-07 don't remember what I was going to say here, but likely something about how predicates supposedly express properties, when really they just express predicates (i.e., part of a property)
- "In RDF, a predicate is something that is in the second position of a triple. RDF have no way of referring to positions in triples, so you cannot use a property between two predicates. What is certainly meant by the OP is "can we use owl:sameAs between two properties". Properties can be identified with IRIs, IRIs can occur anywhere in a triple, subject and object can be related by way of a predicate, and any IRI are allowed in any position of a triple. So, syntactically speaking, it is allowed to relate two properties with owl:sameAs."


- [[p.isRelated]] [[vs.property-graphs-vs-semantic-graphs]]

## thoughts

- 2021-11-07 : the predicate kinda corresponds to the "attribute" part of "attribute-value pairs"; property feels like it should correspond to a concrete attribute-value pair, not just a predicate. 
- some classes have default "getter/setter" verbs, that's kinda properties. so I can see "The predicate indicates a binary relation, also known as a property."
- "The predicate indicates a binary relation, also known as a property."
  - this is the kinda opposing what I've been thinking: the relation is the property, as opposed to the resource


## references

- https://www.mdpi.com/2073-8994/12/1/84/htm
- https://www.wikidata.org/wiki/Wikidata:Relation_between_properties_in_RDF_and_in_Wikidat
- [[ar.maverickphilosopher.predicates-and-properties]]
- https://www.reddit.com/r/askphilosophy/comments/2z17hx/the_difference_between_a_property_and_a_predicate/