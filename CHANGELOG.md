# 📘 CHANGELOG – nginx-docker-lab

This file documents the key steps taken throughout the project, from setting up the environment to publishing everything on GitHub.

---

## 📅 [Day 1] — Initial Setup and Tests

- 🔧 Created Ubuntu 22.04 VM on Azure
- 🐳 Installed Docker and Docker Compose
- 🌐 Opened ports in the NSG: 8081, 8082, 8083
- ✅ Tested default NGINX container on port 8081

---

## 📦 Stage 1 — Custom Docker Image with NGINX

- Created custom `index.html` with emoji
- Wrote `Dockerfile` based on official NGINX image
- Built the image as `daniel/nginx-personalizado`
- Launched the container on port 8081

---

## 🗃️ Stage 2 — Local Volume with Docker

- Created the `~/meusite` directory with persistent HTML
- Ran the `nginx-volume` container with bind mount
- Port 8082 opened and tested externally
- Live HTML reload confirmed via local file edits

---

## ⚙️ Stage 3 — Docker Compose with Volume

- Set up project structure in `~/stack-nginx-compose/site`
- Created `docker-compose.yml` (no `version` field needed)
- Orchestrated NGINX container on port 8083
- Successfully tested page in browser

---

## 🧑‍💻 Stage 4 — Git & GitHub Deployment

- Created GitHub account (`gil-daniel`)
- Initialized local Git repository
- Faced token/HTTPS issues → switched to SSH
- Successfully pushed project using SSH key
- Added a well-formatted English `README.md`

---

## 🏁 Current Status

- [x] Project versioned and hosted on GitHub
- [x] Documentation added with clear objectives and command reference
- [x] Docker-based infrastructure running on Azure VM
- [x] Portfolio-ready foundation in place 🚀

---


