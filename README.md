# nginx-docker-lab 🚀

A hands-on Docker project that sets up a custom NGINX container with persistent volumes and orchestration using Docker Compose. Built and deployed on an Ubuntu VM hosted in Azure, as part of a personal DevOps/SRE learning journey.

---

## 📁 Project Structure
nginx-docker-lab/ ├── docker-compose.yml # Defines the NGINX service with bind mount ├── site/ │ └── index.html # Custom HTML page served by NGINX

---

## 🧠 What You'll Learn

- How to create and build a custom Docker image with NGINX
- How to bind a local directory as a volume to persist website content
- How to use Docker Compose for local container orchestration
- How to expose and access services through specific ports
- How to configure NSG (Network Security Group) rules in Azure

---

## ⚙️ How to Run

### Option 1: Run with Docker CLI and volume

```bash
docker run -d \
  --name nginx-volume \
  -p 8082:80 \
  -v $(pwd)/site:/usr/share/nginx/html \
  nginx
```
Then open: http://your-vm-ip:8082
________________________________________
Option 2: Run with Docker Compose
```bash
docker compose up -d
```
Then open: http://your-vm-ip:8083

🔐 Make sure the corresponding ports (8082, 8083) are allowed in your Azure NSG rules.
________________________________________
🌍 Environment
•	Ubuntu 22.04 LTS (Azure VM)
•	Docker CE + Docker Compose
•	NGINX (official image)
•	Git + GitHub
________________________________________
🏁 Next Steps (Ideas)
•	Add backend container (e.g. Node.js or Python) to compose file
•	Add named volumes and test persistence across rebuilds
•	Host this static site via HTTPS using NGINX + Let's Encrypt
•	Publish image to Docker Hub
•	Set up CI/CD pipeline using GitHub Actions
•	Deploy the stack to AKS or Azure Container Apps
________________________________________
🤝 Author
Daniel Gil
💻 DevOps/SRE in Progress
📍 Hosted on GitHub
