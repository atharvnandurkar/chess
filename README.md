# ♟️ Realtime Multiplayer Chess Platform

A full-stack realtime multiplayer chess platform where players can create matches, play live games, and compete using an Elo-style rating system.

Built with scalable architecture using WebSockets, Redis, PostgreSQL, and TypeScript.

---

## 🚀 Features

- 🔐 Authentication (Google/GitHub)
- ♟️ Create or join realtime chess matches
- ⚡ Live gameplay using WebSockets
- 📦 Redis queue for move synchronization
- 🧠 Chess move validation
- 📈 Elo-based rating system
- 🕒 Match history and game persistence
- 👥 Multiplayer matchmaking
- 🌐 Responsive modern UI

---

## 🏗️ Architecture

```txt
Frontend (React)
        │
        ▼
Backend API (Node.js + Express)
        │
        ▼
WebSocket Server
        │
        ▼
Redis Queue  ───► Game State Sync
        │
        ▼
PostgreSQL Database
```

---

## 🛠️ Tech Stack

### Frontend
- React
- TypeScript
- Tailwind CSS
- Zustand / Context API

### Backend
- Node.js
- Express
- TypeScript

### Realtime
- WebSockets

### Database & Infrastructure
- PostgreSQL
- Redis
- Prisma ORM

### Authentication
- Google OAuth
- GitHub OAuth

---

## 📂 Monorepo Structure

```txt
apps/
 ├── frontend       # React frontend
 ├── backend        # REST API server
 └── ws             # WebSocket realtime server

packages/
 ├── db             # Prisma schema & database
 ├── common         # Shared types/utilities
 └── ui             # Shared UI components
```

---

## ⚙️ Environment Variables

Copy `.env.example` to `.env` in all apps.

Example:

```env
DATABASE_URL=
REDIS_URL=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=

GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=

JWT_SECRET=
```

---

## 🧪 Local Development Setup

### 1. Clone repository

```bash
git clone <repo-url>
cd chess-platform
```

### 2. Install dependencies

```bash
pnpm install
```

### 3. Generate Prisma client

```bash
pnpm --filter @repo/db exec prisma generate
```

### 4. Run database migrations

```bash
pnpm --filter @repo/db exec prisma migrate dev
```

### 5. Start Redis

```bash
docker run -p 6379:6379 redis
```

### 6. Start WebSocket server

```bash
cd apps/ws
pnpm dev
```

### 7. Start backend API

```bash
cd apps/backend
pnpm dev
```

### 8. Start frontend

```bash
cd apps/frontend
pnpm dev
```

---

## 🎯 Core Engineering Challenges Solved

- Realtime multiplayer synchronization
- Preventing move desync
- Distributed WebSocket handling
- Game state persistence
- Rating calculation system
- Matchmaking architecture
- Handling concurrent users

---

## 📸 Screenshots

Add screenshots here.

---

## 📈 Future Improvements

- Spectator mode
- Friend system
- Tournaments
- Game replay system
- Stockfish integration
- Bullet/Blitz/Rapid modes
- Leaderboards
- Chat during matches

---

## 🧠 Lessons Learned

- Designing scalable realtime systems
- WebSocket architecture
- Event-driven backend systems
- Multiplayer state synchronization
- Database modeling for games
- Redis pub/sub patterns

---

## 📄 License

MIT