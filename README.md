# 🛠️ Forage Software Engineering Virtual Experience Program

Project repo for the JPMC Advanced Software Engineering Forage program

This repository showcases my completed work for the **Software Engineering Virtual Experience Program** offered by **Forage** in collaboration with **JPMorgan Chase & Co.** It simulates real-world backend software development tasks, focusing on REST API design, Kafka messaging, and in-memory databases using Java and Spring Boot.

https://www.theforage.com/simulations/jpmorgan/advanced-software-engineering-r0fm

---

## ✅ Program Overview

This virtual internship provided a hands-on simulation of daily backend engineering work at a global financial institution. The tasks helped me strengthen my technical skills, understand enterprise-grade architecture, and apply problem-solving in a professional environment.

---

## 📋 Tasks

| Task                               | Duration   | Status         |
| ---------------------------------- | ---------- | -------------- |
| 🛠️ Project Setup                   | 30–60 mins | 🚧 In progress |
| 🔌 Kafka Integration               | 30–60 mins | 🚧 In progress |
| 🗃️ H2 Database Integration         | 30–60 mins | 🚧 In progress |
| 🌐 REST API Integration            | 30–60 mins | 🚧 In progress |
| 📡 REST API Controller Development | 1–2 hours  | 🚧 In progress |

### Task 1: project setup
- What you'll learn
  - How Software Engineers build and configure backend systems used to process high-volume financial transactions.
  - How to set up a Java development environment using Java 17, Spring Boot, Maven, and an IDE that supports enterprise projects.
  - How to work with engineering requirements and prepare a project scaffold for future integration tasks.
- What you'll do
  - Set up your local development environment by installing Java 17, forking and cloning the project repository, and opening it in your IDE.
  - Explore the existing project scaffold to understand how the Midas Core service is structured.
  - Add the required dependencies to your Spring Boot project and update configuration files.
  - Build and run the project, then verify your setup by running automated tests.

### Task 2: project setup

- What you'll learn
  - How message queues—specifically Kafka—are used to decouple services, improve scalability, and enable asynchronous communication in large backend systems.
  - How to integrate Kafka into a Spring Boot application by creating a listener that consumes messages from a configured topic.
  - How to deserialize incoming Kafka messages into domain objects and verify your integration using an embedded Kafka instance and automated tests.
- What you'll do
  - Implement a Kafka listener in Midas Core that reads from the topic defined in application.yml and deserializes each incoming message into the provided Transaction class.
  - Configure your listener to use the project’s existing Spring Boot setup—no need to specify host/port, as the tests use an embedded Kafka instance.
  - Run TaskTwoTests, use your debugger to inspect the first four received transactions, and record the amounts attached to each.
  - Submit the list of the four transaction amounts once your listener is working correctly.

### Task 3: project setup

- What you'll learn
  - How to integrate a SQL database into a Spring Boot application using H2 and Spring Data JPA.
  - How backend systems validate financial transactions and enforce business rules before persisting data.
  - How to model relational data using JPA entities, including one-to-many and many-to-one relationships.
  - How to combine data ingestion (Kafka) with database persistence in a cohesive service flow.
- What you'll do
  - Configure Midas Core to use an H2 in-memory database through Spring Boot and JPA.
  - Implement validation logic to determine whether a transaction is valid based on user IDs and account balances.
  - Create a TransactionRecord JPA entity and persist valid transactions while discarding invalid ones.
  - Update the sender and recipient balances when transactions are successfully processed.
  - Run TaskThreeTests, inspect the final balance of the waldorf user in your debugger, and submit the rounded-down value.

### Task 4: project setup

- What you'll learn
  - How backend services consume external REST APIs as part of a larger system architecture.
  - How to use Spring’s RestTemplate to send POST requests and deserialize JSON responses into Java objects.
  - How API boundaries act as contracts between teams, enabling independent development and safer system changes.
  - How to incorporate external incentive logic into an existing transaction-processing workflow.
- What you'll do
  - Run the provided Incentive API service locally and connect Midas Core to its /incentive endpoint.
  - Implement a method that posts validated Transaction objects to the Incentive API and receives an Incentive response.
  - Update your transaction-processing logic to store the incentive amount and correctly adjust user balances—adding incentives to recipients but not subtracting them from senders.
  - Run TaskFourTests, use your debugger to determine wilbur’s final balance, and submit the rounded-down result.

---

## 🧰 Tech Stack

- **Java**
- **Spring Boot**
- **Apache Kafka**
- **H2 In-Memory Database**
- **RESTful APIs**
- **Maven**

---

## 🏆 Certificate of Completion

I successfully completed the program and earned a certificate of achievement.

📄 **[View Certificate](./assets/forage-jpmorgan-software-engineering-certificate-of-completion.pdf)**

---
