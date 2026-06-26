# IdentityVault #
A production-grade, multi-tenancy identity data API built 
with Java 21 and Spring Boot 4. Built as a demonstration 
of secure backend engineering with a focus on identity data 
infrastructure. 

## What It Does ##
IdentityVault allows organisations to store and manage 
personal identity records securely. Each organisation is 
a tenant, and it is architecturally impossible for one tenant 
to access another's data, enforced independently at both the 
application layer and the database layer. 

## Engineering Concepts Demonstrated ##
### Multi-tenancy: Tenant isolation via PostgreSQL Row-Level 
Security and application-layer scoping

### Authentication ###
JWT with refresh token rotation. Secure token storage

### Field-level encryption ###
AES-256-GCM encryption on PII columns at rest

### Caching ###
Redis caching of identity lookups with tenant-scoped keys and 
TTL

### Rate Limiting ###
Per-tenant rate limiting on auth endpoints

### Audit Logging ###
Immutable, append-only audit trail of all identity data access 
and mutation

### Structured Error Handling ###
Consistent error envelopes, correlation IDs, and no stack 
traces in responses

### Testing ###
Testcontainers integration tests against PostgreSQL, and Mockito unit tests

### CI/CD ###
GitHub Actions pipeline with automated testing and dependency scanning

## Project Status ##
| Feature                    | Status      |
|----------------------------|-------------|
| Testcontainers and Mockito | X           |
| JWT Authentication         | In Progress |
| Refresh token rotation     | Planned     |
| Multi-tenancy Features     | Planned     |
| Field-level encryption     | Planned     |
| Redis caching              | Planned     |
| Rate limiting              | Planned     |
| Audit log                  | Planned     |
| Structured Error Handling  | Planned     |
| GitHub Actions CI pipeline | Planned     |

## Tech Stack ##
| Layer         | Technology                                        |
|---------------|---------------------------------------------------|
| Language      | Java 21                                           |
| Framework     | Spring Boot 4, Spring Security 6, Spring Data JPA |
| Database      | PostgreSQL 17 with Row-Level Security             |
| Cache         | Redis                                             |
| Rate Limiting | Bucket4j                                          |
| Auth          | JJWT 0.12                                         |
| Encryption    | AES-256-GCM                                       |
| Testing       | JUnit, Mockito, Testcontainers                    |
| Build         | Maven                                             |
| CI/CD         | GitHub Actions                                    |

# Environment Variables #
Environment variables are required to run this project. See .env.example for a 
full list. 

To run locally, configure the environment variables in your IDE.
To run on AWS, store them in AWS Secrets Manager

## Background ##
Built by Katherine Wyers, software engineer specialising in identity and health
data infrastructure, with a PhD in digital public infrastructure from the
University of Oslo.