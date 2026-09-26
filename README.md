<!-- heya, welcome to the repo. grab a seat. -->

### Hey, I'm Krishant.

I make microservices measurable. Backend / distributed-systems engineer by training, security analyst by day job — I got tired of chasing detections manually, so now I build backend pipelines that do it for me, and flag them with performance numbers I can actually defend.

![me on weekends](https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif)

---

#### Currently building: [raft-based-key-value-store](https://github.com/Krishantx/raft-based-distributed-key-value-store)

A distributed key-value store that runs on Raft consensus I wrote from scratch in **Go + gRPC** — no Hashicorp raft, no libraries for the hard part. `raft-aware-proxy` fans client ops to the leader, nodes campaign with a **voting protocol**, keep control with **heartbeats**, and applied log entries land in an in-memory KV repo.

It's mid-flight (heartbeat keep-alive is in, replication edge cases are the current boss fight). It also has my "you don't get to claim it until it's tested" rule attached, so tests land before this goes anywhere near my resume.

#### Also done: [microservice-gateway-platform](https://github.com/Krishantx/microservice-gateway-platform)

A self-contained microservices lab — custom Spring Boot API gateway, Eureka discovery, token-bucket rate limiter, three services, one `docker compose up`, k6-tested until the claims were true: **269 authenticated req/s at p95 ≈ 94 ms, zero errors**, 69 tests at ~99% line coverage, CI green on every push. [![CI](https://github.com/Krishantx/microservice-gateway-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/Krishantx/microservice-gateway-platform/actions)

#### The rest of me
- 300+ LeetCode problems — the boring reps so the fun parts stay fast
- My honest growth log lives in a private repo (this one is public-facing, that one is not)
- Open to backend / platform engineering roles — reach out on [LinkedIn](https://www.linkedin.com/in/krishant-basotra/)

**Things I speak:** Go · gRPC · Java 21 · Spring Boot · Redis · PostgreSQL · Docker Compose · k6 · OpenTelemetry