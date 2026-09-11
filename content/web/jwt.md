---
title: JWT (JSON Web Token)
created: 2026-07-08
---

# JWT (JSON Web Token)

## One-line summary

**JWT is a signed token that proves who the user is.**  
The client sends it with every API request, and the server verifies it before allowing access.

```text
Login successful
→ Server issues JWT
→ Client stores JWT
→ Client sends JWT in Authorization header
→ Server verifies JWT
→ Request is allowed or rejected
```

---

## Why JWT is used

In older session-based login, the server stores login state.

```text
User logs in
→ Server creates session
→ Browser keeps session cookie
→ Server checks session on each request
```

With JWT, the server usually does **not** store the session.

```text
User logs in
→ Server creates JWT
→ Client stores token
→ Client sends token with each request
→ Server verifies token every time
```

This is useful for a multi-server setup.

```text
WAS 1
WAS 2
Redis
DB
```

If users can hit different WAS servers, JWT is convenient because each server can verify the token without relying on one server’s session memory.

---

## JWT structure

A JWT has 3 parts:

```text
Header.Payload.Signature
```

Example shape:

```text
xxxxx.yyyyy.zzzzz
```

### 1. Header

Contains token type and signing algorithm.

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

### 2. Payload

Contains claims, which are pieces of information about the user or token.

Example:

```json
{
  "userId": "admin01",
  "role": "ADMIN",
  "orgCd": "DIVE",
  "exp": 1720000000
}
```

Common claims:

| Claim | Meaning |
|---|---|
| `sub` | Subject, often user ID |
| `role` | User role or authority |
| `orgCd` | Organization/company code |
| `iat` | Issued at time |
| `exp` | Expiration time |

### 3. Signature

Used to check whether the token was changed or forged.

The server signs the token using a secret key or private key.  
If someone changes the payload, the signature check fails.

---

## Important security point

JWT payload is **not automatically encrypted**.

It is usually Base64URL-encoded, which means people can decode and read the payload.  
So do **not** put sensitive data inside JWT.

Avoid putting:

```text
password
resident registration number
credit card number
private personal information
```

Okay to put:

```text
userId
role
orgCd
token expiration time
```

---

Related: [[Spring Security]] [[Backend]]

- make notes about REST API, Spring Security, Spring Boot(controler, service, mapper), MyBatis, PostgreSQL, JDBC, 
- JWT 