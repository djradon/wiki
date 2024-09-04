
- https://github.com/scriptotek/otsrdflib
- dead
- written-in: python

## Features

- classes are ordered alphabetically by their URIs.
  - custom order can be imposed by adding classes to the class_order attribute. For a SKOS vocabulary, for instance, you might want to sort the concept scheme first, followed by the other elements of the vocabulary
- instances of a class are ordered alphabetically by their URIS.
  - custom order can be imposed by defining functions that generate sort keys from the URIs. For instance, you could define a function that returns the numeric last part of an URI to be sorted numerically
- 