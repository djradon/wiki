
- repo: https://github.com/linkeddata/dokieli
- [[c.software.semantic.authoring]] [[c.software.semantic.activity-pub]]
- url: https://dokie.li
- built_on: [[prdct.solid]] [[prdct.activitypub]]
- written_in: javascript (client-side)
- supports: [[prdct.activitypub]] [[prdct.web-annotations]]

## Features

- A dokieli article is simply an HTML document, so anything you can include in an HTML page you can include in your article. We’re adding new features to the UI to help with this all the time. You can directly embed raw data; in Turtle, [[prdct.JSON-LD]], or TriG (used in Nanopublications).
- 
- Unique identifiers (URIs) are automatically generated for every section of your article to make it easy for others to link and refer to them. You can add identifiers to any concepts you think are important at any level of granularity. Additionally, you can add descriptive markup to any concept or snippet of prose which has an identifier; dokieli generates RDFa markup under the hood so your ideas are exposed as Linked Data for others to query, reuse and visualise.