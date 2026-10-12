# Order and Fulfilment Platform

A Spring Boot modular monolith for exploring production-minded order and fulfilment system design.

## Prerequisites

- Java 17
- No separate Maven installation required; the Maven Wrapper is included.

## Build and verify

```bash
./mvnw clean test

```

This verifies:

- the Spring application context starts;
- the expected application modules exist;
- Spring Modulith accepts the module dependency structure.

## Run locally

```bash
./mvnw spring-boot:run
```

## Verify application health

```bash
curl -s http://localhost:8080/actuator/health
```

Expected result:

```json
{"groups":["liveness","readiness"],"status":"UP"}
```

## Application modules

- Order
- Inventory
- Payment
- Fulfilment
- Notification

## Current scope

The current increment establishes the application foundation and module boundaries. Business endpoints, persistence, messaging, authentication, and deployment infrastructure are intentionally deferred.
