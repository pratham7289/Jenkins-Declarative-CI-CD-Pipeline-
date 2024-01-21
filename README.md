
# CI/CD Pipeline for Django Notes App

## Overview

This repository contains the Jenkins pipeline script (written in Groovy) for Continuous Integration and Continuous Deployment (CI/CD) of a Django Notes App. The pipeline automates the cloning of the code, building a Docker image, pushing it to Docker Hub, and deploying the application on an EC2 instance in AWS using Docker Compose.

## Pipeline Stages

1. **Clone Code:**
   - This stage clones the code from the GitHub repository.

2. **Build:**
   - This stage builds a Docker image for the Django Notes App.

3. **Push to Docker Hub:**
   - The Docker image is tagged and pushed to Docker Hub.

4. **Deploy:**
   - The deployed container on the EC2 instance is updated using Docker Compose.

## Prerequisites

Before running the pipeline, ensure the following:

- Jenkins is set up and configured.
- Docker is installed on the Jenkins server.
- AWS credentials are configured in Jenkins.
- Docker Hub credentials are set up in Jenkins.

## Pipeline Configuration

The pipeline script is written in declarative syntax using Groovy and includes the following stages:

- **Clone Code:**
  - Git is used to clone the code from the specified GitHub repository.

- **Build:**
  - Docker is used to build the Docker image named `my-app`.

- **Push to Docker Hub:**
  - The Docker image is tagged and pushed to Docker Hub using provided credentials.

- **Deploy:**
  - Docker Compose is used to manage the deployment on an EC2 instance in AWS.

## How to Run

1. Set up Jenkins and configure the necessary credentials.
2. Create a new pipeline job in Jenkins.
3. Copy and paste the provided Groovy script into the pipeline configuration.
4. Save the pipeline job and manually trigger the build, or set up webhooks for automatic triggering.

## Notes

- Ensure that the specified AWS EC2 instance is running and accessible.
- Make sure Docker Compose is installed on the EC2 instance.
- Adjust the GitHub repository URL and branch as needed.
- Customize Docker image names and tags according to your requirements.

---

Feel free to customize the README according to your specific project details and add any additional information that might be relevant.