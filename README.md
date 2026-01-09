# 🌌🤖 Nebula Node (Reboot)

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

## 📁 Planned Project Structure

```txt
src/
├─ commands/        # Slash commands
├─ events/          # Discord event handlers
├─ services/        # Business logic (XP, moderation, APIs)
├─ db/              # Prisma schema & DB utilities
├─ config/          # Environment-based configuration
├─ utils/           # Shared helpers
└─ index.ts         # Application entry point
