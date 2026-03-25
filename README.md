🚀 Finance Dashboard Deployment using DevOps

This project demonstrates an end-to-end DevOps implementation where a Finance Dashboard web application is containerized using Docker, deployed on AWS EC2, provisioned using Terraform, and automated using a CI/CD pipeline with GitHub Actions.

---

📌 Project Overview

The Finance Dashboard is a simple web-based application designed to display financial data in a structured format.

This project focuses on deployment and automation, showcasing how modern DevOps tools can be used together to:

- Automate infrastructure setup
- Containerize applications
- Deploy on cloud platforms
- Implement continuous integration and deployment

---

🛠️ Tech Stack

- Frontend: HTML, CSS
- Containerization: Docker
- Cloud Platform: AWS EC2
- Infrastructure as Code: Terraform
- CI/CD: GitHub Actions

---

📂 Project Structure

.
├── Dockerfile
├── index.html
├── styles.css
├── main.tf
├── variables.tf
├── outputs.tf
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml

---

🏗️ High-Level Architecture

User → Browser → AWS EC2 → Docker Container → Finance Dashboard

Explanation:

- User accesses the application via browser
- AWS EC2 acts as the hosting server
- Docker container runs the application
- CI/CD pipeline automates deployment
- Terraform provisions infrastructure

---

⚙️ Key Features

- Dockerized application for consistent environment
- Automated deployment using CI/CD
- Infrastructure provisioning using Terraform
- Cloud hosting on AWS EC2
- Live application accessible via public IP

---

🚀 Deployment Steps

1️⃣ Clone the Repository

git clone https://github.com/Krati2251/Tracker.git
cd Tracker

---

2️⃣ Terraform Setup (Infrastructure)

terraform init
terraform plan
terraform apply

This creates:

- EC2 Instance
- Security Group

---

3️⃣ Docker Setup (Application Deployment)

docker build -t finance-app .
docker run -d -p 8501:80 --name finance-app finance-app

---

4️⃣ Access the Application

http://<EC2_PUBLIC_IP>:8501

Example:

http://13.60.252.90:8501

---

🔄 CI/CD Pipeline (GitHub Actions)

The CI/CD pipeline automates deployment whenever code is pushed to the repository.

Workflow:

1. Developer pushes code to GitHub
2. GitHub Actions pipeline triggers
3. Connects to EC2 using SSH
4. Pulls latest code
5. Stops existing Docker container
6. Builds new Docker image
7. Runs updated container

---

🔐 Security Configuration

- Port 22 → SSH access
- Port 8501 → Application access

Security group ensures controlled access to the EC2 instance.

---

⚠️ Challenges Faced

- AWS CLI and credential configuration issues
- SSH key authentication errors
- Docker permission issues on EC2
- GitHub Actions YAML configuration errors
- CI/CD pipeline debugging
- Port mapping mismatch in Docker

---

✅ Solutions Implemented

- Configured IAM and access keys properly
- Correctly set up SSH keys for EC2 access
- Added user to Docker group for permissions
- Fixed YAML structure in GitHub Actions workflow
- Corrected Docker port mapping (8501 → 80)
- Verified container logs and deployment

---

🎯 Outcome

- Fully automated CI/CD pipeline
- Live application deployed on AWS EC2
- Scalable and repeatable infrastructure
- Real-world DevOps implementation

---

📸 Demo

The application is live and accessible via:

http://<EC2_PUBLIC_IP>:8501

---


📌 Conclusion

This project demonstrates a complete DevOps lifecycle including:

- Infrastructure provisioning
- Application containerization
- Cloud deployment
- CI/CD automation

It reflects practical, industry-level implementation of modern DevOps practices.

---
