---
title: WebSocket
---
WebSocket is a technology that allows real-time two-way communication between a client and a server.

Unlike normal HTTP, WebSocket keeps the connection open.
This allows both the client and the server to send messages at any time.

# HTTP vs WebSocket

HTTP is request-response based.
* Client → Request → Server
* Client ← Response ← Server

The server usually responds only when the client sends a request.
WebSocket keeps a continuous connection.
* Client ↔ Server

The server can send messages to the client without waiting for a new request.

# Why WebSocket Is Used

WebSocket is useful for real-time features, such as:
* chat
* live notifications
* live location sharing
* real-time dashboards

In a chat system, users should receive new messages immediately without refreshing the page.
* User A → Server → User B

# WebSocket Flow
1. The client requests a WebSocket connection.
2. The server accepts the connection.
3. The connection stays open.
4. The client and server exchange messages in real time.
5. The connection closes when the user leaves or the network disconnects.

Connect → Keep Connection → Send/Receive Messages → Disconnect

# WebSocket in a Chat System

In a simple chat system:
User A → WebSocket → WAS → WebSocket → User B

However, in a multi-server system, users may be connected to different WAS servers.
* User A → WAS 1
* User B → WAS 2

In that case, Redis Pub/Sub helps deliver messages between servers.

User A
→ WAS 1
→ Redis Pub/Sub
→ WAS 2
→ User B

Related: [[Redis]] 