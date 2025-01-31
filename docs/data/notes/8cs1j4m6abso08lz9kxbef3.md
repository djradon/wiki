
url: https://cloudevents.io/

- supported-by: [[prdct.openfaas]] [[prdct.triggermesh]] [[prdct.kafka]] [[prdct.quarkus]]
- [[p.supports]] 
  - [XML](https://github.com/cloudevents/spec/blob/main/cloudevents/working-drafts/xml-format.md)
  - [JSON](https://github.com/cloudevents/spec/blob/main/cloudevents/formats/json-format.md)

## [[p.hadDefinition]]


## Specifications

- https://github.com/cloudevents/spec/blob/main/cloudevents/formats/json-format.md
- https://github.com/cloudevents/spec/blob/main/cloudevents/working-drafts/xml-format.md

### https://quarkus.io/blog/kafka-cloud-events/

- Events can be used to implement event sourcing, communicate facts, trigger out-of-band processing, or send notifications. Events become an essential piece of any system.


## Resources

- https://developers.redhat.com/blog/2021/03/09/an-introduction-to-javascript-sdk-for-cloudevents
  - "Currently, there are two event formats: Binary, which is the preferred format, and structured. Binary is recommended because it is additive. That is, the binary format only adds some headers to the HTTP request. If there is a middleware that doesn’t understand CloudEvents, it won’t break anything, but if that system is updated to support CloudEvents, it starts working."  