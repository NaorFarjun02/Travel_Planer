# ✈️ Travel Manager App — Architecture & Planning

## 🎯 Project Overview

A web application for managing group trips — including uploading bookings, schedule views, maps, calendar integration, and AI-powered smart search.

---

## 🛠️ Full Tech Stack

### Code Editor
| Tool | Description |
|------|-------------|
| **Cursor** | VSCode-based editor with built-in AI that learns your project. Connects to GitHub. Recommended over plain VSCode |

### Frontend (Client Side)
| Tool | Description |
|------|-------------|
| **React 18** | UI library — most popular, massive community |
| **TypeScript** | JavaScript with types — prevents bugs, easier to learn |
| **Vite** | Fast build tool — runs the project locally |
| **Tailwind CSS** | Utility-first CSS — fast styling with pre-built classes |
| **React Router v6** | Page navigation management |
| **TanStack Query** | Server state management & data fetching |

### Backend (Server Side)
| Tool | Description |
|------|-------------|
| **Node.js** | Runs JavaScript on the server |
| **Express.js** | Framework for building APIs |
| **TypeScript** | Consistency with the frontend |
| **Prisma** | ORM — clean interface for database operations |

### Database
| Tool | Description |
|------|-------------|
| **Supabase** | Managed PostgreSQL, built-in Authentication, visual dashboard, free tier available |

### External Services (APIs)
| Service | Usage | Cost |
|---------|-------|------|
| **Google Maps API** | Daily map view + navigation | Free up to quota |
| **Google Calendar API** | Auto-add events to calendar | Free |
| **Google Cloud Vision / Gemini** | Read booking files (PDF/image) | Free up to quota |
| **Claude API / OpenAI** | AI-powered attraction search | Pay per use |

---

## 🚀 Deployment — Where to Host

### Frontend → Vercel
- Connects directly to GitHub
- Auto-deploys on every `git push`
- Completely free for personal projects
- Automatic HTTPS + global CDN
- 🔗 [vercel.com](https://vercel.com)

### Backend → Railway
- Full Node.js/Express support
- GitHub integration — auto-deploy
- ~$5/month (Hobby plan)
- Easy environment variable management (API Keys, etc.)
- 🔗 [railway.app](https://railway.app)

### Database → Supabase
- Managed PostgreSQL in the cloud
- Free up to 500MB
- Visual dashboard to view data
- Built-in Auth (Google Login, Email, etc.)
- 🔗 [supabase.com](https://supabase.com)

### Domain → Namecheap
- ~$10/year for a standard domain (.com / .io)
- Simple management interface
- Free DNS
- Easy connection to Vercel
- 🔗 [namecheap.com](https://namecheap.com)

---

## 🏗️ Architecture Overview

```
User (Browser)
        │
        ▼
┌─────────────────┐
│   React App     │ ◄──► Google Maps API
│   (Vercel)      │ ◄──► Google Calendar API
└────────┬────────┘
         │ HTTP Requests
         ▼
┌─────────────────┐
│  Express API    │ ◄──► Claude/OpenAI API (smart search)
│  (Railway)      │ ◄──► Google Cloud Vision (booking reader)
└────────┬────────┘
         │ Prisma ORM
         ▼
┌─────────────────┐
│   Supabase      │
│  (PostgreSQL)   │
└─────────────────┘
```

---

## 📁 Recommended Folder Structure

```
travel-app/
├── frontend/                  # React App
│   ├── src/
│   │   ├── components/        # UI components
│   │   ├── pages/             # Pages (trips, single day, map)
│   │   ├── hooks/             # Custom React Hooks
│   │   ├── services/          # API calls
│   │   └── types/             # TypeScript types
│   └── package.json
│
├── backend/                   # Express Server
│   ├── src/
│   │   ├── routes/            # API routes
│   │   ├── controllers/       # Business logic
│   │   ├── services/          # External API integrations
│   │   └── prisma/            # Schema + migrations
│   └── package.json
│
└── README.md
```

---

## 📋 Recommended Development Order

| Phase | What to Build | Est. Time |
|-------|---------------|-----------|
| **1** | Project setup + Auth (Supabase) | Week 1 |
| **2** | Trip CRUD — create, edit, delete | Week 2 |
| **3** | Day-by-day and hour-by-hour schedule view | Week 3 |
| **4** | Google Maps integration | Week 4 |
| **5** | Booking uploads + Google Calendar | Weeks 5–6 |
| **6** | AI-powered smart search | Week 7 |
| **7** | Full deployment + custom domain | Week 8 |

---

## 💰 Estimated Monthly Costs (at launch)

| Service | Cost |
|---------|------|
| Vercel (Frontend) | Free |
| Supabase (DB) | Free |
| Railway (Backend) | ~$5 |
| Namecheap (Domain) | ~$1/month |
| Google APIs | Free up to quota |
| **Total** | **~$6/month** |

---

## ✅ Prerequisites Checklist

- [x] GitHub account
- [x] Node.js installed
- [ ] Supabase account (free) — [supabase.com](https://supabase.com)
- [ ] Vercel account (free, connect via GitHub) — [vercel.com](https://vercel.com)
- [ ] Railway account (free to start) — [railway.app](https://railway.app)
- [ ] Google Cloud account (for APIs) — [console.cloud.google.com](https://console.cloud.google.com)
- [ ] Cursor installed — [cursor.sh](https://cursor.sh)

---

## 📌 Important Notes

- **Google Cloud** — requires a credit card but has a generous free tier that's more than enough for development
- **Supabase Auth** — provides Google/Email login out of the box, no need to build it from scratch
- **Vercel + GitHub** — every `push` to `main` automatically updates the live site
- **Railway** — can connect directly to Vercel and Supabase with minimal config

---

*Last updated: 2026 | Version 1.0*
