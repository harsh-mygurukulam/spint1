## Application Template
---

##  **Author Information**
| Created     | Version | Author        | Last Updated       | Comment          | Reviewer         |
|-------------|---------|---------------|--------------------|------------------|------------------|
| 25-04-2025  | V1   | Harsh Wardhan Singh   |   28-04-2025                | Internal Reviewer| Pritam           |

---


##  Table of Contents

1. [Introduction](#introduction)  
2. [Why need this application?](#why-need-this-application)  
3. [What problems does it resolve?](#what-problems-does-it-resolve)  
4. [Pre-requisites](#pre-requisites)  
    - [System Requirements](#system-requirements)  
5. [Dependencies](#dependencies)  
    - [Build Time Dependency](#build-time-dependency)  
    - [Run Time Dependency](#run-time-dependency)  
    - [Important Ports](#important-ports)  
6. [Architecture](#architecture)  
7. [Dataflow Diagram](#dataflow-diagram)  
8. [Step-by-step installation of Application](#step-by-step-installation-of-application)  
    - [Step 1: Installation of software Dependencies](#step1-installation-of-software-dependencies)  
    - [Step 2: Build/Artifact Generation](#step2-buildartifact-generation)  
    - [Step 3: Application Deployment](#step3-application-deployment)  
9. [Troubleshooting](#troubleshooting)  
10. [Contact Information](#contact-information)  
11. [References](#references)  

---

## Introduction
Salary API is a microservice developed in Java that handles all operations related to salary processing and record-keeping within the OT-Microservices architecture. Designed with portability in mind, this service is platform-agnostic and can operate seamlessly across different operating systems, provided a Java Runtime Environment (JRE) is available. Its core responsibility is to ensure accurate and efficient handling of payroll transactions while integrating smoothly into the broader microservice ecosystem.

---

## Why need this application?
A dedicated service for salary-related operations is crucial in a distributed microservices architecture. Centralizing this logic in a single microservice promotes modularity, simplifies payroll integration, and ensures a single source of truth for all salary data and transactions.

---
## What problems does it resolve?
--> Eliminates salary data duplication across services

--> Provides consistent APIs for salary operations

--> Enhances maintainability of payroll logic

-->Enables audit trails for salary changes

-->Simplifies integration with downstream services like attendance and leave management



---

## Prerequisites

| Hardware Specifications | Minimum Recommendation |
|-------------------------|------------------------|
| Processor                | Dual Core                        |
| Ram                      | 4GB                       |
| Disk                     | 20GB                       |
| OS                       | Ubuntu(22.04)     |

---
## Dependencies

### Build Time Dependency



|Name    |	Version	|Description|
|--------|----------|------------|
|Maven	 |3.8+       |	Java build automation tool|
|OpenJDK	|17+	    |Java development environment|
|Make|4.3+|It runs the default target in a Linux-unix environment|
|Jq | 1.6| To manipulate JSON file|

### Run Time Dependency

|Name    |	Version	|Description|
|--------|----------|------------|
|ScyllaDB	 |4.6+	      |	Distributed NoSQL DB|
|Redis		|6.0+    |No sql Db|

---
### Important Ports

| Inbound Traffic         | Description |
|-------------------------|------------------------|
| 8080          | Used by Spring Boot embedded server           |


| Outbound Traffic         | Description |
|-------------------------|------------------------|
| 9042          | 	ScyllaDB port          |

---
### Architecture

![Screenshot from 2025-04-26 00-57-09](https://github.com/user-attachments/assets/26f5c54d-9dd2-46d5-a106-5b620fb63802)

---
### Dataflow Diagram

**1.User/API Client → Salary API**

A request for salary-related data is made.

**2.Salary API → Redis Cache**

The Salary API first checks Redis to find the requested data (cache lookup).

**3.Redis Cache**

If cache hit → returns the data directly to Salary API.

If cache miss → Redis queries ScyllaDB for the data.

**4.ScyllaDB → Redis Cache**

ScyllaDB sends the requested data to Redis, which updates the cache.

**5.Redis Cache → Salary API**

Redis returns the fresh data back to the Salary API.

**6.Salary API → User/API Client**

Salary API sends the final response.

**7.Migrations Service → ScyllaDB**

Migrations are handled separately, ensuring the database (ScyllaDB) is up-to-date.


## Step-by-step for Salary API

  Please follow step here  [Refer this POC](https://github.com/snaatak-Downtime-Crew/Documentation/blob/SCRUMS-80-Durgesh/ot-ms-understanding/salary/poc/README.md)


---
## Troubleshooting
While setting up and running the Salary API microservice, users may encounter common issues related to port conflicts, database connectivity, build failures, or caching errors. It is recommended to ensure that required ports (like 8080 for the application and 9042 for ScyllaDB) are free and accessible. In case of database connection errors, verify that ScyllaDB and Redis services are correctly installed, configured, and running. Maven build failures can often be resolved by cleaning the build cache or ensuring the correct Maven and JDK versions are installed. Additionally, users should monitor system resources like memory and disk space to avoid runtime issues. Reviewing application logs and enabling debug mode can provide deeper insights for troubleshooting. A detailed list of common errors and their resolutions is provided below to assist users in quickly identifying and fixing problems during installation or deployment.


---

### Contact Information

| Name         | Email Address                                 |
|--------------|-----------------------------------------------|
| Harsh Wardhan Singh | harsh.singh.snaatak@mygurukulam.co           |

---
## References

| Reference               | Link                                                                           |
|-------------------------|--------------------------------------------------------------------------------|
| ScyllaDB Introduction documentation    | [Click here](https://github.com/duggu7055/Snaatak/blob/main/Sprint1/Scylla%20documentation/Readme.md)                             |
| ScyllaDB Installation documentation    | [Click here](https://docs.github.com)                             |
| Redis Installation Guide              | [Click here](https://github.com/snaatak-Downtime-Crew/Documentation/blob/SCRUMS-84-PRINCE/ot-ms-understanding/redis/poc/README.md)                               |
| Maven                   | [Click here](https://maven.apache.org/what-is-maven.html)                                           |
