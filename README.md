# 🚀 Node.js AWS ECS Fargate Deployment


<img width="1420" height="488" alt="image" src="https://github.com/user-attachments/assets/69b212d1-ed89-41a1-ad1a-eaa9cf4cebec" />
<img width="1402" height="481" alt="image" src="https://github.com/user-attachments/assets/b1208613-c4d1-4a2a-8682-623db91be7d7" />


Dockerized Node.js application deployed on AWS ECS Fargate using Amazon ECR for container image storage and Amazon CloudWatch for monitoring and logging.

---

## 📌 Features

- Containerized Node.js application using Docker
- Deployed on AWS ECS Fargate
- Amazon ECR integration for image storage
- CloudWatch logging and monitoring
- ECS Task Definitions and Services
- Publicly accessible deployment

---

## 🛠️ Technologies Used

- Node.js
- Docker
- AWS ECS
- AWS Fargate
- Amazon ECR
- Amazon CloudWatch

---

## 📂 Project Structure

```bash
.
├── Dockerfile
├── app.js
├── package.json
├── package-lock.json
├── Jenkinsfile
├── views/
└── README.md
```

---

## 🐳 Docker Build

Build Docker image:

```bash
docker build -t node-app .
```

Run container:

```bash
docker run -p 8000:8000 node-app
```

---

## ☁️ AWS Deployment Steps

### 1. Push Docker Image to Amazon ECR

```bash
aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <account-id>.dkr.ecr.<region>.amazonaws.com
```

```bash
docker tag node-app:latest <ecr-repo-uri>
```

```bash
docker push <ecr-repo-uri>
```

---

### 2. Create ECS Cluster

- Create ECS Fargate Cluster
- Configure networking
- Attach security groups

---

### 3. Create Task Definition

- Add container image URI
- Configure CPU & Memory
- Configure port mappings
- Add execution role

---

### 4. Run ECS Service / Task

- Launch using Fargate
- Assign public IP
- Access application via public IP

---


---

## 📈 Learning Outcomes

- Docker containerization
- AWS ECS orchestration
- ECS Task Definitions
- AWS networking & security groups
- Cloud deployment fundamentals

---

## 👨‍💻 Author

Talha Khan
