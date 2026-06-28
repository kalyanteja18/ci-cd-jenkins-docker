# ci-cd-jenkins-docker

# CI/CD Pipeline Automation with Jenkins & Docker
Automated CI/CD pipeline using Jenkins and Docker to build and deploy a Python web application.

## Tech Stack
- Jenkins (containerized via Docker)
- Docker
- Python (Flask)
- Git & GitHub

## Pipeline Flow
Code Push → GitHub → Jenkins detects → Docker build → App deployed

## Project Structure
ci-cd-jenkins-docker/

├── app.py

├── Dockerfile

├── Jenkinsfile

└── requirements.txt

## How to Run Locally
```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```
