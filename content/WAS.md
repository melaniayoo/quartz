---
title: WAS (Web Application Server)
---
A WAS is the server that runs the main business logic of a web application.
A Spring Boot backend server can be considered a WAS.

# Role of WAS

A WAS receives requests from clients, processes the logic, communicates with the database, and returns responses.
* Client → WAS → DB
* Client ← WAS ← DB

In a chat system, a WAS can handle:
* creating chat rooms
* saving messages
* retrieving chat history
* managing WebSocket connections
* publishing messages to Redis
* handling read/unread status
* sending notifications

# Web Server vs WAS

A Web Server mainly handles static files, such as:
* HTML
* CSS
* JavaScript
* images

A WAS handles dynamic application logic, such as:
* login
* order lookup
* chat message storage
* database queries
* notifications

Web Server → static files

WAS → business logic

# Why Use Multiple WAS Servers?

If there are many users, one WAS may not be enough to handle all requests.
So multiple WAS servers are used to divide the traffic.

```text
Load Balancer
   ↓
WAS 1
WAS 2
WAS 3
```

This improves performance, availability, and scalability.

Related: [[Load Balancing]] [[WebSocket]]



