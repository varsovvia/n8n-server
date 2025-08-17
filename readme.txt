Got it 👍 — here’s the README.txt in English, clean and copy-paste ready:

# README.txt

## Project Context
This server (DigitalOcean Droplet, Ubuntu 22.04) was created to **learn and deploy n8n in the cloud**.  
The goal is to move from a basic deployment to a more secure, production-ready setup with domain + HTTPS, and later build automations for clients.

## Current State
- Server: DigitalOcean Droplet (2 GB RAM, 1 vCPU, Ubuntu 22.04).
- Access: via **SSH key** from `C:/Users/marti/.ssh/id_ed25519`.
- n8n runs with **Docker Compose** in `/root/n8n`.
- Exposed at `http://165.232.75.201:5678` (currently no HTTPS).
- Environment variables set in `docker-compose.yml` (example: `N8N_SECURE_COOKIE=false` to bypass HTTPS for now).
- **Git Repository**: `n8n-server` - All changes are version controlled here.

## Next Steps
1. Configure **Cloudflare Tunnel + custom domain** → secure HTTPS access.
2. Move n8n database to **managed Postgres** (Neon or Supabase).
3. Add **Redis** (Upstash) to use `EXECUTIONS_MODE=queue`.
4. Create first **test workflows** (e.g., webhook → transform data → respond).
5. Document and version workflows (export JSON into `/workflows` folder).

## Conventions
- Important files live in `/root/n8n/` (server) and in `C:\Users\marti\Proyectos\n8n_selfhost` (local).
- Every **important change** (infra, config, workflows, security, etc.) must be logged in this README.  
  Example: "Cloudflare Tunnel with domain automation.mydomain.com enabled on 2025-08-20".
- **All changes must be committed and pushed to Git repository `n8n-server`** for version control and backup.

## Quick Commands
- **Start n8n**:
  ```bash
  cd /root/n8n
  docker compose up -d


Stop n8n:

docker compose down


View logs:

docker compose logs -f

## Git Repository Setup
- **Repository**: `n8n-server`
- **Remote Origin**: https://github.com/varsovvia/n8n-server.git
- **Branch**: `master`
- **Initial Commit**: ✅ Completed with n8n setup and documentation

### Git Commands
```bash
# Add and commit changes
git add .
git commit -m "Description of changes"

# Push to remote repository
git push origin master

# Pull latest changes
git pull origin master
```

Reminder for Cursor AI

This file is the context model for the project.

Every time something important happens, Cursor AI must help update this README with the new state.

Cursor AI should always use this file to understand what is being built, what decisions were made, and what’s next.