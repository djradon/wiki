
- [[c.software.message-bus]]
- url: https://memphis.dev/
- written-in: #go


## Use Cases

-   Async task management
-   Real-time streaming pipelines
-   Data ingestion
-   Cloud Messaging
    -   Services (microservices, service mesh)
    -   Event/Data Streaming (observability, analytics, ML/AI)
-   Queuing
-   N:N communication patterns
-   Ingest Grafana Loki logs at scale

## Features

- Stream Enrichments: serverless-type functions or complete containerized applications that aggregate several stations and streams, decorate and enrich messages from different sources, write complex functions that cannot be achieved via SQL, and manipulate the schema.
- Memphis Functions empower developers and data engineers with the ability to seamlessly process, transform, and enrich incoming events in real-time through a serverless paradigm, all within the familiar AWS Lambda syntax, in an array of programming languages, including but not limited to Go, Python, JavaScript, .NET, Java, and SQL.

### [[c.feature.possible]]

- https://medium.com/memphis-dev/differences-between-nats-io-and-memphis-23ac8bd43d01
  - "Memphis is currently experimenting with creating that ability for consumers to be able to communicate with each other using gRPC or shared channels."
- Data-Level Observability

## Comparison

- [[vs.nats-jetstream-vs-memphis]]

### NATS API compatibility issues

The following Memphis features will not be supported when using NATS SDK:
- Producers/Consumers' observability
- Schemaverse
- Dead-letter station - resend unacked messages


## [[c.license]]

- Memphis is open-sourced and operates under the "Memphis Business Source License 1.0" license Built out of Apache 2.0, the main difference between the licenses is: "You may make use of the Licensed Work (i) only as part of your own product or service, provided it is not a message broker or a message queue product or service; and (ii) provided that you do not use, provide, distribute, or make available the Licensed Work as a Service. A “Service” is a commercial offering, product, hosted, or managed service, that allows third parties (other than your own employees and contractors acting on your behalf) to access and/or use the Licensed Work or a substantial set of the features or functionality of the Licensed Work to third parties as a software-as-a-service, platform-as-a-service, infrastructure-as-a-service or other similar services that compete with Licensor products or services." Please check out License to read the full text.