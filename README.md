# 👋 Hi, I'm Krishant

Backend & distributed-systems engineer. I build measurable microservice infrastructure — every number below is a tested, CI-verified result.

**Java 21 · Spring Boot · Microservices · Redis · PostgreSQL · Docker Compose · k6 · OpenTelemetry**

---

## 🚧 What I'm building

**Microservice Gateway Platform** — a self-contained microservices stack built from scratch: custom API gateway, service discovery, and a token-bucket rate limiter over a one-command 8-container Docker Compose topology.

- Custom **Spring Boot 3.5 / Java 21 API Gateway** as a filter chain: JWT auth (HS256, 30-min TTL), correlation-ID tracing, header validation, YAML-declared dynamic routing across **Eureka**-discovered services
- **k6 load-tested** (100 concurrent users, 60-second sustained run): **269 authenticated req/s at p95 94 ms, zero errors**; 401s rejected at **~5 ms p95**
- **69 unit/integration tests**, JaCoCo **~99% line / ~98% branch** coverage, **GitHub Actions CI** on every push
- Distributed **token-bucket rate limiter** (Redis buckets + PostgreSQL, HTTP 429, fail-open on outage) and **OpenTelemetry** tracing end to end

[![CI](https://github.com/Krishantx/microservice-gateway-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/Krishantx/microservice-gateway-platform/actions)

## 🧭 What I care about
Distributed systems · performance engineering · observability · honest failure modes (fail-open, budgets) · API hardening