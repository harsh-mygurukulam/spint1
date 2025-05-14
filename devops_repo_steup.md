
#   DevOps Repositories Setup Guide


## Author Information

| **Created** | **Version** | **Last Modified** | **Author**            | **Level**         | **Reviewer** |
|-------------|-------------|-------------------|------------------------|-------------------|--------------|
| 13-05-2025  | V1          |      | Harsh Wardhan Singh    | Internal review   | Pritam       |


##   Table of Contents

- [Introduction](#-introduction)
- [Pre-requisites](#-pre-requisites)
- [Step-by-Step Setup Guide](#-step-by-step-setup-guide)
  - [1. Create DevOps Repositories](#-1-create-devops-repositories)
  - [2. View Created Repositories](#-2-view-created-repositories)
  - [3. Clone and Initialize a Repository](#-3-clone-and-initialize-a-repository)
- [Conclusion](#-conclusion)
- [Contact Information](#-contact-information)
- [References](#-references)


##   Introduction

This guide walks you through setting up GitHub repositories to support a structured DevOps workflow. The setup enables code versioning, CI/CD automation, infrastructure-as-code storage, and centralized configuration management.

---

##   Pre-requisites

Before starting, ensure:

- Git is installed (`git --version`)
- Access to GitHub or an equivalent VCS platform
- SSH keys are configured for secure access
- You have the necessary permissions to create repositories

---

##   Step-by-Step Setup Guide

###   1. Create DevOps Repositories

Create the following repositories in your GitHub organization:

| Repository Name       | Purpose                                           |
|-----------------------|---------------------------------------------------|
| `ci-cd-pipeline`      | Stores Jenkins/GitHub Actions pipelines           |
| `terraform-repo`      | Infrastructure-as-Code using Terraform            |
| `monitoring-repo`     | Configuration for Prometheus, Grafana, and logs   |
| `ansible`             | Configuration management using Ansible            |

  **Screenshot: Creating `ci-cd-pipeline` Repository**  


![Screenshot from 2025-05-12 11-28-01](https://github.com/user-attachments/assets/f7b4091b-bc5b-427e-8c2d-f3c4b27cd861)

---

###   2. View Created Repositories

Once all repositories are created, verify them in the GitHub organization dashboard.

  **Screenshot: Repositories in Organization**  


![Screenshot from 2025-05-12 11-28-52](https://github.com/user-attachments/assets/8b769313-fe24-4e38-bcf6-1bdab9e23ccc)


---

###   3. Clone and Initialize a Repository

```bash
git clone git@github.com:Team-Downtime-Crew/ci-cd-pipeline.git
cd ci-cd-pipeline
echo "# CI/CD Pipeline Repo" > README.md
git add README.md
git commit -m "Initial commit"
git push origin main
```

---


##  Conclusion

You have successfully set up a clean DevOps repository structure. These repositories will serve as the backbone for your CI/CD, infrastructure provisioning, monitoring, and configuration automation workflows.

---

##   Contact Information

| Name                | Email Address                          |
|---------------------|-----------------------------------------|
| Harsh Wardhan Singh | harsh.singh.snaatak@mygurukulam.co     |

---

##   References
| **Link** | **Description**            |
|----------|-------------------------------|
|[GitHub Documentation](https://docs.github.com/)| Comprehensive guide on repository creation and management.|
|[Terraform Documentation](https://developer.hashicorp.com/terraform/docs) | Detailed reference for infrastructure as code setup using Terraform.|
|[Ansible Documentation](https://docs.ansible.com/)| Official guide for configuration management with Ansible.|
| [Prometheus Documentation](https://prometheus.io/docs/) | Resources for monitoring system setup and rules. |
| [Grafana Documentation](https://grafana.com/docs/) | Insights on creating dashboards and integrating with Prometheus.|
