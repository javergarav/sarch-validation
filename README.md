# Sarch Dataset

This repository contains the dataset used to validate the PhD thesis **"Graph-Driven Security Assurance in Web Software Architectures"**.

The goal is to provide a structured collection of **software architecture descriptions** that serve as study objects for:  

- Identifying architectural weaknesses.
- Detecting security vulnerabilities.  
- Redesigning architectures with countermeasures.  

All of these activities are performed at the **security level**.  

---

## Dataset Structure  

The dataset is organized into **two groups of architecture descriptions**.  
Each group is represented by a folder (`group_1`, `group_2`).  

Inside each group, every system is documented in a dedicated `.sarch` file, which describes its architecture using the **Sarch language**.  

---

## Group 1 – Open Source Projects  

These are **real-world open-source projects** manually collected from:

* GitHub: manual review by keywords.
* Previous Research Works: manual review in conference and journal papers.

They provide concrete examples of web-based architectures with different domains, technologies, and patterns.

### Included Projects  

1. **[abixen/abixen-platform](https://github.com/abixen/abixen-platform)**  
  A modular platform for building enterprise applications using microservices and data flow pipelines.  
  Focus: **data-driven architecture**, microservices orchestration, and scalability.  

2. **[xebialabs/e-commerce-microservice](https://github.com/xebialabs/e-commerce-microservice)**  
  An e-commerce application demonstrating microservice architecture principles.  
  Focus: **transactional workflows, service interaction, and API communication**.  

3. **[Microservice-API-Patterns/LakesideMutual](https://github.com/Microservice-API-Patterns/LakesideMutual)**  
  An insurance company system built to illustrate **Microservice API patterns**.  
  Focus: **API gateway, backend-for-frontend, service decomposition patterns**.  

4. **[idugalic/micro-company](https://github.com/idugalic/micro-company)**  
  A sample company domain using DDD (Domain-Driven Design) with microservices.  
  Focus: **event-driven architecture, CQRS, and bounded contexts**.  

5. **[eventuate-tram/eventuate-tram-sagas-examples-customers-and-orders](https://github.com/eventuate-tram/eventuate-tram-sagas-examples-customers-and-orders)**  
  Demonstrates the **Saga pattern** for managing distributed transactions.  
  Focus: **fault tolerance, consistency, and resiliency in microservices**.  

6. **[spring-petclinic/spring-petclinic-microservices](https://github.com/spring-petclinic/spring-petclinic-microservices)**  
  A well-known case study for microservice architectures.  
  Focus: **service decomposition, API gateway, service discovery, monitoring, and resilience patterns**.  

7. **[sqshq/piggymetrics](https://github.com/sqshq/piggymetrics)**  
  A personal finance app based on microservices.  
  Focus: **Spring Boot, Spring Cloud, API gateway, config server, monitoring, and distributed tracing**.  

8. **[mudigal-technologies/microservices-sample](https://github.com/mudigal-technologies/microservices-sample)**  
  An example of a Java Spring Boot microservices project.  
  Focus: **basic service interaction and database integration**.  

9. **[anilallewar/microservices-basics-spring-boot](https://github.com/anilallewar/microservices-basics-spring-boot)**  
  A starter template for building microservices.  
  Focus: **Spring Boot, REST APIs, and service orchestration basics**.  

10. **[apssouza22/java-microservice](https://github.com/apssouza22/java-microservice)**  
  A Java microservices sample project.  
  Focus: **REST APIs, fault isolation, and modular service design**.  

11. **[fernandoabcampos/spring-netflix-oss-microservices](https://github.com/fernandoabcampos/spring-netflix-oss-microservices)**  
  Demonstrates Netflix OSS stack for microservices.  
  Focus: **Eureka (service discovery), Zuul (API gateway), Hystrix (fault tolerance)**.  

12. **[ewolff/microservice](https://github.com/ewolff/microservice)**  
  A demo application for **microservice design patterns**.  
  Focus: **DDD, independent deployability, and scaling**.  

13. **[ewolff/microservice-kafka](https://github.com/ewolff/microservice-kafka)**  
  A variant of the previous project using **Kafka for asynchronous communication**.  
  Focus: **event-driven architecture and message-based decoupling**.  

14. **[aspnetrun/run-aspnetcore-microservices](https://github.com/aspnetrun/run-aspnetcore-microservices)**  
  A .NET Core implementation of an e-commerce system with microservices.  
  Focus: **ASP.NET Core, Docker, Kubernetes, and service orchestration**.  

15. **[gfawcett22/EnterprisePlanner](https://github.com/gfawcett22/EnterprisePlanner)**  
  A project management and planning tool built with microservices.  
  Focus: **enterprise workflows and modular services**.  

16. **[EdwinVW/pitstop](https://github.com/EdwinVW/pitstop)**  
  A garage management system based on microservices.  
  Focus: **event sourcing, CQRS, and cloud-native integration**. 

Sources:

* [microSecEnD – TUHH Software Security Group](https://tuhh-softsec.github.io/microSecEnD/models.html)
---

## Group 3 – LLM-generated Architectures  

This group contains **synthetic architectures generated using Large Language Models (LLMs)**.  
They complement real-world architectures by providing additional scenarios for security.

