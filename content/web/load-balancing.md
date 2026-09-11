---
title: Load Balancing
---
Load balancing means distributing traffic across multiple servers.

When many users access a service, one server may become overloaded.
A load balancer solves this by sending requests to different WAS servers.

```text
Client
  ↓
Load Balancer
  ↓
WAS 1 / WAS 2 / WAS 3
```

# Role of a Load Balancer

A load balancer receives client requests and forwards them to an available server.

Example:
* User A → WAS 1
* User B → WAS 2
* User C → WAS 3

# Why Load Balancing Is Used

Load balancing is used to:
* prevent one server from being overloaded
* improve system performance
* keep the service running even if one server fails
* make the system easier to scale

# Common Load Balancing Methods
## Round Robin
Requests are distributed to servers in order.
* 1st request → WAS 1
* 2nd request → WAS 2
* 3rd request → WAS 3
* 4th request → WAS 1

## Least Connections
The request goes to the server with the fewest active connections.
* Choose the WAS with the least number of connections

## IP Hash
The same user is usually sent to the same server based on their IP address.
* Same user → same WAS

# Load Balancing with WebSocket
WebSocket connections stay open after they are created.
Because of this, WebSocket systems need to handle load balancing carefully.

For example:
* User A → WAS 1
* User B → WAS 2

If User A sends a message, only WAS 1 receives it at first.
To deliver the message to User B on WAS 2, the servers need to share messages.
This is where Redis Pub/Sub can be used.

Related: [[Redis]] [[WebSocket]] [[WAS]]