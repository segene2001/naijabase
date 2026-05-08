# NaijaBase

> The open-source backend platform built for Nigerian developers — [naijabase.dev](https://naijabase.dev)

NaijaBase is a [Supabase](https://supabase.com)-inspired Backend-as-a-Service hosted on Nigerian servers (Nobus Cloud, Lagos), billed in Naira, and fully NDPA compliant.

## What it provides

- **PostgreSQL database** — full Postgres with a visual editor and row-level security
- **Authentication** — email/password, phone OTP, OAuth; NIN/BVN integrations planned
- **Realtime** — WebSocket subscriptions to database changes
- **File storage** — S3-compatible object storage with CDN from Lagos
- **Naira billing** — payments via Paystack, no dollar conversion required
- **NDPA compliance** — data residency in Nigeria, audit logs, DPA templates

## Tech stack

| Layer | Technology |
|-------|-----------|
| Frontend dashboard | Next.js + Tailwind CSS |
| Backend API | Node.js + Express + PostgreSQL |
| Auth | Supabase Auth (self-hosted) |
| Payments | Paystack |
| Database | PostgreSQL on Nobus Cloud (Lagos) |
| Hosting | Nobus Cloud / Layer3 (Nigerian servers) |

## Monorepo structure

```
naijabase/
├── index.html      ← Public landing page (GitHub Pages)
├── app/            ← Developer dashboard (Next.js)
├── api/            ← Backend REST API (Node.js + Express)
├── docs/           ← Documentation site
└── README.md
```

## Getting started

### Prerequisites

- Node.js 18+
- npm 9+ or pnpm 8+
- PostgreSQL 15+

### Run the API

```bash
cd api
cp .env.example .env   # fill in your values
npm install
npm run dev
```

### Run the dashboard

```bash
cd app
npm install
npm run dev
```

The dashboard runs at `http://localhost:3000` and the API at `http://localhost:4000`.

## Environment variables

See `api/.env.example` and `app/.env.example` for the full list of required variables.

## Contributing

Issues and pull requests are welcome. Please read `CONTRIBUTING.md` before submitting.

## License

MIT © NaijaBase Contributors
