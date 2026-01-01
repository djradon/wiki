
- [[c.Software.messaging.middleware]]
- written-in: kotlin
- supports: java
- requires: 
  - [[prdct.pulsar]] 
  - [[prdct.redis]] or [[prdct.MySQL]]

## similar

- [[prdct.infinitic]]
- [[prdct.catalyst]]
- [[prdct.zeebe]]
- [[prdct.temporal]]
- [[prdct.conductor]]
- [[prdct.kestra]]
- [[prdct.iwf]] 

## Terms

- **Services** primarily defined by their interfaces and are invoked using event-based RPC
- **Tasks** a method within a service class. It can be anything from a database operation, an API call, to any complex action specific to your domain.
- 


## Orchestration

![[t.cs.sd.architecture.orchestration#^21ydosqb6dt1]]

## References

- [[ar.medium.the-way-we-are-building-event-driven-applications-is-misguided]]