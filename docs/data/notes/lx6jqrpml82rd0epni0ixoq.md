
- url: https://nemo-ufes.github.io/gufo/
- repo: https://github.com/nemo-ufes/gufo/
- related: [[prdct.ufo-protege-plugin]] [[prdct.ontouml-vp-plugin]]

## Features

- "A key feature of UFO (and hence, gUFO) is that it includes two taxonomies: one with classes whose instances are individuals (classes in this taxonomy include gufo:Object, gufo:Event) and another with classes whose instances are types (classes in this taxonomy include gufo:Kind, gufo:Phase, gufo:Category)."
- UFO distinguishes Endurant Types into Substantial Types and Moment
Types.

## Classes

- Individual
  - AbstractIndividual: evil, chaos
    - Instant
    - QualityValue 
      - Use this class only for quality values (qualia) that are to be reified in the A-box and associated with a gufo:ConcreteIndividual through the object property gufo:hasReifiedQualityValue. Otherwise, use the gufo:hasQualityValue data property and a literal to determine the quality value.
        - i.e., it's a type for quality values that are part
  - ConcreteIndividual
    - Endurant
      - Aspect
        - ExtrinsicAspect
          - ExtrinsicMode
          - Relator
        - IntrinsicAspect
          - IntrinsicMode
          - Quality
      - Object: e.g. Gunaar, Shadow Keep
        - Collection: 
          - FixedCollection: Gunaar and Tserro together
          - VariableCollection: The Shadows. "If various roles for the parts of a fleet were envisioned (such as "cargo airplane", "passenger airplane"), then a fleet would be best understood as a gufo:FunctionalComplex."
        - FunctionalComplex: complicated to differentiate from VariableCollection
        - Quantity
    - Event
      - Participation "John's participation in the meeting encompasses all events that are part of the meeting and that depend solely on him"
    - Situation
      - QualityValueAttributionSituation
      - TemporaryConstitutionSituation
      - TemporaryInstantiationSituation
      - TemporaryParthoodSituation
      - TemporaryRelationshipSituation
- Type
  - AbstractIndividualType
  - ConcreteIndividualType
    - EndurantType
      - NonRigidType
        - Phase
        - PhaseMixin
        - Role
        - RoleMixin
      - SemiRigidType
        - Mixin
      - NonSortal
        - Category "Non-sortals do not provide a uniform principle of identity for their instances; instead, they just classify things that share common properties but which obey different principles of identity."
        - Mixin "A gufo:EndurantType that is both non-sortal and semi-rigid. As a semi-rigid type, it applies necessarily to some of its instances and contingently to some others. As a non-sortal, it captures properties shared by instances of different kinds. For example, the type "FemaleAnimal" may be considered a gufo:Mixin as it applies necessarily to animals of certain species, e.g., lions and sharks, while it applies contingently to animals of other species such as clownfish and mushroom corals (which may change sex given certain conditions)."
        - PhaseMixin
        - RoleMixin
      - RigidType
        - Category
        - Kind
        - Subkind
      - Sortal
        - Kind
        - Phase
        - Role
        - SubKind
    - EventType
    - SituationType
  - RelationType
    - ComparativeRelationshipType
    - MaterialRelationshipType

## Resources

- https://github.com/nemo-ufes/gufo/blob/master/docs/overview.md