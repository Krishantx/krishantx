<!-- heya, welcome to the repo. grab a seat. -->

### Hey, I'm Krishant.

I make microservices measurable. Backend / distributed-systems engineer by training, security analyst by day job — I got tired of chasing detections manually, so now I build backend pipelines that do it for me, and flag them with performance numbers I can actually defend.

![me on weekends](https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif)

---

#### Currently building: [microservice-gateway-platform](https://github.com/Krishantx/microservice-gateway-platform)

A self-contained microservices platform — custom API gateway, Eureka service discovery, token-bucket rate limiter, three services, all under one `docker compose up`. Built it from scratch, then load-tested it until the claims were true:

- Custom **Spring Boot 3.5 / Java 21** API gateway as a filter chain: JWT auth (HS256, 30-min TTL), correlation-ID tracing, YAML-declared routing across Eureka-discovered services
- **k6**, 100 concurrent users, 60 s sustained: **269 authenticated req/s at p95 ≈ 94 ms, zero errors**; 401s told "no" in ~5 ms
- **69 unit/integration tests**, JaCoCo ~99% lines / ~98% branches, **CI green on every push** [![CI](https://github.com/Krishantx/microservice-gateway-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/Krishantx/microservice-gateway-platform/actions)
- Token-bucket rate limiter (Redis + PostgreSQL, fail-open when it goes down — the gateway degrades, it doesn't die), OpenTelemetry tracing end to end

#### The rest of me
- 300+ LeetCode problems — the boring reps so the fun parts stay fast
- My honest growth log lives in a private repo (this one is public-facing, that one is not)
- Open to backend / platform engineering roles — reach out on [LinkedIn](https://www.linkedin.com/in/krishant-basotra/)

**Things I speak:** Java 21 · Spring Boot · Redis · PostgreSQL · Docker Compose · k6 · OpenTelemetry