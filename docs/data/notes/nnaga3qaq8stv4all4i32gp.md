
## Triply's take


- Using a hash in IRIs assumes that the IRI without the hash serves the full content of the dataset, containing full descriptions of all hash-containing IRIs with that prefix. This assumption is often true for RDF stored in a single file on a plain file server. This assumption is almost always false for any other data publication system, including all sophisticated data publishing systems that use a column store, relational store, triple store, or document store. This means that an IRI strategy that uses hashes significantly narrows down the possible implementations of a linked data system that publishes data according to that IRI strategy.
- Using a hash in IRIs assumes that the server does not return results in pages (pagination). A server that returns paginated results will often not return the full content of a dataset in the first request. This immediately violates the implementation of the hash component as standardized by HTTP(S), which requires that the full dataset is returned in the first successful reply.
- Using a hash in IRIs assumes that the dataset in which all hash-containing IRIs occur is small enough to be downloaded from a server all at once and fully searched though by an unadvanced client. Specifically, the client cannot be assumed to use advanced forms of indexing to ensure speedy retrieval of the fragment. This means that retrieval may be a little bit faster for small vocabularies that are cached well by the client and whose terms are often looked up by the user, and that retrieval is slower or impossible in all other scenarios.
- Using a hash in IRIs assumes that the small dataset in which all hash-containing IRIs occur will remain small forever. If new hash-containing IRIs are regularly added to the dataset, retrieval times will increase over time.

## Daniel Garijo's take

![[ar.best-practices-for-implementing-fair-vocabularies-and-ontologies-on-the-web#hash-versus-slash-uris]]

## References

- https://www.w3.org/wiki/HashVsSlash
- https://triplydb.com/how-to-model/-/stories/how-to-model-iris
- [[ar.best-practices-for-implementing-fair-vocabularies-and-ontologies-on-the-web]]
- [[ar.best-practice-recipes-for-publishing-rdf-vocabularies]]