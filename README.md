# TaskMaster (CI/CD Demonstration)

## Overview

TaskMaster is a lightweight Spring Boot application created to demonstrate a fully automated CI/CD pipeline, Docker containerization, and modern DevOps best practices.  
The primary focus of this project is not application complexity, but the implementation of an end-to-end DevOps workflow suitable for real-world systems.

---

## Project Goal

The objective of this project is to showcase a modern DevOps lifecycle, including:

- **Containerization:** Packaging the application using Docker  
- **Automation:** Continuous integration with automated build and test execution on every commit  
- **Infrastructure as Code:** Environment management using Docker Compose  

This repository serves as a proof-of-concept for production-ready CI/CD practices.

---

## DevOps Pipeline Workflow

The project implements a standard continuous integration and delivery pipeline:

1. **Code Commit**  
   Developer pushes code changes to GitHub.

2. **Build and Test**  
   CI server automatically compiles the Java application and executes JUnit tests.

3. **Docker Image Build**  
   A Docker image is created from the packaged artifact.

4. **Deployment**  
   The container is deployed to the target environment (local server, cloud VM, or platform services such as AWS or Render).

---

## Technology Stack

- **Backend:** Java 21, Spring Boot  
- **Containerization:** Docker, Docker Compose  
- **CI/CD:** GitHub Actions or Jenkins  
- **Build Tool:** Maven  

---

## Running the Application with Docker

You do not need Java installed locally. Docker is sufficient.

### Clone the Repository

```bash
git clone https://github.com/avadhutmali/taskmaster.git
cd TaskMaster
```

### Run Using Docker Compose

```bash
docker-compose up --build
```

### Access the Application

The API will be available at:

```
http://localhost:8080/tasks
```

---

## Application Features

- **Create Task:** Add a new task  
- **View Tasks:** Retrieve all existing tasks  
- **Delete Task:** Remove completed tasks  

> Note: Data is persisted using an H2 in-memory database by default. A MySQL container can be added for persistent storage.

---

## Project Structure

```
TaskMaster/
├── src/               # Java source code
├── Dockerfile         # Container image definition
├── docker-compose.yml # Multi-container configuration
├── .github/           # CI/CD pipeline configuration
└── pom.xml            # Maven dependencies
```

---

## Future DevOps Improvements

- Deploying the application to a Kubernetes (K8s) cluster  
- Integrating Prometheus and Grafana for container monitoring and observability  

---
