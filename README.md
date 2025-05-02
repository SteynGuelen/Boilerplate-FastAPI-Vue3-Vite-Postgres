# 🚀 Boilerplate FastAPI + Vue 3 + Vite + Postgres

A production-ready boilerplate combining a **FastAPI** backend, **Vue 3** frontend (with **Vite**), and **PostgreSQL** database - fully containerized with **Docker Compose**. Includes authentication ready to go.

Perfect as a starting point for full-stack applications with a clean and scalable setup.

---

## ✨ Features

- **FastAPI** backend
  - Async Python API using FastAPI
  - JWT Authentication fully implemented
  - PostgreSQL connection with SQLAlchemy models and Pydantic schemas
  - User registration and login system included
- **Vue 3** frontend
  - Vite-powered Vue 3 app for fast development
  - Pinia for state management with persisted authentication state
  - Vue Router configured and ready to expand
- **PostgreSQL** database
  - User data storage
  - Easily extendable to other models and relationships
- **Docker Compose** orchestration
  - One-command startup for fullstack development
  - Hot reloading configured for local backend and frontend
- **Preconfigured** for local development and easy production deployment
- **Scalable** project structure
  - Clean separation between backend and frontend
  - API proxying configured in Vite for seamless local requests

---

## 🛠️ Quickstart

Make sure you have **Docker** installed and running.

### Development

1. Clone the repository:
   ```bash
   git clone https://github.com/SteynGuelen/Boilerplate-FastAPI-Vue3-Vite-Postgres.git
   cd Boilerplate-FastAPI-Vue3-Vite-Postgres
   ```

2. Start all services:
   ```bash
   docker compose up --build
   ```

3. Access the services:
   - Frontend: [http://localhost:8088](http://localhost:8088)
   - Backend API: [http://localhost:8000/api](http://localhost:8000/api)
   - Swagger Docs: [http://localhost:8000/docs](http://localhost:8000/docs)

---

If you only want to work on the frontend with hot module reload:

```bash
cd frontend
npm install
npm run dev
```

It will be available at [http://localhost:5173](http://localhost:5173).

---

### Production

1. Build and start production services:
   ```bash
   docker compose -f docker-compose.prod.yml up --build
   ```

2. Access:
   - Frontend: [http://your-server-ip:8088](http://your-server-ip:8088)

---

## 📂 Project Structure

```
.
├── backend/          # FastAPI app
│   ├── app/          # Application code (models, routers, auth, etc.)
│   ├── Dockerfile.dev
│   ├── Dockerfile.prod
│   └── requirements.txt
├── frontend/         # Vue 3 + Vite app
│   ├── src/
│   ├── Dockerfile.dev
│   ├── Dockerfile.prod
│   └── vite.config.js
├── docker-compose.yml
├── docker-compose.prod.yml
└── README.md
```

---

## 🧩 Why This Boilerplate?

This boilerplate was primarily created for my personal projects, so I can easily jumpstart fullstack applications.  
Most public templates had a bit too much, so I created my own.

The focus is on simplicity, extensibility, and real-world usability:
- Clean, minimalistic starting point
- Includes user registration and login out of the box
- Ready for projects that need secure APIs and authenticated frontends
- Easy to deploy without additional setup

---

## 🐛 Known Issues

- Hot Module Reloading (HMR) for the frontend doesn't work properly when using Docker with WSL2 on Windows. (Works fine when running `npm run dev` directly, but no backend then.)
- On very first frontend load, Vue Router might enter a `router-view` container state early. Needs fixing.

---

**Made with ❤️ by a Dutch guy coding from NYC.**
