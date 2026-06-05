# LNT_ALL_PROJECTS

[![GitHub](https://img.shields.io/badge/GitHub-darshankerkar-181717?style=flat&logo=github)](https://github.com/darshankerkar)
[![Projects](https://img.shields.io/badge/Projects-5-blue?style=flat)](https://github.com/darshankerkar/LNT_ALL_PROJECTS)
[![Training](https://img.shields.io/badge/Program-LnT%20DevOps%20Training-orange?style=flat)](https://github.com/darshankerkar/LNT_ALL_PROJECTS)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat)](LICENSE)

---

A consolidated repository containing all hands-on projects built during the **LnT DevOps Training Program**. Each project is a self-contained, production-oriented implementation covering a core area of modern DevOps: CI/CD, containerization, Git workflows, infrastructure automation, and Kubernetes autoscaling.

---

## Table of Contents

- [Repository Structure](#repository-structure)
- [Projects Overview](#projects-overview)
  - [Mini Project 4: CI/CD Pipeline](#mini-project-4-ci-cd-pipeline)
  - [Mini Project 3: Dockerised To-Do API](#mini-project-3-dockerised-to-do-api)
  - [Mini Project 2: Git Workflow Simulator](#mini-project-2-git-workflow-simulator)
  - [Infrastructure as Code Pipeline](#infrastructure-as-code-pipeline)
  - [Mini Project 8: Kubernetes Autoscaling](#mini-project-8-kubernetes-autoscaling)
- [Technology Stack](#technology-stack)
- [Training Curriculum](#training-curriculum)
- [Getting Started](#getting-started)

---

## Repository Structure

```
LNT_ALL_PROJECTS/
│
├── Mini_Project_4/              # GitHub Actions CI/CD with Python Calculator
│   ├── .github/workflows/
│   │   └── CI.yml
│   └── Day_3/Project/Calculator/
│       ├── calculator.py
│       └── test_calculator.py
│
├── Mini_Project_3/              # Production-grade Dockerized REST API
│   ├── app.py
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── Makefile
│   └── requirements.txt
│
├── Mini_Project_2/              # Professional Git collaboration workflow simulator
│   ├── .github/
│   │   ├── CODEOWNERS
│   │   └── PULL_REQUEST_TEMPLATE.md
│   └── workflow-simulator.py
│
├── IAC_Pipeline/                # Terraform + GitHub Actions IaC pipeline
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── modules/staging/
│   └── .github/workflows/
│       ├── lint.yml
│       ├── plan.yml
│       └── apply.yml
│
├── Mini_Project_8/              # Kubernetes Deployment with HPA
│   ├── deployment.yaml
│   ├── hpa.yaml
│   ├── components.yaml
│   └── dockerfile
│
└── README.md
```

---

## Projects Overview

---

### Mini Project 4: CI/CD Pipeline

**Directory:** [`Mini_Project_4`](./Mini_Project_4)

A complete CI/CD pipeline implementation using **GitHub Actions**, built around a Python Calculator application. This project shows how automated pipelines enforce static analysis, testing, and workflow validation on every commit.

#### What it does

- Runs **pytest** unit tests on every push and pull request
- Performs **pylint** static analysis for code quality
- Validates calculator operations before merge

#### Key Files

| File | Purpose |
|------|---------|
| `.github/workflows/CI.yml` | GitHub Actions pipeline definition |
| `Day_3/Project/Calculator/calculator.py` | Calculator module with add and subtract functions |
| `Day_3/Project/Calculator/test_calculator.py` | Pytest test cases |

#### Concepts Covered

- GitHub Actions workflows
- Automated testing with pytest
- Static analysis with pylint
- CI enforcement for pull requests

---

### Mini Project 3: Dockerised To-Do API

**Directory:** [`Mini_Project_3`](./Mini_Project_3)

A production-ready, containerized Flask REST API for to-do management. This project uses multi-stage Docker builds, Gunicorn, and Docker Compose for local orchestration.

#### Architecture

- Multi-stage Docker build for smaller runtime image
- Production server with Gunicorn and non-root container execution
- Local orchestration via Docker Compose

#### Key Files

| File | Purpose |
|------|---------|
| `app.py` | Flask application implementation |
| `Dockerfile` | Multi-stage Docker build definition |
| `docker-compose.yml` | Local service orchestration |
| `requirements.txt` | Python dependency list |

#### Concepts Covered

- Docker and Docker Compose
- Flask API development
- Production-grade containerization patterns
- Build optimization and security best practices

---

### Mini Project 2: Git Workflow Simulator

**Directory:** [`Mini_Project_2`](./Mini_Project_2)

A documentation-first project that models a professional GitHub collaboration workflow including feature branches, pull request standards, code ownership, and release tagging.

#### What it covers

- Branch naming conventions
- Pull request review workflow
- CODEOWNERS-based reviewer assignment
- Standard PR templates and merge discipline

#### Key Files

| File | Purpose |
|------|---------|
| `.github/PULL_REQUEST_TEMPLATE.md` | Pull request checklist and guidance |
| `.github/CODEOWNERS` | Automatic reviewer routing |
| `workflow-simulator.py` | Script illustrating workflow steps |

#### Concepts Covered

- Git branch workflows
- Code review and approval policies
- Release tagging strategy
- Team collaboration best practices

---

### Infrastructure as Code Pipeline

**Directory:** [`IAC_Pipeline`](./IAC_Pipeline)

A Terraform-based infrastructure automation pipeline backed by GitHub Actions for linting, planning, and applying AWS infrastructure changes.

#### Pipeline Flow

- `lint.yml` validates formatting and Terraform syntax
- `plan.yml` generates and reports Terraform plans on PRs
- `apply.yml` applies infrastructure changes after merge

#### Key Files

| File | Purpose |
|------|---------|
| `main.tf` | Root Terraform configuration |
| `variables.tf` | Input parameter definitions |
| `outputs.tf` | Stack outputs |
| `modules/staging/` | Reusable staging infrastructure resources |

#### Concepts Covered

- Terraform modules and reusable design
- GitOps-style infrastructure review
- Automated plan/comment workflow
- AWS resource provisioning via code

---

### Mini Project 8: Kubernetes Autoscaling

**Directory:** [`Mini_Project_8`](./Mini_Project_8)

A Kubernetes autoscaling demo that deploys an Nginx application with a Horizontal Pod Autoscaler backed by Metrics Server.

#### What it includes

- Kubernetes Deployment manifest
- HPA configuration to scale pods based on CPU usage
- Metrics Server integration for resource metrics

#### Key Files

| File | Purpose |
|------|---------|
| `deployment.yaml` | Application deployment manifest |
| `hpa.yaml` | Horizontal Pod Autoscaler configuration |
| `components.yaml` | Metrics Server and supporting resources |

#### Concepts Covered

- Kubernetes Deployment and replica management
- Horizontal Pod Autoscaler (HPA)
- Metrics Server resource metrics
- Container orchestration on Kubernetes

---

## Technology Stack

| Category | Technologies |
|----------|-------------|
| CI/CD | GitHub Actions, pytest, pylint |
| Containerization | Docker, Docker Compose, Gunicorn |
| Infrastructure as Code | Terraform, AWS, reusable modules |
| Orchestration | Kubernetes, HPA, Metrics Server |
| Version Control | Git, branching workflows, CODEOWNERS |
| Application | Python, Flask |

---

## Training Curriculum

This repository reflects the LnT DevOps training program and includes hands-on projects for:

- CI/CD automation
- Dockerized application deployment
- Git workflow collaboration
- Infrastructure automation with Terraform
- Kubernetes autoscaling patterns

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/gauravtiwari2101/LnT_All_Mini-Projects.git
cd LNT_ALL_PROJECTS
```

Open the project you want to explore:

```bash
cd Mini_Project_4
cd Mini_Project_3
cd Mini_Project_2
cd IAC_Pipeline
cd Mini_Project_8
```

Each project directory contains its own README and setup instructions.

---

## Author

**Gaurav Tiwari**
LnT DevOps Training Program

---

*Last Updated: June 2026*
