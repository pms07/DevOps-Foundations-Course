# Multi-Container Docker Application with CI/CD: Calculator App Project

## Complete Project Instructions
Refer to the complete project instructions here: [DevOps Foundations Course/Project](https://github.com/shiftkey-labs/DevOps-Foundations-Course/tree/master/Project)

#### Submission by - *Pavankumar Sakhare *

---

## Project Overview

- *Brief project description:*
  This project is a calculator application with a *React frontend* and a *Python Flask backend*. It is containerized using Docker, orchestrated with Docker Compose, and features a CI/CD pipeline for automation.

- *implemention details:*
  - *Frontend Dockerfile*: To containerize the React application.
  - *Backend Dockerfile*: To containerize the Flask API.
  - *Docker Compose YAML*: To set up and manage multi-container services.
  - *GitHub Actions Workflow*: To automate CI/CD processes.

---

## Docker Implementation

### Backend Dockerfile
- Uses python:3.9-slim as the base image.
- Installs dependencies from requirements.txt.
- Exposes port 5000 for the Flask API.
- Runs the app using python app.py.

### Frontend Dockerfile
- Uses node:14-alpine as the base image.
- Installs dependencies and builds the React app.
- Exposes port 3000 for the React application.
- Runs the app using npm start.

---

## Docker Compose Configuration

- *Services*:
  - *frontend*: React app, port 3000.
  - *backend*: Flask API, port 5000.

- *Networking*: Services communicate using Docker Compose’s default network.

---

## CI/CD Pipeline

### Workflow
- *Triggers*: On push or pull_request to master branch.
- *Stages*:
  1. Build and push Docker images to Docker Hub.
  2. Deploy Docker Compose configuration to the cloud.

---

## Lessons Learned

- Docker containers provide a lightweight and isolated environment for development and deployment.
- Docker Compose simplifies the management of multi-container services.
- GitHub Actions provides a flexible and scalable CI/CD pipeline.
- Docker ensures consistent environments across deployments.
- CI/CD pipelines streamline and automate the development workflow.

---

## Future Improvements

- We can add more unit tests to the Flask API.
- We can add integration tests to the frontend and backend.
- We can add more complex calculations to the calculator app.
- We can add a database to store user data.
- We can add authentication and authorization to the Flask API.
- Optimize Docker images using multi-stage builds.
- Expand CI/CD to include automated deployment to the cloud.

---