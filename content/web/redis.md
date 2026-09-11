---
title: Redis
---
Redis is an in-memory data store.
It stores data in memory, so it is much faster than a traditional disk-based database.

Redis is commonly used for:
* caching
* session storage
* real-time ranking
* message brokering
* Pub/Sub messaging

# Key Idea

Redis stores data in a key-value format.
* key → value

Example:
* user:1 → Melania
* chatRoom:100 → active

# Redis Pub/Sub

Redis Pub/Sub is a real-time messaging feature.

Pub/Sub stands for:
* Publisher: sends a message
* Channel: the path where the message is sent
* Subscriber: receives messages from a channel

Publisher → Redis Channel → Subscribers

# Why Redis Pub/Sub Is Used in Chat

In a chat system, users may be connected to different WAS servers.

* User A → WAS 1
* User B → WAS 2

If User A sends a message, WAS 1 receives it first.
However, User B is connected to WAS 2, not WAS 1.

So WAS 1 publishes the message to Redis.
Then all WAS servers subscribed to that Redis channel receive the message.

User A → WAS 1 → Redis Pub/Sub → WAS 2 → User B

This allows users to receive messages no matter which WAS server they are connected to.

# Important Point

Redis Pub/Sub does not permanently store messages.
It only delivers messages to subscribers that are currently connected.
Therefore, chat messages should still be saved in a database.

* DB → stores chat history
* Redis Pub/Sub → delivers real-time messages between servers

Related: [[WebSocket]] [[WAS]]