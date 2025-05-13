
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
  - [4. Setup Branch Protection Rules (Optional)](#-4-setup-branch-protection-rules-optional)
  - [5. Set Collaborator Permissions](#-5-set-collaborator-permissions)
  - [6. Configure Webhooks for CI/CD (Optional)](#-6-configure-webhooks-for-cicd-optional)
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

###   4. Setup Branch Protection Rules (Optional)

- Navigate to **Settings → Branches**
- Create a rule to protect the `main` branch
- Enable: require pull request review, status checks, and restrict force pushes

---

###   5. Set Collaborator Permissions

- Go to **Settings → Collaborators**
- Invite team members and assign appropriate access levels (admin/write/read)

---

###   6. Configure Webhooks for CI/CD (Optional)

- Go to **Settings → Webhooks**
- Add your Jenkins/GitHub Actions URL
- Select events like `push` or `pull_request` for triggering automation

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

