NeuralChat — Real-time AI Chat Dashboard

A fullstack AI chat application with:
- Streaming responses via Server-Sent Events (SSE)
- 4 AI Personas (Assistant, Creative, Analyst, Mentor)
- Session management with history, export, and delete
- Live stats panel (sessions, messages, uptime)
- Dark editorial UI with DM Mono + Syne fonts

---

## Stack

| Layer | Tech |
|-------|------|
| Frontend | React + Vite |
| Backend | Node.js + Express |
| AI | Anthropic Claude API |
| Streaming | Server-Sent Events (SSE) |

---

## Getting Started

### 1. Backend
```bash
cd backend
npm install
cp .env.example .env
# Add your ANTHROPIC_API_KEY to .env
npm run dev
```

### 2. Frontend
```bash
cd frontend
npm install
npm run dev
```

Open **http://localhost:5173**

---

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | /sessions | List all sessions |
| POST | /sessions | Create new session |
| DELETE | /sessions/:id | Delete a session |
| GET | /sessions/:id/messages | Get messages |
| POST | /sessions/:id/chat | Send message (SSE stream) |
| GET | /sessions/:id/export | Export as JSON |
| GET | /stats | Server stats |

---

## Features
- Real-time token streaming
- 4 AI personas with different system prompts
- Multi-session chat history
- Export chats as JSON
- Live server stats dashboard
