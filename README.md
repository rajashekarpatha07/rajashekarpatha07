<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&lines=Raja+Shekar+Patha;Backend+Developer+%7C+Node.js+%26+TypeScript;Building+Real-Time+Systems+That+Scale" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/raja-shekar-patha-4519a6340/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rajashekarpatha07@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rajashekarpatha07)
[![MedSwift Live](https://img.shields.io/badge/MedSwift-Live%20on%20AWS%20EC2-22c55e?style=for-the-badge&logo=amazonaws&logoColor=white)](https://medswift.duckdns.org/)

<img src="https://komarev.com/ghpvc/?username=rajashekarpatha07&color=58a6ff&style=for-the-badge&label=Profile+Views"/>

</div>

---

## 🧠 About Me

Backend developer focused on building **real-time systems**, **high-performance APIs**, and **distributed infrastructure**. I care about writing clean, well-structured code and understanding *why* a system is designed the way it is — not just making it work.

```
🚑  Shipped MedSwift — a real-time ambulance dispatch system deployed on AWS EC2
📐  Sharpening DSA skills and exploring system design patterns
🏗️  Interested in distributed systems, message queues, and scalable architecture
📍  Hyderabad, India
```

---

## ⚙️ Tech Stack

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)

**Databases**

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

**DevOps & Tools**

![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

---

## 🚀 Projects

### 🚑 MedSwift V2 — Real-Time Emergency Dispatch System

> **🟢 Deployed on AWS EC2** → [medswift.duckdns.org](https://medswift.duckdns.org/)

Every second matters in an emergency. MedSwift auto-connects patients to the nearest available ambulance — no manual coordination, no delay.

| Feature | Implementation |
|---|---|
| **Geospatial Dispatch** | Redis GeoIndex + MongoDB Geospatial with progressive radius failover: 5km → 10km → 17km → 30km |
| **Atomic Assignment** | Ambulance removed from Redis pool before trip is saved; rollback on failure — eliminates double-dispatch |
| **Real-Time Sync** | Socket.IO rooms (`user:{id}`, `ambulance:{id}`, `trip:{id}`) with 4 JWT-authenticated roles |
| **State Machine** | Strict trip lifecycle: `SEARCHING → ACCEPTED → ARRIVED_PICKUP → EN_ROUTE_HOSPITAL → ARRIVED_HOSPITAL → COMPLETED` |
| **Audit Trail** | Immutable status timeline appended on every state change in MongoDB |
| **API Documentation** | Swagger / OpenAPI for automated schema generation and developer testing |
| **Security** | Input validation (Zod), JWT auth, request sanitization — aligned with OWASP Top 10 |
| **Architecture** | Modular TypeScript with strict schema validation across all routes |

**Stack:** `TypeScript` `Node.js` `Express` `MongoDB` `Redis` `Socket.IO` `JWT` `Zod` `Swagger` `AWS EC2`

[![Repo](https://img.shields.io/badge/GitHub-MedswiftV2-181717?style=for-the-badge&logo=github)](https://github.com/rajashekarpatha07/MedswiftV2)
[![Live](https://img.shields.io/badge/Live-medswift.duckdns.org-22c55e?style=for-the-badge&logo=amazonaws)](https://medswift.duckdns.org/)

---

### 📚 College Hub V2 — Academic Management Platform

A platform for managing academic resources — notes, schedules, and announcements — with role-based access for students, faculty, and admins.

**Engineering Highlights:**

- **TypeScript Migration** — Rewrote from JavaScript/Mongoose to TypeScript + Prisma ORM + MySQL for type safety and structured relational models
- **Redis Caching** — Targeted caching on student dashboard endpoints (announcements, materials, question papers) to cut repeated DB reads
- **Cache Invalidation** — Automated utilities that clear student and faculty caches whenever new resources are published
- **Media Optimization** — Backend-signed direct-to-Cloudinary uploads, offloading bandwidth and binary storage from the app server
- **25+ REST APIs** — All typed end-to-end with TypeScript and Prisma

**Stack:** `TypeScript` `Node.js` `Express` `Prisma` `MySQL` `Redis` `Cloudinary`

[![Repo](https://img.shields.io/badge/GitHub-collegehubv2-181717?style=for-the-badge&logo=github)](https://github.com/rajashekarpatha07/collegehubv2)

---

## 📊 GitHub Stats


<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=rajashekarpatha07&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true&count_private=true&rank_icon=github&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff&cache_seconds=86400" alt="GitHub Stats" />
&nbsp;&nbsp;
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rajashekarpatha07&layout=compact&theme=github_dark&hide_border=true&langs_count=7&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&cache_seconds=86400" alt="Top Languages" />

<br/><br/>

<img width="68%" src="https://streak-stats.demolab.com/?user=rajashekarpatha07&theme=github-dark-blue&hide_border=true&background=0d1117&ring=58a6ff&fire=58a6ff&currStreakLabel=c9d1d9&sideLabels=c9d1d9&dates=4d6a99" alt="GitHub Streak" />

<br/><br/>

<img width="90%" src="https://github-readme-activity-graph.vercel.app/graph?username=rajashekarpatha07&theme=github-compact&bg_color=0d1117&color=58a6ff&line=58a6ff&point=c9d1d9&area=true&hide_border=true" alt="Contribution Graph" />

</div>

---

## 🔭 Currently Working On

| Area | Focus |
|---|---|
| 📐 **DSA** | Arrays, trees, graphs, dynamic programming — sharpening algorithmic thinking |
| 🏗️ **System Design** | Distributed systems, message queues, consistent hashing, load balancing |
| ☁️ **Cloud & DevOps** | Going deeper with AWS services and containerization |

---

## 🎓 Education

**B.Tech in Cyber Security** · *2023 – 2027*  
Ellenki College of Engineering and Technology · Hyderabad, India

- 🤖 **AI Core Committee Member** — Organized Python & Machine Learning workshops for 50+ students
- 🎭 **Cultural Committee Member** — Led 5+ college-level cultural and community events

---

<div align="center">
  <i>Open to backend roles and interesting collaborations</i>
</div>
