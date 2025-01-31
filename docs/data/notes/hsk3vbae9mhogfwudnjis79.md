
## Description

- RDFa is a way to embed triples into an HTML document. It can be confusing for beginners, but some software tools generate valid RDFa which is fine, but don't try to create it by hand until you get some experience!

- To decode RDFa in an HTML page, just put the URL into http://graphite.ecs.soton.ac.uk/browser/ 

## Examples

```html
<div about="/alice/posts/trouble_with_bob">
    <h2 property="dc:title">The trouble with Bob</h2>
    <h3 property="dc:creator">Alice</h3>
    ...
</div>
```

## Questions

- is <a href> the only way to specify a object resource

```html
<div about="http://dbpedia.org/resource/Albert_Einstein">
  <span property="foaf:name">Albert Einstein</span>
  <span property="dbp:dateOfBirth" datatype="xsd:date">1879-03-14</span>
  <div rel="dbp:birthPlace" resource="http://dbpedia.org/resource/German_Empire">
    <span property="dbp:conventionalLongName">the German Empire</span>
    <span rel="dbp-owl:capital" resource="http://dbpedia.org/resource/Berlin" />
  </div>
</div>
```

## Cons

-   adding inline semantic markup to existing web pages can be tricky and time-consuming when it is necessary to understand the existing page structure and the hierarchical nesting of various `<div>` and `<span>` elements - and care must be taken to check that the RDF triples that can be extracted from the page are as intended, without mis-connected nodes or dangling nodes. Sometimes it is necessary to re-assert the `Subject` of a set of RDF triples using the about attribute.
-   inline semantic markup can break very easily if further HTML edits are made to a semantically annotated page, without involving the semantic annotator in the discussion. A simple example of this is that the person adding the inline semantic annotations might use an attribute such as `property="schema:image"` or `itemprop="schema:image"` to indicate that a specific image on the page is a depiction of the `Subject`. Now if someone else wraps an `<a href>` hyperlink around the annotated image, then the image is then considered to be a `schema:image` property of the thing identified by the URL of the new hyperlink, rather than the `schema:image` of the original `Subject`. The original triple can be restored by inserting an `about` attribute within the `<img>` image tag - but it seems undesirable that this kind of defensive coding must be used merely to ensure that another web editor cannot easily break the RDF triples that were originally intended to be present.
  - t.2024.10.03.21 you could get around this issue but not saying anything about any other resources
  - ensure machine-only modification could help too. 
  - compare "single block markup using [[prdct.JSON-LD]]": 
    - the single block of JSON-LD markup is decoupled from the human-readable HTML markup appearing in the <body> of the page, which means that if changes are made to the structure of the <body> section, there is much less risk of breaking or misconnecting the collection of RDF triples that can be extracted from the page.

## Libriaries

- [[prdct.rdfa-streaming-parser-js]]

## Resources

- https://www.w3.org/2006/07/SWD/RDFa/primer/

## References

- [[ar.linked-data-basics-for-techies]]