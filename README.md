# tech-learning-hub
A collection of technical learnings, hands-on experiments, notes, and practical examples covering software engineering, Java, Spring Boot, microservices, cloud, system design, AI/GenAI, and distributed systems.

## Connection Pooling
Connection pooling is a technique that keeps a reusable set of database connections ready for use instead of opening a new connection for every request. This reduces connection setup overhead, improves latency, and helps systems handle higher traffic more efficiently.

A simple way to think about it:

```text
Clients  -->  App Server  -->  Connection Pool  -->  Database
                 ^                 |
                 |                 +--> reused connections
                 |
                 +--> request/return lifecycle
```

In practice, the app borrows a connection from the pool when needed, uses it briefly, and then returns it so other requests can reuse it. Proper pool sizing and timeout settings are important to avoid bottlenecks or exhausting database resources.
