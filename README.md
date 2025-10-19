# 🐍 Creating A Simple Web Application Using Python, Flask, and Redis with Docker Compose

This project demonstrates how to build and deploy a simple **Flask web application** that uses **Redis** as a database to count website visits.  
The app is containerized using **Docker** and orchestrated using **Docker Compose**.

---

## 🔧 Project Overview

- **Frontend/Backend:** Flask (Python Framework)
- **Database:** Redis (In-memory data store)
- **Containerization:** Docker & Docker Compose
- **Goal:** Count and display the number of visits to the web app.

---

## 🧱 Project Structure

Flask-Redis-DockerCompose-App/
│
├── app.py # Flask Application
├── requirements.txt # Python Dependencies
├── Dockerfile # Docker Image for Flask App
├── docker-compose.yml # Multi-container Configuration
├── README.md # Documentation
└── templates/
└── index.html # HTML Template for Web UI
---


---

## 🚀 Step-by-Step Setup

### 🔹 Step 1: Clone the Repository

```bash
git clone https://github.com/MenaMagdyHalem/Flask-Redis-DockerCompose-App.git
cd Flask-Redis-DockerCompose-App
```

##🔹 Step 2: Build and Start the Application
```bash
docker-compose up -d --build
```

##🔹 Step 3: Access the Application

Once the containers are running, open your browser and go to: <br>

👉 http://localhost:5000 <br>

You’ll see a webpage showing how many times the page has been visited.

## 🔹 Step 4: Check Running Containers
```bash
docker ps
CONTAINER ID   IMAGE               COMMAND                  PORTS                    NAMES
a1b2c3d4e5f6   flask-redis-app     "python app.py"          0.0.0.0:5000->5000/tcp   flask-redis-dockercompose-app_web_1
b2c3d4e5f6g7   redis:alpine        "docker-entrypoint.s…"   6379/tcp                 flask-redis-dockercompose-app_redis_1

```

## 🔹 Step 5: Stop the Application
To stop and remove the containers:
```bash
docker-compose down
```
---

##🧠 How It Works
Flask App (app.py) connects to the Redis service.
Redis stores a key called hits that tracks the visit count.
Each time the user visits the page, Flask increments the counter and displays the total.
Docker Compose manages both containers — web and redis.
---

## 👨‍💻 Author
Mena Magdy Halem
Instructor & DevOps Engineer


