# SIT737 2025 - Prac5P
## Dockerized Web Application - 737webapp

### Project Overview
This repository contains a simple Node.js web application, **737webapp**, which has been containerized using **Docker** and **Docker Compose**. The project includes a **health check** feature and can be deployed using **Docker Hub**.

---

## Getting Started
### 1. Clone the Repository
```sh
git clone https://github.com/Abhishek-S-28/sit737-2025-prac5p.git
cd sit737-2025-prac5p
```

### 2. Install Dependencies
Ensure you have **Node.js** installed, then run:
```sh
npm install
```

### 3. Run the Application Locally
```sh
node server.js
```
Now visit: **http://localhost:3000**

---

## Docker Implementation
### 1. Build and Run the Docker Container
```sh
docker build -t 737webapp .
docker run -p 3000:3000 737webapp
```

### 2. Run Using Docker Compose
```sh
docker-compose up -d
```

### 3. Verify the Application
Visit: **http://localhost:3000**  
Or run:
```sh
curl http://localhost:3000
```

### 4. Push Docker Image to Docker Hub
```sh
docker tag 737webapp abhishek2806/737webapp:latest
docker push abhishek2806/737webapp:latest
```

---

## Appendix: Implementation Steps
### 1. Web Application (Node.js + Express)
- Created a basic **Express.js** server (`server.js`) that responds with `"Hello from dockerized webapp!"`.

### 2. Dockerization
- **Dockerfile**:
  - Used `node:18` as the base image.
  - Set `/app` as the working directory.
  - Installed dependencies and copied source files.
  - Exposed **port 3000**.
  - Used `CMD ["node", "server.js"]` to run the app.

### 3. Docker Compose
- Created `docker-compose.yml` with:
  - Service named `web`.
  - Port mapping (`3000:3000`).
  - Health check to monitor service availability.

### 4. Deployment
- Pushed the image to **Docker Hub** (`abhishek2806/737webapp`).
- Ensured container restarts automatically if it fails.

---

## Submission
- **GitHub Repo:** [sit737-2025-prac5p](https://github.com/Abhishek-S-28/sit737-2025-prac5p)
- **Docker Image:** `docker pull abhishek2806/737webapp`

---

## Conclusion
This project successfully demonstrates how to **containerize a Node.js application using Docker**, implement **health checks**, and deploy it using **Docker Compose and Docker Hub**.

