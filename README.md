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

### [ShelterED](https://github.com/ShelterED-project/ShelterED) — backend lead, team of 6
Offline-first learning platform for schools: lessons, tests and class roll call keep working in a bomb shelter without internet and sync to the cloud later with no loss and no duplicates.
- Sync protocol: batched idempotent events with client UUIDs, per-event transactions, conflict rules, gap-free change feed cursor
- Air-alert integration, automatic roll call, Web Push (VAPID) to students, teachers and parents
- Offline "backpack" knowledge packs with ETag, brotli/gzip; image pipeline (WebP, EXIF stripping, dedup)
- Auth: OAuth 2.0 PKCE, JWT with refresh rotation, PIN login for kids with lockout-free rate limiting
- Celery + beat with a DB outbox when the broker is down; privacy: data inventory, retention purge, child data deletion
- 500+ pytest tests, Alembic migrations, OpenAPI contract, Docker, GitHub Actions

`FastAPI` `SQLAlchemy async` `PostgreSQL` `Redis` `Celery` `Docker`

### [website-for-store](https://github.com/Stanislave19/website-for-store) — full-stack e-commerce
Watch store: catalog with filters, cart, wishlist, orders, admin panel.

`FastAPI` `PostgreSQL` `Alembic` `Next.js` `Tailwind` `Docker` `Nginx`

### Examly — GlobalLogic hackathon 2026 ([repo](https://github.com/Codecon-2026/keerpich))
Gamified NMT exam prep with an AI mentor. My part: gamification backend — XP boosts, daily goals and spin wheel, streaks, leagues, flash mode with Redis TTL, Celery resets.

`FastAPI` `PostgreSQL` `Redis` `Celery` `OpenAI API`

### [Weather-simulator-MVP](https://github.com/Stanislave19/Weather-simulator-MVP-)
Soil moisture and temperature simulation for fields: RK4 ODE solver, cubic splines, Simpson integration, least-squares calibration behind an async FastAPI with background tasks.

`FastAPI` `Numerical methods` `Alembic`

### Private repositories
- **mono-donation-bot** — Telegram bot that receives Monobank webhooks and posts donation notifications, with duplicate-transaction protection (`FastAPI` `aiogram`)
- **numerical_methods_2026** — 11 numerical methods labs: LU decomposition and iterative solvers, Runge–Kutta and Adams with adaptive step, Hooke–Jeeves optimization, approximation and differentiation

### University
- [Python-university](https://github.com/Stanislave19/Python-university) — sorting, trees, MST (Kruskal, Prim), hashing
- [CPP-OOP](https://github.com/Stanislave19/CPP-OOP), [CPP-ATAP](https://github.com/Stanislave19/CPP-ATAP), [Delphi-OOP](https://github.com/Stanislave19/Delphi-OOP) — OOP and algorithms labs
- [lab3_web](https://github.com/Stanislave19/lab3_web), [backend-course-2026-4](https://github.com/Stanislave19/backend-course-2026-4) — Node.js CLI and HTTP server labs
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
