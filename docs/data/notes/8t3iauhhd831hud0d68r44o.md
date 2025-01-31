

- related: [[prdct.datalog]] [[prdct.ruleml]] [[prdct.sqwrl]]
- spec: https://www.w3.org/submissions/SWRL/


## Issues

- SWRL shares OWL’s open world assumption so certain types of rules that assume a closed world may be difficult or impossible to write in SWRL

## Solutions

- [[prdct.protege-swrlapi]]

## Resources

- http://dior.ics.muni.cz/~makub/owl/

## References

- https://www.michaeldebellis.com/post/drools-vs-pellet-for-swrl-rules by @michael-debellis
  - the difference between using [[prdct.drools]] and using the [[prdct.pellet]] reasoner and why using Pellet is usually the better option
  - Another excellent use of DROOLS is that it is used to extend SWRL's time built-ins to implement the [[t.cs.time.allens-interval-algebra]]  for reasoning about time.
- https://github.com/protegeproject/swrlapi/wiki/ModellingTime

