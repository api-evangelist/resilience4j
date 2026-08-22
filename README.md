# Resilience4j

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
