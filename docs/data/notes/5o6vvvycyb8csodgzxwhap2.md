

## Issues

- As foaf:homepage is an Inverse Functional Property ([OWL], Section 6.1), different descriptions of a dataset provided in different places on the Web can be automatically connected or “smushed” if they use the same homepage URI. To avoid inappropriate “smushing”, one should not use related pages that are not specifically about the dataset, such as the funding project's homepage or publishing organisation's homepage, as the value of foaf:homepage.