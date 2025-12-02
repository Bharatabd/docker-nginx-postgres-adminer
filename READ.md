#Dockler Nginx + Postgres + Adminer Stack

## Overview
This project simulates a production-like mutli-container environment using Docker and Docker Compose.

**Services:**
- **web**: Custom Nginx container serving a static website.
- **db**: PostgreSQL database with initialization script.
- **adminer**: Web-based UI to manage the PostgreSQL database.


## Architecture
- All services are connected via a custom Docker bridge network 'app-net'.
- PostgreSQL data is stored in a named volume 'db-data' for persistence.
- Database schema and sample data are created automatically from 'db/init.sql'.
- Nginx serves 'index.html' from a custom image built using 'nginx/Dockerfile'.


## How to Run

```bash
docker compose build 
docker compose up -d 
