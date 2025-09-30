# Graph-driven Security Assurance in Web Software Architectures – Dataset

This repository contains the dataset used to validate the thesis **"Graph-driven Security Assurance in Web Software Architectures."**  

The goal is to provide a structured collection of **software architectures** that serve as study objects for:  

- Identifying architectural weaknesses  
- Detecting security vulnerabilities  
- Redesigning architectures with countermeasures  

All of these activities are performed at the **security level**.  

---

## Dataset Structure  

The dataset is organized into **three groups of architectures**.  
Each group is represented by a folder (`group_1`, `group_2`, `group_3`).  

Inside each group, every system is documented in a dedicated `.sarch` file, which describes its architecture using the **SARCH language**.  

---

## Group 1 – Open Source Projects  

These are **real-world open-source projects** manually collected from GitHub.  
They provide concrete examples of microservice-based architectures with different domains, technologies, and integration patterns.  

### 📌 Included Projects  

- **[abixen/abixen-platform](https://github.com/abixen/abixen-platform)**  
  A modular platform for building enterprise applications using microservices and data flow pipelines.  
  Focus: **data-driven architecture**, microservices orchestration, and scalability.  

- **[xebialabs/e-commerce-microservice](https://github.com/xebialabs/e-commerce-microservice)**  
  An e-commerce application demonstrating microservice architecture principles.  
  Focus: **transactional workflows, service interaction, and API communication**.  

- **[Microservice-API-Patterns/LakesideMutual](https://github.com/Microservice-API-Patterns/LakesideMutual)**  
  An insurance company system built to illustrate **Microservice API patterns**.  
  Focus: **API gateway, backend-for-frontend, service decomposition patterns**.  

- **[idugalic/micro-company](https://github.com/idugalic/micro-company)**  
  A sample company domain using DDD (Domain-Driven Design) with microservices.  
  Focus: **event-driven architecture, CQRS, and bounded contexts**.  

- **[eventuate-tram/eventuate-tram-sagas-examples-customers-and-orders](https://github.com/eventuate-tram/eventuate-tram-sagas-examples-customers-and-orders)**  
  Demonstrates the **Saga pattern** for managing distributed transactions.  
  Focus: **fault tolerance, consistency, and resiliency in microservices**.  

- **[spring-petclinic/spring-petclinic-microservices](https://github.com/spring-petclinic/spring-petclinic-microservices)**  
  A well-known case study for microservice architectures.  
  Focus: **service decomposition, API gateway, service discovery, monitoring, and resilience patterns**.  

- **[sqshq/piggymetrics](https://github.com/sqshq/piggymetrics)**  
  A personal finance app based on microservices.  
  Focus: **Spring Boot, Spring Cloud, API gateway, config server, monitoring, and distributed tracing**.  

- **[mudigal-technologies/microservices-sample](https://github.com/mudigal-technologies/microservices-sample)**  
  An example of a Java Spring Boot microservices project.  
  Focus: **basic service interaction and database integration**.  

- **[anilallewar/microservices-basics-spring-boot](https://github.com/anilallewar/microservices-basics-spring-boot)**  
  A starter template for building microservices.  
  Focus: **Spring Boot, REST APIs, and service orchestration basics**.  

- **[apssouza22/java-microservice](https://github.com/apssouza22/java-microservice)**  
  A Java microservices sample project.  
  Focus: **REST APIs, fault isolation, and modular service design**.  

- **[fernandoabcampos/spring-netflix-oss-microservices](https://github.com/fernandoabcampos/spring-netflix-oss-microservices)**  
  Demonstrates Netflix OSS stack for microservices.  
  Focus: **Eureka (service discovery), Zuul (API gateway), Hystrix (fault tolerance)**.  

- **[ewolff/microservice](https://github.com/ewolff/microservice)**  
  A demo application for **microservice design patterns**.  
  Focus: **DDD, independent deployability, and scaling**.  

- **[ewolff/microservice-kafka](https://github.com/ewolff/microservice-kafka)**  
  A variant of the previous project using **Kafka for asynchronous communication**.  
  Focus: **event-driven architecture and message-based decoupling**.  

- **[aspnetrun/run-aspnetcore-microservices](https://github.com/aspnetrun/run-aspnetcore-microservices)**  
  A .NET Core implementation of an e-commerce system with microservices.  
  Focus: **ASP.NET Core, Docker, Kubernetes, and service orchestration**.  

- **[gfawcett22/EnterprisePlanner](https://github.com/gfawcett22/EnterprisePlanner)**  
  A project management and planning tool built with microservices.  
  Focus: **enterprise workflows and modular services**.  

- **[EdwinVW/pitstop](https://github.com/EdwinVW/pitstop)**  
  A garage management system based on microservices.  
  Focus: **event sourcing, CQRS, and cloud-native integration**.  

---

## Group 2 – Research Systems  

This group contains **architectures from prior academic research**.  
These systems were used in peer-reviewed studies to evaluate microservice security and design properties.  

🔗 [microSecEnD – TUHH Software Security Group](https://tuhh-softsec.github.io/microSecEnD/models.html)  

Examples include:  
- A taxi-hailing system  
- An online shop  
- An IoT-based monitoring platform  
- Various benchmark microservice systems  

Focus: **empirical validation, security metrics, and vulnerability analysis**.  

---

## Group 3 – LLM-generated Architectures  

This group contains **synthetic architectures generated using Large Language Models (LLMs)**.  
They complement real-world and research-based architectures by providing additional scenarios for:  

- Stress-testing architectural analysis methods  
- Exploring “what-if” redesigns with embedded countermeasures  
- Expanding coverage of architectural patterns and anti-patterns  

---

## Folder Structure  

