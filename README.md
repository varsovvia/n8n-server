# n8n.server

Docker-based setup for a self-hosted [n8n](https://n8n.io) automation server.  
This repository contains configuration, environment files, and documentation to run and manage n8n on a remote server.

## Features
- Docker Compose setup for n8n
- Environment variables for easy configuration
- Documentation of setup, workflows, and infrastructure
- Backup and versioning of important files

## Quick Start
```bash
# Start n8n
docker compose up -d

# Stop n8n
docker compose down

# View logs
docker compose logs -f
