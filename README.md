# 🌌🤖 Nebula Node (Reboot)

[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-informational)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-informational)](https://nodejs.org/)
[![discord.js](https://img.shields.io/badge/discord.js-v14-informational)](https://discord.js.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Backend-informational)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-ORM-informational)](https://www.prisma.io/)
[![PM2](https://img.shields.io/badge/PM2-Process%20Manager-informational)](https://pm2.keymetrics.io/)
[![Docker](https://img.shields.io/badge/Docker-Optional-informational)](https://www.docker.com/)

> **Internal Note:** Swap these placeholder badges for real CI badges once GitHub Actions are added.

**Nebula Node** is a Discord bot being rebuilt **from scratch** with a modern, maintainable, and production-ready architecture.

This repository represents a **clean restart** of the project after a long hiatus.  
All previous files and setups have been intentionally discarded to remove technical debt and confusion.

The goal is to build Nebula Node *the right way* — documented, modular, scalable, and understandable even months later.

---

## 🧭 Project Status

🚧 **Early Development / Bootstrapping Phase**

- No legacy code  
- No backward compatibility requirements  
- Architecture-first approach  
- Everything documented as it is rebuilt  

---

## 🪐 Nebula Infrastructure Naming

Nebula Node is designed to fit neatly into the rest of the Nebula ecosystem:

- **NebulaCore** → primary services / source-of-truth (VPS or main host)
- **NebulaNest** → home lab / Unraid services hub
- **Nebula Node** → Discord automation + utilities “control plane” for your community

Example responsibilities:
- Nebula Node → Discord commands, status reporting, admin workflows
- NebulaCore → database (Postgres), production bot runtime, CI runners (optional)
- NebulaNest → game servers, backups, media services, internal endpoints

---

## 🎯 Project Goals

### Core Goals
- Clean, readable TypeScript codebase  
- Predictable project structure  
- Easy local development  
- Safe production deployment  
- Clear separation between **dev** and **prod**  
- Self-hosted friendly (VPS / Docker)  

### Long-Term Vision
Nebula Node is intended to grow into:
- A powerful Discord utility bot  
- A game-server companion (Minecraft, WoW, etc.)  
- A platform with optional web dashboards  
- A potential SaaS-style offering (optional)  

---

## ✨ Planned Features

### 🌌🤖 Discord Bot Core
- Slash-command based architecture (discord.js v14)  
- Modular command & event loading  
- Per-guild configuration system  
- Permission-aware commands  
- Robust error handling & logging  

### 🛡️ Moderation
- Ban / Kick / Timeout commands  
- Moderation logging  
- Audit-friendly design  
- Configurable per server  

### 📈 XP & Leveling
- Custom XP system  
- PostgreSQL-backed persistence  
- Configurable leveling curves  
- Rank roles & progression  
- Future web visualization support  

### 🎮 Game Server Utilities
- Minecraft server control (start / stop / status)  
- Player count reporting  
- Auto-shutdown on inactivity  
- Scheduled backups  
- Expandable for other games  

### 🔌 Integrations
- External APIs (fun & utility)  
- Pluggable service architecture  
- Easy to add / remove features  

### 🌐 Future Web Dashboard (Optional)
- Discord OAuth login  
- Server configuration UI  
- XP & stats visualization  
- Admin tools  
- Multi-server support  

---

## 🛠️ Planned Tech Stack

| Layer | Choice |
|-----|------|
| Language | TypeScript |
| Discord API | discord.js v14 |
| Runtime | Node.js (18+) |
| Database | PostgreSQL |
| ORM | Prisma |
| Process Manager | PM2 |
| Hosting | VPS |
| Networking | Tailscale |
| (Optional) Containers | Docker / Docker Compose |

---

## 🧪 Dev vs Prod Layout

A simple, repeatable split that keeps development safe and production stable.

### Recommended Environments

**Development (local machine)**
- Runs Nebula Node in dev mode (`tsx` / `ts-node-dev` / `nodemon`)
- Uses a dedicated **dev bot token** + **dev Discord server**
- Uses a separate Postgres DB (or schema)

**Production (NebulaCore VPS)**
- Runs compiled build (`dist/`) under PM2
- Uses **prod bot token** + real Discord server(s)
- Uses production Postgres
- Logging + monitoring (later)

---

## 🔐 Environment Variables

Create these files:

- `.env.example` (committed)
- `.env.dev` (ignored)
- `.env.prod` (ignored)

### Example `.env.example`

```bash
# Discord
DISCORD_TOKEN=replace_me
DISCORD_CLIENT_ID=replace_me

# App
NODE_ENV=development
LOG_LEVEL=info

# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/nebulanode

# Optional: Feature flags
FEATURE_XP=true
FEATURE_MODERATION=true
FEATURE_GAMESERVERS=true
