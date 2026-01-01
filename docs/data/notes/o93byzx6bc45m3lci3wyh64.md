
- repo: https://github.com/jbogard/MediatR
- written-in: [[t.cs.languages.c-sharp]]

## Cons

- **You want event/notification handlers to be run in independently in isolation.** This is where out-of-process messaging comes in. In this case, you might want to look at  [[prdct.nservicebus]], [Brighter](https://www.goparamore.io/), [[prdct.masstransit]], [[prdct.rebus]].
  - https://codeopinion.com/why-use-mediatr-3-reasons-why-and-1-reason-not/