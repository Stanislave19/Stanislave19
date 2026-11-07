<div align="center">

### Python Backend Engineer

*Async APIs, background jobs and data that survives a bad network.*

![Open to work](https://img.shields.io/badge/Open_to_work-backend%20%7C%20internship%20%7C%20junior-2ea44f?style=for-the-badge)

</div>

---

## ⚡ Tech Stack

**Backend**

![Python](https://img.shields.io/badge/Python_3.13-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic_v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2.0_async-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA539?style=flat-square)
![Django](https://img.shields.io/badge/Django_REST-092E20?style=flat-square&logo=django&logoColor=white)

**Data & Queues**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery_+_beat-37814A?style=flat-square&logo=celery&logoColor=white)
![asyncpg](https://img.shields.io/badge/asyncpg-336791?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**Auth & Security**

![JWT](https://img.shields.io/badge/JWT_+_refresh_rotation-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth_2.0_PKCE-4285F4?style=flat-square)
![Rate limiting](https://img.shields.io/badge/Redis_rate_limiting-DC382D?style=flat-square&logo=redis&logoColor=white)

**Quality & DevOps**

![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat-square&logo=ruff&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Also**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

---

## 🚀 Projects

**By the numbers:** 480+ commits across 15 repositories in 2026 · 11 merged PRs in ShelterED · 500+ backend tests in ShelterED

### [ShelterED](https://github.com/ShelterED-project/ShelterED) — backend lead, team of 6 · 164 commits
Offline-first learning platform for schools: lessons, tests and class roll call keep working in a bomb shelter without internet and sync to the cloud later with no loss and no duplicates.
- **Sync protocol v1:** batched idempotent events with client UUIDs, per-event transactions, conflict rules, device clock-skew correction, gap-free change feed cursor; bad events are rejected individually instead of blocking the batch
- **Alerts & roll call:** alerts.in.ua polling with dedup, manual/drill alerts, roll call auto-opened when a lesson starts during an alert and closed on all-clear; ETag polling for the teacher screen
- **Web Push (VAPID):** subscriptions, fan-out with retries outside DB transactions, roll-call status pushed to parents
- **Offline "backpack" knowledge packs:** versioned, rebuilt on lesson/schedule changes, served with ETag and brotli/gzip; image pipeline (WebP, EXIF/GPS stripping, content dedup)
- **Auth & hardening:** OAuth 2.0 PKCE, JWT refresh rotation, PIN login for kids, layered rate limits, security headers/HSTS, 1 MiB body limit, prod-only config checks
- **Reliability:** Celery + beat with a DB outbox when the broker is down, task time limits, debounced aggregate recompute, batched queries and FK indexes
- **Child data privacy:** wellbeing check-in visible only to the child and parents with view audit, retention purge, data deletion requests confirmed by school admin
- Alembic migrations tested both ways, OpenAPI contract with drift test, end-to-end scenario tests, Docker image (non-root)

`FastAPI` `SQLAlchemy async` `PostgreSQL` `Redis` `Celery` `Docker`

### [website-for-store](https://github.com/Stanislave19/website-for-store) — full-stack e-commerce, solo · 137 commits
Watch store built end to end in two weeks: storefront, customer accounts and admin panel.
- Catalog API with filters, search, sorting, pagination, category tree and EAV product attributes; DB indexes and filter caching
- Checkout with Nova Poshta city/branch autocomplete via a backend proxy; orders notify managers in Telegram
- Customer accounts: registration, order history, addresses, wishlist; cart and promo codes (with brute-force rate limit)
- Admin panel: JWT in httpOnly cookie, owner/manager roles, CRUD for products, categories, promo codes, orders; bulk CSV/Excel import with photo download
- Security: login rate limiting, upload content validation, no default secret key, DB port not exposed
- Ops: prod Docker Compose behind Nginx, atomic `pg_dump` backups with offsite copy, restore runbook; SEO (sitemap, JSON-LD, canonical tags)

`FastAPI` `PostgreSQL` `Alembic` `Next.js` `TypeScript` `Tailwind` `Docker` `Nginx`

### VPK-OSINT — team data project · 81 commits (private)
Pipeline that maps defense-industry enterprises from open sources: job postings, registries and sanctions lists, merged into evidence-backed company cards with a rating, a map and a relationship graph.
- Job-site collectors with a unified vacancy schema, sharded parallel runs, checkpoints and a circuit breaker on blocking
- Noise filtering and signal levels (core / adjacent / grey) with evidence quotes; company discovery with multi-source tax-ID verification
- Sanctions and export-control matching (OFAC, OpenSanctions) and the "sanctions gap"; registry data streamed without storing the full dump
- Relationship edges (parent/subsidiary, shared owners, directors, addresses); API on SQL with a full reload in one transaction; ML score shown separately from the rule-based rating

`Python` `PostgreSQL` `Docker` `JavaScript`

### Examly — GlobalLogic hackathon 2026 ([repo](https://github.com/Codecon-2026/keerpich)) · 30 commits
Gamified NMT exam prep with an AI mentor. My part: the backend core and gamification.
- Models, services, routers, Alembic migrations and Google OAuth; 82 passing tests at the first merge
- XP boosts, daily goals, spin wheel, streaks, league multipliers, flash mode with Redis TTL, NMT countdown; Celery reset tasks

`FastAPI` `PostgreSQL` `Redis` `Celery` `OpenAI API`

### [Weather-simulator-MVP](https://github.com/Stanislave19/Weather-simulator-MVP-) · 12 commits
Soil moisture and temperature simulation for fields: RK4 ODE solver, cubic splines, Simpson integration, least-squares calibration behind an async FastAPI.
- Background simulation tasks, pagination, rate limiting, logging middleware, health check with DB status, Alembic migrations

`FastAPI` `Numerical methods` `Alembic`

### Private repositories
- **mono-donation-bot** (19 commits) — Telegram bot that receives Monobank webhooks and posts donation notifications, with duplicate-transaction protection (`FastAPI` `aiogram`)
- **numerical_methods_2026** (16 commits) — numerical methods labs: LU decomposition and iterative solvers, Runge–Kutta and Adams with adaptive step, Hooke–Jeeves optimization, approximation and differentiation

### University
- [Python-university](https://github.com/Stanislave19/Python-university) — sorting, trees, MST (Kruskal, Prim), chain and open-addressing hashing
- [CPP-OOP](https://github.com/Stanislave19/CPP-OOP), [CPP-ATAP](https://github.com/Stanislave19/CPP-ATAP), [Delphi-OOP](https://github.com/Stanislave19/Delphi-OOP) — OOP and algorithms labs
- [lab3_web](https://github.com/Stanislave19/lab3_web), [backend-course-2026-4](https://github.com/Stanislave19/backend-course-2026-4) — Node.js CLI (commander) and HTTP server with query filters
- [django-blog-demo](https://github.com/Stanislave19/django-blog-demo) — Django blog REST API

---

## 🧭 How I work

- Small, reversible commits and PRs with green CI
- Tests for the main scenario and for every access rule
- Idempotent writes and "nothing gets lost" by default
- Schema changes only through migrations that work both ways

<div align="center">

*Open to backend internships and junior roles — reach me via GitHub.*

</div>
