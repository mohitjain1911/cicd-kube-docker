# Continuous Delivery for Docker Containers

## Project Overview

In this project, we aim to implement a continuous delivery pipeline for Docker containers using tools like Jenkins, Docker Hub, Helm, and Kubernetes. The primary focus is on achieving automated building, testing, and deployment of Docker images to a Kubernetes Cluster.

## Project Objectives

1. **Continuous Integration Setup:**
   - Establish a Jenkins-SonarQube-Nexus setup for continuous integration.
   - Set up Docker Hub for managing Docker images.

2. **Docker Engine Integration:**
   - Configure Docker engine in Jenkins for seamless Docker image building.
   - Install necessary Jenkins plugins for Docker pipeline support.

3. **Kubernetes Cluster Creation:**
   - Create a Kubernetes Cluster using Cops on an EC2 instance.
   - Install Helm in the Cops VM for managing Kubernetes applications.

4. **Helm Charts Creation and Testing:**
   - Develop Helm charts with variables for application images.
   - Test Helm charts in a Kubernetes cluster, ensuring proper functionality.

5. **Jenkins Pipeline Configuration:**
   - Create a declarative Jenkins pipeline code for the entire continuous delivery process.
   - Incorporate build, test, Docker image creation, and Helm chart deployment stages.

6. **Git Repository Update:**
   - Update the Git repository with Helm charts, Dockerfile for the application image, and Jenkinsfile for the pipeline code.

7. **Jenkins Job Creation:**
   - Set up a Jenkins job for the created pipeline.
   - Run and test the Jenkins job to validate the continuous delivery pipeline.

## Project Scenario

The scenario involves a microservices architecture where developers make frequent code changes. The goal is to automate the entire process, from building Docker images to deploying them in a Kubernetes Cluster. This setup ensures that as developers commit code changes, an automated pipeline builds, tests, and deploys the updated Docker images.

## Project Solution

To address the challenges of manual deployment and time-consuming processes, we implement a continuous delivery pipeline. The pipeline involves Jenkins fetching code changes from the Git repository, running tests, analyzing code quality with SonarQube, building Docker images, and deploying them using Helm charts on a Kubernetes Cluster.

## Tools Used

- **Jenkins:** CI/CD server for orchestrating the continuous delivery pipeline.
- **SonarQube:** Code analysis server for ensuring code quality.
- **Nexus:** Repository manager for storing artifacts.
- **Docker Hub:** Docker image repository for hosting Docker images.
- **Helm:** Kubernetes package manager for deploying applications.
- **Kubernetes Cluster (Cops):** Container orchestration tool for managing Docker containers.
- **Git:** Version control system for tracking code changes.
- **Maven:** Build tool for Java applications.
- **Docker Engine:** Containerization platform for building and running Docker images.

## Project Execution Flow

1. **Continuous Integration Setup:**
   - Configure Jenkins, SonarQube, and Nexus for continuous integration.
   - Set up Docker Hub for Docker image repository.

2. **Docker Engine Integration:**
   - Integrate Docker engine with Jenkins.
   - Install necessary Jenkins plugins for Docker pipeline support.

3. **Kubernetes Cluster Creation:**
   - Create a Kubernetes Cluster using Cops on an EC2 instance.
   - Install Helm in the Cops VM for Kubernetes application management.

4. **Helm Charts Creation and Testing:**
   - Develop Helm charts for the application stack.
   - Test Helm charts in a Kubernetes Cluster.

5. **Jenkins Pipeline Configuration:**
   - Create a declarative Jenkins pipeline code with stages for building, testing, and deploying.
   - Incorporate Docker image building and Helm chart deployment steps.

6. **Git Repository Update:**
   - Update the Git repository with Helm charts, Dockerfile, and Jenkinsfile.

7. **Jenkins Job Creation:**
   - Set up a Jenkins job for the continuous delivery pipeline.
   - Run and test the Jenkins job to validate the pipeline.

## Conclusion

By implementing this continuous delivery pipeline, the project aims to automate the deployment of Docker containers, ensuring faster and more reliable application updates in a microservices architecture. The integration of Jenkins, Docker, Helm, and Kubernetes provides a robust foundation for efficient continuous delivery.

## Prerequisites

- JDK 1.8 or later
- Maven 3 or later
- Docker installed on Jenkins
- Docker Hub account
- Kubernetes Cluster (Cops setup)
- Helm installed on the Cops VM
- Git installed
- SonarQube server configured

## Technologies
- Jenkins
- SonarQube
- Nexus
- Docker
- Helm
- Kubernetes
- Git
- Maven
- Docker Hub

## Database
Here, we used MySQL as the database.
MySQL DB Installation Steps for Linux Ubuntu 14.04:
- `$ sudo apt-get update`
- `$ sudo apt-get install mysql-server`

Look for the file:
- `/src/main/resources/accountsdb`
- `accountsdb.sql` is a MySQL dump file. Import this dump to the MySQL DB server:
  - `$ mysql -u <user_name> -p accounts < accountsdb.sql`