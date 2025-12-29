# Aedar

**AI-powered execution agent that transforms project ideas into roadmaps and auto-schedules them to your calendar.**

> Stop planning. Start shipping.

---

## What is Aedar?

Aedar bridges the gap between "I have an idea" and "I'm shipping it." Describe your project in plain English, get a structured technical roadmap, and watch it appear on your calendar automatically.

**Key differentiator:** Aedar doesn't just plan — it executes.

---

## Features

- **AI Chat Interface** — Conversational roadmap generation with context awareness
- **Smart Roadmaps** — Phases, milestones, time estimates, and learning resources
- **Auto-Schedule** — One-click Google Calendar integration with availability detection
- **Planning Modes** — Sprint (concise), Standard (balanced), Architect (deep analysis)
- **Session History** — Save, revisit, and share roadmaps
- **Public/Private Sharing** — Share roadmaps via link or keep them private

---

## Tech Stack

| Layer      | Technology                           |
| ---------- | ------------------------------------ |
| Frontend   | Next.js 15, TypeScript, Tailwind CSS |
| Backend    | NestJS, TypeScript                   |
| Database   | Supabase (PostgreSQL + Auth)         |
| AI         | Google Gemini                        |
| Calendar   | Google Calendar API                  |
| Deployment | Vercel (frontend), Render (backend)  |

---

## Quick Start

### Prerequisites

- Node.js 18+
- Supabase account
- Google Cloud project (for Calendar API)

### Installation

```bash
# Clone the repository
git clone https://github.com/cridiv/aedar.git
cd aedar

# Install dependencies
cd aedar-frontend && npm install
cd ../aedar-backend && npm install
```

### Environment Variables

**Frontend (`aedar-frontend/.env.local`)**

```env
NEXT_PUBLIC_SUPABASE_URL=your-supabase-url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
NEXT_PUBLIC_API_URL=http://localhost:5000
```

**Backend (`aedar-backend/.env`)**

```env
SUPABASE_URL=your-supabase-url
SUPABASE_SERVICE_KEY=your-service-key
GEMINI_API_KEY=your-gemini-key
GOOGLE_CLIENT_ID=your-client-id
GOOGLE_CLIENT_SECRET=your-client-secret
```

### Run Locally

```bash
# Terminal 1 - Backend
cd aedar-backend
npm run start:dev

# Terminal 2 - Frontend
cd aedar-frontend
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

---

## How It Works

1. **Describe** — Tell Aedar what you want to build
2. **Generate** — AI creates a structured roadmap with phases and milestones
3. **Schedule** — Connect your calendar and auto-book each task
4. **Execute** — Follow your scheduled plan and ship

---

## Project Structure

```
aedar/
├── aedar-frontend/     # Next.js 15 app
│   ├── app/
│   │   ├── chat/       # Main chat interface
│   │   ├── roadmap/    # Roadmap viewer
│   │   └── signin/     # Authentication
│   └── lib/            # Supabase client
│
└── aedar-backend/      # NestJS API
    └── src/
        ├── chat/       # AI chat endpoints
        ├── roadmap/    # Roadmap CRUD
        ├── mcp/        # Calendar integration
        └── common/     # Shared services
```

---

## Deployment

**Frontend (Vercel)**

1. Import repo → Set root to `aedar-frontend`
2. Add environment variables
3. Deploy

**Backend (Render)**

1. Create Web Service → Set root to `aedar-backend`
2. Build: `npm install && npm run build`
3. Start: `npm run start:prod`
4. Add environment variables

---

## Authors

- **Aderemi Ademola** — Backend & AI ([@cridiv](https://x.com/cridiv))
- **Peters Joshua** — Frontend ([@joshpet77](https://x.com/joshpet77))

---

## License

MIT

---
