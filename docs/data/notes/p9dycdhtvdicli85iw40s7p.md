
- url: https://surrealdb.com/
- repo: https://github.com/surrealdb/surrealdb
- written_in: rust
- supports: C#, javascript, rust, python, go, java

## Features

- The power of 10+ products in one unified multi-model database
- live query
- graph support via "edge tables" [[t.cs.graph]]
  - https://surrealdb.com/docs/surrealql/statements/relate
  - Offer bi-directional querying.
  - Offer referential integrity.
  - Allow you to store data alongside the relationship. (edges get their own tables)
- [[prdct.geojson]] geometries
- seems to take care of ORM/OGM mapping natively? https://docs.surrealdb.com/docs/integration/sdks/dotnet/

## Issues

- no RDF support

## References

- https://github.com/Laragear/Surreal/blob/master/README.md
- [In Search of an Efficient Data Structure
for a Temporal-Graph Database](https://surrealdb.com/static/whitepaper.pdf)
- https://surrealdb.com/blog/unlocking-streaming-data-magic-with-surrealdb-live-queries-and-change-feeds