# Dockerized Node.js App

This is a simple Node.js application that runs inside a Docker container. The app listens on a specified port and returns a greeting message when accessed.

## Features
- Lightweight Express.js server
- Dockerized for easy deployment
- Configurable port using environment variables

## Prerequisites
- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)

## Installation
### 1. Clone the Repository
```sh
git clone https://github.com/your-username/dockerized-node-app.git
cd dockerized-node-app
```

### 2. Install Dependencies
```sh
npm install
```

### 3. Run Locally
```sh
node server.js
```

## Docker Setup
### 1. Build the Docker Image
```sh
docker build -t your-dockerhub-username/my-node-app .
```

### 2. Run the Container
```sh
docker run -p 3000:3000 your-dockerhub-username/my-node-app
```
Now visit `http://localhost:3000/` in your browser.

## Deploying to Docker Hub
### 1. Log in to Docker Hub
```sh
docker login
```

### 2. Tag the Image
```sh
docker tag my-node-app your-dockerhub-username/my-node-app
```

### 3. Push to Docker Hub
```sh
docker push your-dockerhub-username/my-node-app
```

## CI/CD with GitHub Actions
This project uses GitHub Actions to build and push the Docker image automatically.
Make sure you add the following secrets in **GitHub → Repo Settings → Secrets & Variables → Actions**:
- `DOCKER_USERNAME`: Your Docker Hub username
- `DOCKER_PASSWORD`: Your Docker Hub password or access token

## License
This project is open-source and available under the [MIT License](LICENSE).

---

Happy Coding! 🚀

