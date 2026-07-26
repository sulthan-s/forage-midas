# Midas Core — JPMorgan Chase & Co. Forage Software Engineering

Midas Core is a backend financial microservice built with Spring Boot, Apache Kafka, and Spring Data JPA. The application ingests, validates, and processes high-throughput financial transactions, enforces business validation rules, integrates with external incentives services, and exposes REST endpoints for user balance queries.

---

## 🏗️ Architecture & Features

* **Kafka Data Ingestion:** Consumes stream updates containing transaction payloads from Kafka topics (`trader-updates`).
* **Transaction Validation & Business Logic:** Validates sender/recipient existence and checks sender balances prior to processing transactions.
* **Database Persistence:** Stores valid transactions and maintains relational user mappings using Spring Data JPA and an H2 in-memory database.
* **External Incentives API Integration:** Connects with an external Incentive microservice via REST (`RestTemplate`) to apply promotional bonuses to transactions.
* **REST API Endpoints:** Exposes a `/balance` REST endpoint to query real-time account balances.
* **Integration Testing:** Covered with comprehensive Testcontainers and Spring Boot integration tests (`TaskOneTests` through `TaskFiveTests`).

---

## 🛠️ Tech Stack

* **Language:** Java 17+
* **Framework:** Spring Boot 3.x (Spring Web, Spring Data JPA, Spring Kafka)
* **Messaging:** Apache Kafka
* **Database:** H2 In-Memory Database
* **Build Tool:** Maven (Maven Wrapper)
* **Testing:** JUnit 5, Testcontainers

---

## 🚀 Getting Started

### Prerequisites
* **Java Development Kit (JDK):** Version 17 or higher
* **Git**

### Environment Setup
Set your `JAVA_HOME` path (adjust to your local JDK path):

```powershell
$env:JAVA_HOME="C:\Program Files\Java\jdk-26"
