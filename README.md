SIT737 2025 - Prac5P
Dockerized Web Application - 737webapp
📌 Project Overview
This repository contains a simple Node.js web application, 737webapp, which has been containerized using Docker and Docker Compose. The project includes a health check feature and can be deployed using Docker Hub.

🚀 Getting Started
1️⃣ Clone the Repository
sh
Copy
Edit
git clone https://github.com/Abhishek-S-28/sit737-2025-prac5p.git
cd sit737-2025-prac5p
2️⃣ Install Dependencies
Ensure you have Node.js installed, then run:

sh
Copy
Edit
npm install
3️⃣ Run the Application Locally
sh
Copy
Edit
node server.js
Now visit: http://localhost:3000

🐳 Docker Implementation
1️⃣ Build and Run the Docker Container
sh
Copy
Edit
docker build -t 737webapp .
docker run -p 3000:3000 737webapp
2️⃣ Run Using Docker Compose
sh
Copy
Edit
docker-compose up -d
3️⃣ Verify the Application
Visit: http://localhost:3000
Or run:

sh
Copy
Edit
curl http://localhost:3000
4️⃣ Push Docker Image to Docker Hub
sh
Copy
Edit
docker tag 737webapp abhishek2806/737webapp:latest
docker push abhishek2806/737webapp:latest
📜 Appendix: Implementation Steps
✅ 1. Web Application (Node.js + Express)
Created a basic Express.js server (server.js) that responds with "Hello from dockerized webapp!".

✅ 2. Dockerization
Dockerfile:

Used node:18 as the base image.

Set /app as the working directory.

Installed dependencies and copied source files.

Exposed port 3000.

Used CMD ["node", "server.js"] to run the app.

✅ 3. Docker Compose
Created docker-compose.yml with:

Service named web.

Port mapping (3000:3000).

Health check to monitor service availability.

✅ 4. Deployment
Pushed the image to Docker Hub (abhishek2806/737webapp).

Ensured container restarts automatically if it fails.

⚠️ Fixing Git Push Issues
If you get an error while pushing, follow these steps:

1️⃣ Fetch the latest changes from remote
sh
Copy
Edit
git fetch origin
2️⃣ Pull the latest changes and rebase
sh
Copy
Edit
git pull --rebase origin main
3️⃣ Push the changes
sh
Copy
Edit
git push origin main
4️⃣ (If necessary) Force push to overwrite remote (⚠️ Use with caution)
sh
Copy
Edit
git push --force origin main
📩 Submission
GitHub Repo: sit737-2025-prac5p

Docker Image: docker pull abhishek2806/737webapp

🎯 Conclusion
This project successfully demonstrates how to containerize a Node.js application using Docker, implement health checks, and deploy it using Docker Compose and Docker Hub.
