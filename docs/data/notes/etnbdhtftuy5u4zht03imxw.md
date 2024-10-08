
- [[c.software.decisionengine]]
- repo: https://github.com/kiegroup/kogito-runtimes
- url: https://kogito.kie.org/
- related: [[prdct.drools]]

## Features

- ability to use the Java-based declaration of a rule unit to automatically map it with the signature of a REST endpoint

## [[c.solution.related]]

- [[prdct.drools]]
  - "use Drools core features but bring the following improvements:
    - Modular Rules
      - introduces the concept of Rule unit, which is a module for rules and a unit of execution. A rule unit collects a set of rules with the declaration of the type of facts that the rules act on. A rule unit also serves as a unique namespace for each group of rules. A single rule base can contain multiple rule units.
    - Advanced Code generation to create Endpoints from Rules