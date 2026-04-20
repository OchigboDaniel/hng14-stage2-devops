# hng14-stage2-devops

# HNG Stage 2 DevOps Project

## Overview
This project is a microservices job processing system made up of:

- Frontend (Node.js)
- API (FastAPI)
- Worker (Python)
- Redis (message queue)

---

## Architecture Flow
Frontend → API → Redis → Worker → Redis → API → Frontend

---

## Prerequisites
- Docker
- Docker Compose

---

## How to Run

1. Clone the repository

2. Start all services:

```bash
docker compose up --build