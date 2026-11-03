# PROJECT CHARTER
## EDOMS Commerce — Event-Driven Order Management System

**Document Version:** 1.0  
**Status:** Draft  
**Project Type:** Software Engineering Portfolio Project  
**Architecture:** Microservices / Event-Driven Architecture

---

## 1. Project Background

EDOMS Commerce is a fictional e-commerce company experiencing increasing transaction volumes.

Its existing order management system handles order processing, inventory management, payment processing, and customer notifications within a tightly coupled application.

As transaction volume grows, the company faces challenges related to service dependency, system scalability, failure handling, and operational visibility.

The company intends to develop a distributed order management system using microservices and event-driven architecture.

## 2. Problem Statement

The existing system has the following limitations:

- High coupling between business modules.
- Synchronous dependencies between order, inventory, and payment processing.
- Limited failure isolation.
- Difficult independent scaling.
- Insufficient event recovery mechanisms.
- Limited observability across business transactions.

## 3. Project Objectives

The project aims to:

1. Decouple business capabilities into independent microservices.
2. Implement asynchronous communication using Apache Kafka.
3. Improve reliability through message handling and recovery mechanisms.
4. Prevent duplicate business processing through idempotency.
5. Implement distributed transaction management using the Saga pattern.
6. Provide observability through centralized logging and metrics.
7. Automate testing, building, and deployment.

## 4. Project Scope

### In Scope

- Order management.
- Inventory management and stock reservation.
- Payment simulation.
- Customer notification.
- Kafka-based event processing.
- Transactional Outbox Pattern.
- Idempotent consumers.
- Retry and Dead Letter Queue.
- Monitoring and observability.
- Automated testing.
- Docker-based deployment.
- Kubernetes deployment.

### Out of Scope — Initial Release

- Real payment gateway integration.
- Real email or WhatsApp delivery.
- Multi-warehouse inventory optimization.
- Advanced recommendation engine.
- Real customer identity verification.
- Multi-region deployment.

## 5. Technology Stack

| Component | Technology |
|---|---|
| Backend | Golang, Gin |
| Messaging | Apache Kafka |
| Database | PostgreSQL |
| Frontend | React |
| Containerization | Docker |
| Local orchestration | Docker Compose |
| Production orchestration | Kubernetes / OpenShift |
| CI/CD | GitHub Actions |
| Monitoring | Prometheus, Grafana |
| Logging | Structured logging |
| Testing | Go testing, Testcontainers, k6 |

## 6. Expected Deliverables

- Functional microservices.
- Event-driven communication.
- Database schema and migrations.
- API documentation.
- Architecture documentation.
- Automated test suites.
- Monitoring dashboards.
- CI/CD pipeline.
- Docker Compose deployment.
- Kubernetes deployment manifests.
- Technical documentation and demonstration.

## 7. Success Criteria

The project will be considered successful when:

- Orders can be created and tracked.
- Inventory reservation works correctly.
- Payment success and failure scenarios are handled.
- Services communicate through Kafka events.
- Duplicate events do not cause duplicate business operations.
- Failed events can be retried or moved to DLQ.
- The system recovers from service restarts.
- Integration and end-to-end tests pass.
- Monitoring dashboards expose relevant metrics.
- The application can be deployed through automated pipelines.

## 8. Constraints and Assumptions

- This project uses a fictional business scenario.
- Payment processing is simulated.
- Initial development uses a local Docker environment.
- Production-like deployment will be introduced incrementally.
- Performance targets must be validated through load testing.
- Each microservice owns its business data.

## 9. Project Governance

Technical decisions must be documented through Architecture Decision Records (ADR).

Requirements must be traceable to implementation and test cases.

Changes to the initial project scope must be reviewed before implementation.

---

**Document Owner:** Project Lead  
**Status:** Pending Requirement Review