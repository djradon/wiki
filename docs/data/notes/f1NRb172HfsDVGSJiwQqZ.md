
- repo: https://github.com/terminusdb/terminusdb
- written_in: prolog
- [[p.builtWith]] [[prdct.rdf]] but evolved into a document graph db
- [[p.similarTo]]
  - [[prdct.typedb]] but more triple/semantic-webby
  - [[prdct.fluree]] 
- related: [[prdct.dfrnt]]
- supports: [[prdct.graphql]] [[prdct.woql]]
- client_support: 
  - javascript: TerminusDB JavaScript client library can be used either as a Node.js package or as a script that runs in the browser.
  - python

## Features

-   The [db schema](https://terminusdb.com/docs/schema) is defined in [[prdct.owl]]
-   Most operation occurs in-memory, but is persisted in a forward-only log (similar to git)
-   This “git-for-data” approach allows branch, merge, squash, rollback, diff, blame, and time-travel, etc.
-   [[prdct.json-ld]] is interchange format, suitable for web, but editing in turtle is possible
-   You can query any part of a graph and retrieve as a JSON-LD document (serialized to the depth you want)
-   Query format is also JSON-LD, making queries composable and you can store/query queries like normal data
-   Client-side the queries are created using fluent JS (for web devs) and/or Ruby (for data scientists)
-   Provides transaction processing and updates using immutable database data structures
-   Through this immutability the db regains full ACID support
-   "TerminusDB can read RDF files with little difficulty. However, to get the value of TerminusDB you really need a schema. So first stop is really trying to figure out what we might need to massage about the RDF to get it into an easily schemable form."

## Issues

- maybe doesn't export JSON-LD but https://github.com/dfrnt-com/tuscli might work
- WOQL need rework
  - temporal not fully supported in query
    - "TerminusDB has valid time as data in the database, and system or transaction time as a data in a commit graph.
The commit graph keeps track of the time at which facts are known, creates a structure called a "commit" and connects it to the parent commit.
This allows us to do things like present object change histories which are based on the transaction/system time of a change.
Our query language works on the commit graph (both WOQL and GraphQL) and the database itself so its possible to look at these two time dimensions independently.
We also have APIs to expose object history etc. and we hope to include these in our query language so that you can easily ask temporal questions. At the minute the temporal questions usually are somewhat simple that we are able to ask (when did this object change, what was its change history) etc. rather than the complete bitemporal query which is theoretically possible."

## Resources

- https://medium.com/terminusdb/6-reasons-why-terminusdb-is-the-right-toolkit-to-build-collaborative-apps-6fb9ae96ff4
- https://terminusdb.com/blog/loading-data-in-turtle-rdf-format-to-terminusdb/
- https://forum.solidproject.org/t/terminusdb-a-delightful-database-for-linked-data/3140
  - mentioned: https://news.ycombinator.com/item?id=22867767
- https://terminusdb.com/blog/graphql-query/
- [[ar.terminusdb.the-semantic-web-is-dead]]