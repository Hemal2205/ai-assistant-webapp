# AI Assistant Web App

A full-stack AI-powered assistant platform with real-time task execution, ML/NLP integration, and scalable deployment options.

---

## Features

- **Backend**: Flask + Celery + Redis + Socket.IO
- **Frontend**: React + Zustand + Route Guards
- **Security**: Role-based access, login/logout flow
- **Monitoring**: Prometheus & Grafana (optional)
- **CI/CD**: GitHub Actions (pre-configured)
- **Deployable on**: EC2, GKE, Azure Web Apps
- **Single-command launch**: Docker Compose

---

## How to Run (One Command Setup)

### Prerequisites
- Docker + Docker Compose

### Steps

```bash
git clone https://github.com/your-username/ai-assistant-webapp.git
cd ai-assistant-webapp
docker-compose up --build
```

- Frontend: [http://localhost:3000](http://localhost:3000)
- Backend: [http://localhost:5000](http://localhost:5000)
- Default login: `admin` / `password`

---

## Folder Structure

```
ai-assistant-project/
├── backend/
│   ├── app.py
│   ├── config.py
│   ├── routes/
│   ├── controllers/
│   ├── tasks/
│   ├── utils/
│   ├── tests/
│   └── requirements.txt
├── frontend/
│   └── src/
│       ├── App.js
│       ├── index.js
│       ├── pages/
│       ├── components/
│       └── store/
├── Dockerfile.backend
├── Dockerfile.frontend
├── docker-compose.yml
└── .github/
    └── workflows/
        └── deploy.yml
```

---

## API Endpoints

- `POST /api/login` - Authenticate user
- `GET /api/logout` - Logout user
- `POST /api/task` - Submit async task (admin-only)

---

## Deployment Options

- **EC2**: systemd + Gunicorn + Nginx (see Cloud Deployment Guide)
- **GKE**: `k8s-deployment.yaml` + `k8s-service.yaml`
- **Azure Web App**: Docker image + `az webapp up`

---

## Monitoring

To enable Prometheus metrics:
- Flask app exposes default metrics
- Optionally deploy Grafana & Prometheus containers

---

## License

MIT