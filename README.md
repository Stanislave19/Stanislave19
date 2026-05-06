# Hi, I'm Stanislav 👋

> Backend Python developer focused on async APIs, real-time systems, and numerical computing.

---

## About Me

I build backend services in Python — mostly async REST APIs, event-driven systems, and integrations with AI providers and external data sources. My interests sit at the intersection of solid engineering (clean architecture, migrations, background processing) and applied math (ODEs, interpolation, numerical optimization).

I enjoy designing systems where the data model, the API surface, and the infrastructure all reinforce each other — and where performance characteristics are understood, not guessed.

---

## 🛠 Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Backend & API**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-CA4245?style=flat&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-2C3E50?style=flat)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat&logo=socket.io&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)

**Data & Infrastructure**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)

**Scientific & AI**
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)

---

## 📌 Featured Projects

### Keerpich — EdTech Platform Backend
A learning platform backend supporting real-time interactions between users, AI-generated content, and asynchronous workflows.

- **API:** FastAPI with async endpoints and WebSocket channels for live sessions and leaderboards
- **Persistence:** PostgreSQL with SQLAlchemy 2.0; schema evolved across 29 Alembic migrations
- **Background work:** Celery + Redis for periodic recalculations, ranking updates, and scheduled tasks
- **AI integrations:** OpenAI and Groq for question generation and conversational tutoring
- **Auth:** JWT-based sessions with Google OAuth 2.0
- **Deployment:** Docker Compose stack behind Nginx

**Stack:** Python · FastAPI · PostgreSQL · Redis · Celery · WebSockets · OpenAI · Docker

---

### AgroSim — Agricultural Weather Simulator
A simulation backend for soil and climate dynamics in agricultural regions, combining real weather data with numerical models.

- **Soil moisture & temperature:** ODE system solved with classical Runge–Kutta (RK4)
- **Data preprocessing:** cubic spline interpolation for missing observations
- **Agronomic metrics:** Growing Degree Days computed via Simpson's rule, ET₀ evapotranspiration, runoff, crop coefficients
- **Drought detection:** alerts derived from numerical differentiation of moisture curves
- **Model calibration:** Gaussian elimination and least-squares fitting
- **External data:** Open-Meteo for weather, Nominatim/OpenStreetMap for geocoding

**Stack:** Python · FastAPI · SQLite · SQLAlchemy · NumPy · SciPy

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Stanislave19&show_icons=true&hide_border=true&count_private=true" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Stanislave19&layout=compact&hide_border=true" alt="Top Languages" />
</p>

---

Open to interesting backend problems — especially ones involving real-time data, simulation, or thoughtful API design.
