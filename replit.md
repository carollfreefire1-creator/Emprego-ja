# SOS Serviços

A platform that connects clients with service professionals for home maintenance (electrical, plumbing, painting, cleaning, etc.).

## Tech Stack

- **Framework:** Next.js 15 (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **ORM:** Prisma
- **Database:** PostgreSQL via Supabase
- **Auth:** Supabase Auth (SSR)
- **Validation:** Zod

## Project Structure

- `app/` — Next.js App Router pages and API routes
- `components/` — Reusable React components
- `actions/` — Server Actions
- `lib/` — Shared utilities (Prisma client, Supabase client, rate limiting, etc.)
- `prisma/` — Database schema and seed data
- `supabase/migrations/` — SQL migration files

## Running the App

```bash
npm run dev        # Start dev server on port 5000
npm run build      # Build for production
npm run db:push    # Sync Prisma schema to database
npm run db:seed    # Seed database with mock data
```

## Environment Setup

Copy `.env.example` to `.env.local` and fill in:
- `DATABASE_URL` / `DIRECT_URL` — Supabase PostgreSQL connection strings
- `NEXT_PUBLIC_SUPABASE_URL` — Supabase project URL
- `NEXT_PUBLIC_SUPABASE_ANON_KEY` — Supabase anonymous key
- `SUPABASE_SERVICE_ROLE_KEY` — Supabase service role key
- `NEXT_PUBLIC_APP_URL` — App public URL
- `CRON_SECRET` — Secret for internal cron job endpoints

## User Preferences

- Portuguese (Brazilian) is the primary language of the application
