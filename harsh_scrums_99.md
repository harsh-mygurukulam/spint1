
# Conclusion Documentation of **Monorepo vs Micro Repo**

| Created     | Version | Author        | Last Updated       | Comment          | Reviewer         |
|-------------|---------|---------------|--------------------|------------------|------------------|
| 26-04-2025  | V1   | Harsh Wardhan Singh   | 26-04-2025    | Internal Reviewer| Pritam           |
| 26-04-2025| V1.1| Harsh Wardhan Singh | 28-04-2025 | Internal Reviewer| Pritam |


## Table of Contents
- [Purpose](#purpose)
- [Introduction](#introduction)
- [Comparison Monorepo vs Micro Repo](#comparison-monorepo-vs-micro-repo)
- [Conclusion](#conclusion)
- [Contacts](#contacts)
- [References](#references)


## Purpose

The purpose of this documentation is to design an effective Version Control System (VCS) strategy that suits our organizational and project needs. We aim to compare Monorepo and Microrepo approaches, evaluate them against relevant criteria, and choose a path that best supports scalability, maintainability, and team collaboration.

## Introduction

Version Control Systems (VCS) are the backbone of modern software development, enabling collaboration, version tracking, and deployment management. Choosing the right repository structure is critical to ensure the system remains scalable, flexible, and efficient over time.

Two popular strategies for organizing repositories are:

- **Monorepo (Monolithic Repository)**
- **Microrepo (Multiple Repositories)**

Each has distinct characteristics, advantages, and trade-offs.

---

## Monorepo

A Monorepo approach consolidates multiple projects or services into a single repository. Organizations like Google, Meta, Uber, and Airbnb famously use Monorepos.

**Characteristics:**
- Single repository containing all services, libraries, and common components.
- Centralized control over versioning and standards.
- Shared tooling and dependencies.

**Advantages:**
- Easier to make atomic changes across multiple projects.
- Unified CI/CD pipelines.
- Promotes code reuse and sharing.
- Centralized access control and permissions.

**Challenges:**
- Repository can grow very large.
- Complex build and test processes.
- Tools must handle large-scale repositories efficiently.

---

## Microrepo

A Microrepo approach maintains each project or service in its own separate repository. Companies like Amazon, Netflix, LinkedIn, and Oracle follow this pattern.

**Characteristics:**
- Each service, library, or module has its own isolated repository.
- Teams have autonomy over their repositories.
- Different services can have different lifecycles.

**Advantages:**
- Simpler repositories that are easier to clone, build, and maintain.
- Decentralized ownership and responsibility.
- Flexibility in choosing technologies and versioning policies.

**Challenges:**
- Cross-repository changes are complex.
- Dependency management can become difficult.
- CI/CD pipelines must coordinate across multiple repositories.

---

## Comparison Monorepo vs Micro Repo

| Criteria        | Monorepo                                          | Microrepo                                      |
|-----------------|----------------------------------------------------|------------------------------------------------|
| **Companies**    | Google, Meta, Uber, Airbnb                        | Amazon, Netflix, LinkedIn, Oracle               |
| **Collaboration**| Shared repository, shared ownership               | Separate repositories, independent ownership   |
| **Dependency**   | Shared dependencies                               | Independent dependency management              |
| **Scalability**  | Single standard applied across all services      | Services define their own standards             |
| **Tooling**      | Bazel, Buck, Nix, Lerna                           | Gradle, Maven, NPM, CMake                       |
| **Atomic Changes**| Easy across all services                         | Difficult across multiple repositories          |
| **Access Control**| Centralized                                      | Decentralized                                   |
| **Build Complexity**| High for large codebases                       | Moderate depending on repo size                 |

---

## Conclusion

After careful evaluation, we will adopt a Monorepo strategy as it aligns better with our need for atomic changes across services, centralized standards, streamlined dependency management, and enhanced team collaboration. To support scalability and minimize conflicts, we will enforce clear modular boundaries and leverage powerful Monorepo tooling.

---
## Contacts

| Name        | Email| 
  |-------------|---------|
  | Harsh Wardhan Singh| harsh.singh.snaatak@mygurukulam.co| 



---

## References


| Title        | Link| 
  |-------------|---------|
  | Google Monorepo Practices|[https://opensource.google/documentation/reference/monorepos/](https://www.thoughtworks.com/en-in/insights/blog/agile-engineering-practices/monorepo-vs-multirepo)| 

    
---
