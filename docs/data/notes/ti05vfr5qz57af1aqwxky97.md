
- repo: https://github.com/centrifugal/centrifugo
- written-in: go
- commercial-version: [[prdct.centrifugo.pro]]
- based-on: [[prdct.redis]]
![[prdct.mercure#^ahtfnaeq7g62]]

## Description

- Centrifugo can instantly deliver messages to application online users connected over supported transports (WebSocket, HTTP-streaming, SSE/EventSource, GRPC, SockJS, WebTransport). Centrifugo has the concept of channel subscriptions – so it's a user-facing PUB/SUB server.

## Use Cases

- Chats apps, live comments, multiplayer games, real-time data visualizations, collaborative tools, etc. can all be built on top of a real-time messaging system.

## Features

- Built-in Redis, KeyDB, Tarantool engines, or [[prdct.nats]] broker make it possible to scale connections across different Centrifugo nodes
- while Centrifugo can still transfer JSON data over the wire it now also supports binary Websocket connections with Protobuf message format.
- On backend side Centrifugo provides HTTP and GRPC API to publish data into channels.
- several kinds of channels with different security levels and some options that can be defined in configuration. For example so called private channels where every subscription attempt must be additionally signed.
  - Within channel developer has some useful features like history cache, presence information (information about active channel subscribers), also join and leave notifications when client subscribes on channel (or unsubscribes from it). This is very important to have to build game lobby for example.
- recovery feature: Every channel can optionally keep a stream of Publications and client can recover missed messages upon reconnect providing the sequence number of last seen Publication in channel.
- while Centrifugo server is mostly designed to stream messages in one direction — from server to client — library allows to exchange messages in fully bidirectional way with full control over each client connection.
- supports durability with redis backend

## Comparison

### Centrifugo vs PubNub

- Pubnub's channel groups allow you to group multiple channels under a single identifier. This grouping mechanism enables a client to subscribe to multiple channels via a single group name rather than subscribing to each channel individually. It simplifies client-side logic, especially when the exact channels a client needs to listen to can change dynamically.


![[prdct.mercure#mercure-vs-centrifugo]]


## References

- https://medium.com/@fzambia/how-centrifugo-solves-real-problems-of-real-time-messaging-applications-a15d6b8fc8ac
- https://centrifugal.dev/docs/getting-started/comparisons

Centrifugo

: go