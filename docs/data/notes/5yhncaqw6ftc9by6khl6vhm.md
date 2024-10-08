

- [[c.software.agent-framework]]
- https://jacamo-lang.github.io/
- repo: https://sourceforge.net/projects/jacamo/
- written-in: java
- related: [[prdct.cartago]] [[prdct.jason]] [[t.cs.agents.multi-agent-oriented-programming]] [[prdct.moise]]
- docs: https://github.com/jacamo-lang/jacamo/tree/main/doc

## Summary

- agents are programmed in Jason [2] using the AgentSpeak language; organisations are specified in Moise [3] in an XML-based document; and environments are coded in Java using the CArtAgO API


![](/assets/images/2024-04-11-08-45-50.png)

We assume that roles cannot live autonomously: they exist in the system in view of the interaction. We follow the ontological model for roles proposed in [6], and brought inside the object-oriented paradigm in [4], which is characterized by three aspects: (1) Foundation: a role must always be associated with the institution it belongs to and with its player; (2) Definitional dependence: the definition of the role must be given inside the definition of the institution it belongs to; (3) Institutional empowerment: the actions defined for the role in the definition of the institution have access to the state of the institution and of the other roles, thus, they are called powers; instead, the actions that a player must offer for playing a role are called requirements. The agents that will be the role players become able to perform protocol actions, that are powers offered by a specific role and whose execution affect the social state. On the other hand, they need to satisfy the related requirements: specifically, in order to play a role an agent needs to have the capabilities of satisfying the related commitments – capabilities which can be internal of the agent or supplied as powers as well.

## Resources

- [Goal-Oriented Test-Driven Development](https://github.com/jacamo-lang/jacamo/blob/master/doc/tutorials/tdd/readme.adoc)
- [[book.multi-agent-oriented-programming]]
- [[ar.multi-agent-oriented-programming-the-ja-ca-mo-platform]]

## References

- [[ar.programming-jade-and-jason-agents-based-on-social-relationships-using-a-uniform-approach]]
- https://github.com/JaCaMo-EASSS23/slides/blob/main/environment.pdf
- [[ar.knowledge-level-integration-for-jacamo]]