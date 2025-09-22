# nodejs-cicd-demo1
A demo Node.js web application integrated with a CI/CD pipeline using GitHub Actions and Docker. The workflow automates testing, building, and pushing Docker images to DockerHub upon every push to the main branch.

## 📦 Technologies Used

- Node.js
- Express.js
- Docker
- GitHub Actions (CI/CD)
- DockerHub (for image storage)

## 🎯 Objective

Set up a complete CI/CD pipeline that:

1. Runs on every push to the `main` branch
2. Installs dependencies
3. Runs tests
4. Builds a Docker image
5. Pushes the Docker image to DockerHub

## 📁 Project Structure
nodejs-cicd-demo/
├── app.js
├── package.json
├── Dockerfile
├── .dockerignore
├── .gitignore
└── .github/
└── workflows/
└── main.yml


## ⚙️ How CI/CD Works

- Trigger: Push to `main` branch
- Environment: Ubuntu runner via GitHub Actions
- Steps:
  - Checkout code
  - Install Node.js and dependencies
  - Run tests
  - Build Docker image
  - Login to DockerHub
  - Push image to DockerHub

## 🐳 Docker

### Build the Docker image locally:

```bash
docker build -t your-dockerhub-username/nodejs-cicd-demo .

