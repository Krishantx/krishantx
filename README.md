<!-- heya. you found my corner of github. -->

### Hey,

I build backend systems, occasionally break distributed ones, and then spend an unreasonable amount of time figuring out **why**.

Mostly **Go, Java, Spring Boot, gRPC, Redis and PostgreSQL**.

I'm especially interested in the stuff that happens after `"it works on my machine"` — concurrency, distributed systems, failure handling, observability, performance, and what happens when one innocent-looking service suddenly has five friends and a network between them.

![me explaining why this is definitely not a race condition](https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif)

---

### 🕸️ Currently fighting: [raft-based-distributed-key-value-store](https://github.com/Krishantx/raft-based-distributed-key-value-store)

I'm building a distributed key-value store in **Go + gRPC**, with the Raft consensus algorithm implemented from scratch.

No Hashicorp Raft. No consensus library doing the scary bits for me.

Five independent nodes elect a leader, exchange heartbeats, replicate logs, survive elections, and eventually agree that `"foo" = "bar"` — which turns out to require a suspicious amount of engineering.

There's also a `raft-aware-proxy` sitting in front of the cluster so clients don't have to care which node currently wears the crown.

**Currently working on:** log replication, commit semantics, leader failure, and the various creative ways distributed systems find to humble me.

Still a work in progress. It earns the résumé spot when the tests say it does.

---

### ⚙️ The one that survived the tests: [microservice-gateway-platform](https://github.com/Krishantx/microservice-gateway-platform)

A microservices playground that got slightly out of hand.

It started as *"I'll build an API gateway"* and somehow became:

**Spring Boot 3.5 · Java 21 · Eureka · Redis · PostgreSQL · Docker · OpenTelemetry · k6**

Under the hood:

- custom API gateway + filter chain
- JWT authentication
- Eureka service discovery
- token-bucket rate limiting
- Redis hot path with PostgreSQL persistence
- correlation-ID tracing
- YAML-based routing
- containerized services
- CI + automated tests

Then I pointed k6 at it until I had numbers I could actually defend:

**~269 authenticated req/s · p95 94 ms · 0 errors**

And because `"trust me bro"` isn't a testing strategy:

**69 tests · ~99% line coverage · ~98% branch coverage**

[![CI](https://github.com/Krishantx/microservice-gateway-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/Krishantx/microservice-gateway-platform/actions)

---

### 🧪 Other experiments

I have a habit of turning things I want to understand into projects.

**[Rate Limiter as a Service](https://github.com/Krishantx/Rate-Limiter-as-a-Service)**  
Token-bucket rate limiting backed by Redis + PostgreSQL, configurable per client and endpoint.

**Distributed Task Queue**  
PostgreSQL-backed workers using `FOR UPDATE SKIP LOCKED`, because apparently databases can be pretty good queues when you ask nicely.

**Zero-Knowledge Cloud Storage**  
Client-side encrypted storage where the server gets your ciphertext and absolutely none of your secrets.

And then there's the occasional smaller project created because I thought:

> "Wait... how does that actually work?"

Those tend to become repositories.

---

### 🧠 Side quests

- 200+ LeetCode problems
- learning distributed systems by implementing the painful parts
- slowly getting better at Go
- occasionally discovering that the bug was, in fact, a goroutine
- measuring things before putting numbers on a résumé
- trying to leave every codebase slightly less cursed than I found it

---

### 🛠️ Things I speak

`Go` · `gRPC` · `Java 21` · `Spring Boot` · `PostgreSQL` · `Redis` · `Docker` · `REST` · `OpenTelemetry` · `Prometheus` · `Grafana` · `k6`

---

### 🕷️ What's next?

I'm looking for **backend / platform / distributed-systems engineering** roles where I can work on systems that have interesting problems hiding underneath apparently simple APIs.

Preferably the kind where **latency, concurrency, reliability, scale, or distributed state** eventually ruin someone's afternoon.

Those are usually the fun ones.

You can find me on [LinkedIn](https://www.linkedin.com/in/krishant-basotra/).

---

*Still learning. Still shipping. Still checking whether the leader is alive.*
