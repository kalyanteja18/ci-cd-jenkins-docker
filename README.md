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



## Pipeline Output
App verified via: `docker exec jenkins curl http://localhost:5000`
Response: "CI/CD Pipeline Working! Deployed via Jenkins & Docker"

<img width="780" height="116" alt="image" src="https://github.com/user-attachments/assets/7ad8f91b-dbd7-4b33-9c3d-e283798b40af" />

