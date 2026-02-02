# Monitoring Stack (Prometheus + Grafana)

This repository contains a configuration for deploying a system monitoring stack in Docker containers using Infrastructure as Code (IaC) principles.

## 🚀 Overview
The stack is built with Docker Compose and provides real-time infrastructure visibility:
* **Prometheus** — Metric collection and time-series database.
* **Grafana** — Data visualization and alerting dashboard.
* **Node Exporter** — Host-level metric exporter (CPU, RAM, Disk, Network).

## 🛠 Technology Stack
* **Runtime:** Docker / Docker Compose
* **OS:** Linux (Ubuntu 24.04 LTS tested)
* **Monitoring:** Prometheus, Grafana, Node Exporter

## 📦 Deployment

1. Clone the repository:
   ```
   git clone https://github.com/your-username/monitoring-stack.git
   cd monitoring-stack
   ```

2. Start the stack:
```
docker-compose up -d
```

3. Create a .env file from .env.example and fill in your credentials.

4. Access the services:
   * **Grafana:** http://localhost:3000
   * **Prometheus:** http://localhost:9090

## 📊 Configuration Details
* **Prometheus:** Configured via prometheus.yml to scrape targets every 15 seconds.
* **Dashboards:** Node Exporter metrics are automatically discovered as a data source in Prometheus.
* **Persistence:** Data is stored in Docker volumes to ensure persistence across container restarts.

---
*Developed as part of HomeLab infrastructure and systems administration practice.*
