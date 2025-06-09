# 📊 Flask Monitoring with Docker, Prometheus, and Grafana

A complete DevOps monitoring project that runs on an AWS EC2 instance using Docker Compose. It includes a simple Flask application monitored using Prometheus and visualized via Grafana.

---

## 🧰 Tech Stack & Tools

- **AWS EC2 (Ubuntu 22.04)** – Cloud host for deployment
- **Flask** – Lightweight Python web application
- **Docker** – Containerization of all services
- **Docker Compose** – Multi-container orchestration
- **Prometheus** – Metrics collection and monitoring
- **Node Exporter** – System metrics exporter for Prometheus
- **Grafana** – Real-time metrics dashboard
- **Git & GitHub** – Version control and code hosting

---

## 🏗️ Architecture Overview

```
User --> Flask App (port 5000)
                   ↓
        Prometheus <---- Node Exporter (port 9100)
             ↓
         Grafana (port 3000)
```

---

## 🚀 How to Run

### 1. Clone or Create Project Directory on EC2
```bash
mkdir flask-monitoring && cd flask-monitoring
```

### 2. Create the Following Files
- `app.py`
- `requirements.txt`
- `Dockerfile`
- `prometheus.yml`
- `docker-compose.yml`

(Refer to the code section or guide for file contents)

### 3. Run the Docker Stack
```bash
docker-compose up -d
```

### 4. Access Services
- Flask App → `http://<EC2-IP>:5000`
- Prometheus → `http://<EC2-IP>:9090`
- Grafana → `http://<EC2-IP>:3000`
- Node Exporter → `http://<EC2-IP>:9100/metrics`

Login to Grafana with:
- **Username**: `admin`
- **Password**: `admin`

> 📌 Add Prometheus as the Grafana data source.

---

## 🗃️ GitHub Setup
```bash
git init
git add .
git commit -m "Initial commit - Flask + Docker + Prometheus + Grafana"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/flask-monitoring.git
git push -u origin main
```

---

## 📬 Contact
**Author:** Priyanshu Tripathi  
[GitHub](https://github.com/Priyanshutripathi555)
