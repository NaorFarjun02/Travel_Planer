# ✈️ Travel Manager App --- Next.js Architecture

## 🎯 Project Overview

A modern fullstack web application for managing group trips ---
including booking uploads, schedule views, maps, calendar integration,
and AI-powered smart search.

Built with **Next.js 14 (App Router)** for a simplified and scalable
architecture.

------------------------------------------------------------------------

## 🏗️ Architecture Overview

    User (Browser)
            │
            ▼
    ┌────────────────────────────┐
    │      Next.js App           │
    │  (Frontend + API Routes)   │
    │        Vercel Hosting      │
    └─────────────┬──────────────┘
                  │
                  ▼
            Supabase (PostgreSQL)
                  │
                  ▼
        External Services (APIs)
        - Google Maps API
        - Google Calendar API
        - Google Cloud Vision
        - OpenAI / Claude

------------------------------------------------------------------------

## 🛠️ Tech Stack

### Frontend + Backend (Fullstack)

-   Next.js 14 (App Router)
-   React 18
-   TypeScript
-   Tailwind CSS
-   Server Actions
-   API Route Handlers

### Database

-   Supabase (Managed PostgreSQL)
-   Prisma ORM

### Authentication

-   Supabase Auth (Google + Email login)

### External APIs

-   Google Maps API
-   Google Calendar API
-   Google Cloud Vision (booking reader)
-   OpenAI / Claude API (AI search)

------------------------------------------------------------------------

## 📁 Recommended Folder Structure

    travel-app/
    ├── app/                  # Next.js App Router
    │   ├── layout.tsx
    │   ├── page.tsx
    │   ├── trips/
    │   ├── api/
    │   └── dashboard/
    │
    ├── components/           # Reusable UI components
    ├── lib/                  # Prisma, Supabase, utilities
    ├── services/             # External API logic
    ├── types/                # Shared TypeScript types
    ├── prisma/
    │   └── schema.prisma
    │
    ├── public/
    └── README.md

------------------------------------------------------------------------

## 🚀 Development Setup

### 1. Install Dependencies

``` bash
npm install
```

### 2. Run Development Server

``` bash
npm run dev
```

Visit: http://localhost:3000

------------------------------------------------------------------------

## 🔐 Environment Variables (.env)

Create a `.env.local` file:

    DATABASE_URL=
    NEXT_PUBLIC_SUPABASE_URL=
    NEXT_PUBLIC_SUPABASE_ANON_KEY=
    OPENAI_API_KEY=
    GOOGLE_MAPS_API_KEY=
    GOOGLE_CALENDAR_API_KEY=

------------------------------------------------------------------------

## 🧠 Core Features Roadmap

### Phase 1 --- Auth + Trip CRUD

-   Supabase authentication
-   Create / Edit / Delete trips
-   Dashboard overview

### Phase 2 --- Schedule View

-   Day-by-day breakdown
-   Timeline layout
-   Drag & drop planning

### Phase 3 --- Maps Integration

-   Google Maps daily route view
-   Distance & duration calculation

### Phase 4 --- Booking Uploads

-   PDF / Image upload
-   Google Vision text extraction
-   Auto trip parsing

### Phase 5 --- Calendar Integration

-   One-click add to Google Calendar

### Phase 6 --- AI Smart Search

-   Natural language search
-   "Best sushi near hotel under 30\$"
-   Personalized attraction suggestions

------------------------------------------------------------------------

## 💰 Estimated Monthly Costs

  Service           Cost
  ----------------- -----------------------
  Vercel            Free
  Supabase          Free
  Google APIs       Free up to quota
  OpenAI / Claude   Pay per usage
  Domain            \~\$1/month
  **Total (MVP)**   **\~\$1--\$10/month**

------------------------------------------------------------------------

## 📦 Deployment

### Frontend + Backend

Deploy directly to **Vercel**.

-   Connect GitHub repository
-   Auto deploy on every push
-   Automatic HTTPS
-   Global CDN

### Database

Hosted on **Supabase Cloud**.

------------------------------------------------------------------------

## 📌 Design Principles

-   Clean dashboard layout
-   Data-first interface
-   Minimalist UI
-   Mobile-friendly
-   AI-enhanced user experience

------------------------------------------------------------------------

## 🧭 Long-Term Scalability

-   Background jobs for AI processing
-   Rate limiting middleware
-   Caching strategy (React Query / Server Cache)
-   Role-based permissions (future)

------------------------------------------------------------------------

Last updated: 2026-03-02 Version: 2.0 (Next.js Fullstack)