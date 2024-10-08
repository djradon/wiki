
- url: 

## Features
- Facets: Supports facets corresponding to rdf-star expressions for annotations and version management.
  - "key value pairs on edges — as an extension to RDF triples."
  - can also be used as weights for edges.
  - "Facets are however not first class citizen in Dgraph like predicates."
- "combines RDF and labeled property graphs, making it ideal for AI-aware large language model editors and data analytics."
- Not a triple store, but uses RDF "for convention"

faq:
  - q: Does Dgraph support GraphQL?
  - a: Dgraph started with the aim to fully support GraphQL. However, as our experience with the language grew, we started hitting the seams. It couldn’t support many of the features required from a language meant to interact with Graph data, and we felt some of the features were unnecessary and complicated. So, we’ve created a simplified and feature rich version of GraphQL. For lack of better name, we’re calling DQL. You can read more about it here.
  - q: When is Dgraph going to support Gremlin?
    a: Dgraph will aim to support Gremlin after v1.0. However, this is not set in stone. If our community wants Gremlin support to interact with other frameworks, like Tinkerpop, we can look into supporting it earlier.



## References

- https://www.bloorresearch.com/technology/graph-databases/
- https://dgraph.io/docs/dql/dql-syntax/dql-rdf/
- https://www.linkedin.com/pulse/dgraph-exploring-json-graph-database-kurt-cagle/