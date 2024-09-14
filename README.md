# Static Website Deployment

This project demonstrates the deployment of a static website using Jenkins, Docker, and AWS ECR.

## Files

- `Dockerfile`: Configures the Docker image to use Apache HTTP Server to serve the static website.
- `Jenkinsfile`: Jenkins pipeline configuration for building, pushing the Docker image to AWS ECR, and deploying it.
- `.gitignore`: Specifies which files and directories should be ignored by Git.

## Setup

1. **Jenkins**: Configure a Jenkins pipeline to use the `Jenkinsfile`.
2. **AWS ECR**: Set up an AWS ECR repository to store Docker images.
3. **Docker**: Ensure Docker is installed on your Jenkins server.

## Instructions

1. **Build and Run Docker Container**:
   ```bash
   docker build -t my-static-website .
   docker run -itd --name my-website-container -p 8081:80 my-static-website
