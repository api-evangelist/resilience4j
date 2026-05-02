# Resilience4j

Resilience4j is a lightweight fault tolerance library designed for Java 17+ and functional programming, providing higher-order functions to enhance functional interfaces with Circuit Breaker, Rate Limiter, Retry, Bulkhead, TimeLimiter, and Cache patterns. Designed as a replacement for Netflix Hystrix, it integrates with Spring Boot 2 and 3, Micronaut, RxJava, Spring Reactor, Micrometer, Prometheus, and Dropwizard Metrics. Used in production by Deutsche Telekom (400M+ requests/day), PlayStation Network, AOL, and Auto Trader Group. Latest release: v2.4.0 (March 2026).

## Core Modules

| Module | Description |
|--------|-------------|
| Circuit Breaker | Prevents cascading failures with COUNT_BASED or TIME_BASED sliding windows |
| Rate Limiter | Controls request throughput with configurable limits and refresh periods |
| Bulkhead | Isolates resources with concurrent call limits (Semaphore or ThreadPool) |
| Retry | Automatic retries with fixed, exponential, or randomized backoff |
| Time Limiter | Timeout handling with configurable duration and future cancellation |
| Cache | Result caching based on javax.cache (JCache) |

## Framework Integrations

- **Spring Boot 2 & 3** — Auto-configuration, health indicators, Actuator endpoints
- **Micronaut** — Native integration
- **RxJava 2 & 3** — Reactive operators
- **Spring Reactor** — Reactive operators
- **Feign** — HTTP client integration
- **Kotlin** — Coroutine support

## Monitoring

Resilience4j exposes metrics via:
- **Micrometer** — Prometheus, Grafana, Datadog, etc.
- **Dropwizard Metrics** — JMX, console, CSV
- **Spring Boot Actuator** — `/actuator/circuitbreakers`, `/actuator/retries`, `/actuator/ratelimiters`, `/actuator/bulkheads`

## Artifacts

### JSON Schema

- [circuit-breaker-configuration.json](json-schema/circuit-breaker-configuration.json) — Schema for CircuitBreaker configuration (application.yml / application.properties).
- [retry-configuration.json](json-schema/retry-configuration.json) — Schema for Retry configuration.
- [rate-limiter-configuration.json](json-schema/rate-limiter-configuration.json) — Schema for RateLimiter configuration.
- [bulkhead-configuration.json](json-schema/bulkhead-configuration.json) — Schema for Bulkhead configuration.
- [time-limiter-configuration.json](json-schema/time-limiter-configuration.json) — Schema for TimeLimiter configuration.

### JSON Structure

- [resilience4j-circuit-breaker-structure.json](json-structure/resilience4j-circuit-breaker-structure.json) — Field-level documentation for circuit breaker configuration.
- [resilience4j-retry-structure.json](json-structure/resilience4j-retry-structure.json) — Field-level documentation for retry configuration.

### JSON-LD

- [resilience4j-context.jsonld](json-ld/resilience4j-context.jsonld) — JSON-LD context mapping Resilience4j vocabulary to schema.org.

### Examples

- [resilience4j-circuit-breaker-config-example.json](examples/resilience4j-circuit-breaker-config-example.json) — Spring Boot application.yml configuration example for a circuit breaker protecting a payment service.

### Vocabulary

- [resilience4j-vocabulary.yml](vocabulary/resilience4j-vocabulary.yml) — Domain vocabulary covering circuit breaker states, resilience patterns, and monitoring concepts.

## Links

- **Documentation:** https://resilience4j.readme.io/docs
- **Getting Started:** https://resilience4j.readme.io/docs/getting-started
- **GitHub:** https://github.com/resilience4j/resilience4j
- **GitHub Organization:** https://github.com/resilience4j
- **Releases:** https://github.com/resilience4j/resilience4j/releases
- **Maven Central:** https://search.maven.org/search?q=io.github.resilience4j
- **Spring Boot Demo:** https://github.com/resilience4j/resilience4j-spring-boot-demo
- **License:** Apache-2.0
