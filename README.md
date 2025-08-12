# react-next-devops
# Local Development Environment – React Frontend & Next.js Backend with Docker & Ansible

This repository contains a fully automated local development environment, orchestrated with Docker Compose and provisioned via Ansible.  
It’s tailored for **rapid development** with instant code reloading, as well as **production-grade deployment** with health checks, restarts, and multi-architecture image builds.

---

## 📂 Project Structure

```bash
.
├── ansible/
│   ├── roles/
│   │   ├── docker/
│   │   ├── mysql/
│   │   └── app_deploy/
│   ├── build_and_push.yml
│   └── deploy.yml
├── backend/
│   ├── package.json
│   ├── server.js
│   └── ...
├── frontend/
│   ├── package.json
│   ├── pages/
│   │   └── index.js
│   └── ...
├── docker-compose.yml
├── .env
├── README.md
└── screenshots/

browsImage Size Analysis
Backend: 124MB → reduced to 54MB using multi-stage builds.
Frontend: 102MB → reduced to 48MB by pruning dev dependencies and using Alpine base images.
Database: Standard MySQL 8.0 image, unchanged.
Strategies Used:
Multi-stage builds for backend & frontend.
Alpine Linux base images.
Pruned node_modules in production builds.
Cached dependencies separately from app code.er_view.png
    └── terminal_output.png
