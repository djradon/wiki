
- url: https://graphbrain.net/
- written-in: #python
- #aka "An OpenCog that works"
- 

![](/assets/images/2023-09-23-13-09-46.png)

## Features

- provides an actual database system that allows for persistent storage and manipulation of semantic hypergraphs.
- "Taxonomies can be built using type-of relations between hyperedges, with the help of the special predicate type_of/P/..", i.e., typeof = instanceOf

## Cons

- single backend implementation, that is based on LevelDB (a very efficient sorted key-value store that is stored in a local directory). Hypergraphs stored in this format can only be accessed by one process/thread at a time.

## Highlights

- Graphbrain is built around a unifying concept: the [[Semantic Hypergraph (SH)|t.cs.graph.semantic-hypergraph]], which makes it possible to represent a natural language sentence such as “Einstein first published the theory of relativity in 1905” as an ordered, recursive hyperlink
  - http://graphbrain.net/manual/notation.html 

## Resources

- [[ar.linking-graph-databases-and-semantic-web-for-reasoning-in-library-domains]]