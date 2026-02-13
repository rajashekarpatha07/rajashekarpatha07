<h1 align="center">Raja Shekar Patha</h1>

<p align="center">
  Backend Developer &nbsp;·&nbsp; Node.js &nbsp;·&nbsp; Hyderabad, India
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/raja-shekar-patha-4519a6340/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  &nbsp;
  <a href="mailto:rajashekarpatha07@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://github.com/rajashekarpatha07">
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
  </a>
</p>

---

I build backend systems — APIs, real-time infrastructure, and data layers. My focus is on writing clean, well-structured code and understanding *why* a system is designed the way it is, not just making it work.

Currently re-architecting **MedSwift** with PostgreSQL + Prisma after learning the limitations of the first version.

---

## Tech Stack

**Languages:** TypeScript · JavaScript · Python · C

**Backend:** Node.js · Express.js · Socket.IO · Prisma · JWT · Zod

**Databases:** PostgreSQL · MongoDB · MySQL · Redis

**Tools:** Git · Docker · Linux · Postman

---

## Projects

### 🚑 MedSwift — Real-time Emergency Dispatch System

The core problem: in a medical emergency, every second matters. This system connects patients to the nearest available ambulance automatically, without manual coordination.

**How it works:**
- Redis Geospatial index stores all active (ready) ambulances. On a trip request, the system searches at 5km → 10km → 17km → 30km until it finds one
- The nearest ambulance is auto-assigned atomically — removed from the Redis pool before the trip is saved, with a rollback if the save fails, preventing double-assignment
- Socket.IO rooms (`user:{id}`, `ambulance:{id}`, `trip:{id}`) handle real-time state sync between patient, driver, and admin
- Trip status follows a strict state machine: `SEARCHING → ACCEPTED → ARRIVED_PICKUP → EN_ROUTE_HOSPITAL → ARRIVED_HOSPITAL → COMPLETED`
- Every status change is appended to an immutable timeline in MongoDB for audit

**Stack:** Node.js · TypeScript · Express · MongoDB · Redis · Socket.IO · Zod · JWT

[![Repo](https://img.shields.io/badge/GitHub-medswift-181717?style=flat-square&logo=github)](https://github.com/rajashekarpatha07/medswift)

---

### 🚑 MedSwift V2 *(In Progress)*

Rebuilding with lessons learned from V1. Main changes: PostgreSQL + Prisma for proper relational data and ACID guarantees, structured logging with Pino instead of console.log, and fixing the gaps I found in V1 (missing compound indexes, rate limiting disabled, Redis KEYS → SCAN).

**Stack:** TypeScript · Express · Prisma · PostgreSQL · Redis · Socket.IO

[![Repo](https://img.shields.io/badge/GitHub-MedswiftV2-181717?style=flat-square&logo=github)](https://github.com/rajashekarpatha07/MedswiftV2)

---

### 📚 College Hub V2 — Academic Platform

A platform for managing academic resources — notes, schedules, announcements — with role-based access for students, faculty, and admins.

Redis caching on the most-hit read endpoints brought repeated DB queries down significantly. Built 25+ REST APIs, all typed end-to-end with TypeScript and Prisma.

**Stack:** TypeScript · Express · Prisma · MySQL · Redis · Cloudinary

[![Repo](https://img.shields.io/badge/GitHub-collegehubv2-181717?style=flat-square&logo=github)](https://github.com/rajashekarpatha07/collegehubv2)

---

## GitHub Stats

<p align="center">
  <img height="170em" src="https://github-readme-stats.vercel.app/api?username=rajashekarpatha07&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true&count_private=true&rank_icon=github&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff"/>
  &nbsp;
  <img height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rajashekarpatha07&layout=compact&theme=github_dark&hide_border=true&langs_count=6&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9"/>
</p>

<p align="center">
  <img width="65%" src="https://streak-stats.demolab.com/?user=rajashekarpatha07&theme=github-dark-blue&hide_border=true&background=0d1117&ring=58a6ff&fire=58a6ff&currStreakLabel=c9d1d9&sideLabels=c9d1d9&dates=4d6a99"/>
</p>

> Stats only count public repositories. If the cards show "not found", make sure your key repos are set to public on GitHub.

---

## Currently Working On

- Finishing MedSwift V2 — PostgreSQL migration + proper logging
- Learning Docker and AWS for deploying these projects
- Going deeper into system design — distributed systems, message queues

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=rajashekarpatha07&color=58a6ff&style=flat-square&label=Profile+Views"/>
</p>
