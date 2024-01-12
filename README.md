# AFTAS Project Docker Integration Presentation

## Overview
In this phase of the AFTAS project, we successfully integrated Docker to streamline the deployment process and enhance the overall execution of the application. The integration focused on combining the Spring Boot backend and Angular frontend into a single Docker container, providing a simple and cohesive deployment solution.

## Docker Commands

### Backend Docker Image Creation

Navigate to the backend directory and build the Docker image:

```bash
cd aftas
docker build -t backend-image .
```

### Frontend  Docker Image Creation

```bash
# Navigate to the frontend directory
cd aftas-frontend

# Build the Docker image
docker build -t frontend-image .
```
### Docker Compose
```bash
# Run Docker Compose to orchestrate the deployment
docker-compose up
```

## Docker Configuration Files

### Backend Dockerfile
- Specify the base image
- Set the working directory
- Copy the JAR file into the container
- Expose the port
- Command to run the application

### Frontend Dockerfile
- Specify the base image
- Set the working directory
- Copy package.json and package-lock.json files
- Install dependencies
- Copy the application files
- Build the application

### Docker Compose (docker-compose.yml)
- Version specification
- Backend service configuration
  - Build context and Dockerfile location
  - Port mapping 
- Frontend service configuration
  - Build context and Dockerfile location
  - Port mapping
  - Dependency on the backend service

## Conclusion
The Docker integration successfully encapsulates the AFTAS application into a unified container, simplifying deployment and ensuring smooth execution. The provided commands and configuration details enable seamless image creation and deployment, facilitating a more efficient development and deployment process.