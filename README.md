<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:58A6FF&height=180&section=header&text=Cem%20Deniz%20Demir&fontColor=FFFFFF&fontSize=48&fontAlignY=35&desc=Full-Stack%20Software%20Engineer&descAlignY=58&descSize=18" width="100%" alt="header" />

<a href="https://cemdenizdemir.com">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=640&lines=Identity+%26+authentication+systems;Security+as+a+design+constraint%2C+not+a+patch;Performance+as+a+design-time+concern;AI-assisted%2C+human-reviewed+engineering;Node.js+%C2%B7+TypeScript+%C2%B7+NestJS+%C2%B7+PostgreSQL" alt="what I do" />
</a>

<br><br>

<a href="https://cemdenizdemir.com"><img src="https://img.shields.io/badge/Portfolio-0D1117?style=for-the-badge&logo=firefox&logoColor=58A6FF" alt="Portfolio" /></a>
<a href="https://linkedin.com/in/cemdenizdemir"><img src="https://img.shields.io/badge/LinkedIn-0D1117?style=for-the-badge&logo=linkedin&logoColor=58A6FF" alt="LinkedIn" /></a>
<a href="mailto:cemdenizdemir@gmail.com"><img src="https://img.shields.io/badge/Email-0D1117?style=for-the-badge&logo=gmail&logoColor=58A6FF" alt="Email" /></a>
<img src="https://img.shields.io/badge/Istanbul,%20Türkiye%20·%20Open%20to%20relocation-0D1117?style=for-the-badge&logo=googlemaps&logoColor=58A6FF" alt="Location" />

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

</div>

## `01` — About

I build production systems across **Node.js/TypeScript** backends and **Next.js** frontends, owning the full delivery lifecycle from architecture through CI/CD.

My focus is **identity and authentication** — and more broadly, treating security as a design constraint rather than a late-stage addition. In practice: OWASP-aligned request handling, argon2 hashing, schema validation at every input boundary, RBAC, and layered rate limiting as defaults, not additions. I apply the same mindset to **performance**: query shape, payload size, and cache behavior are decided at design time, not tuned after the fact.

Currently a Software Engineer at **N-Creative**, where I own order management, data sync, CDN delivery, and internal tooling end to end:

- Replaced full database seeding with an **incremental delta-sync engine** — each deploy transfers only changed records; production mutations run through a sandboxed gateway.
- Cut API response times by restructuring **Prisma queries** and tuning **PostgreSQL indexes**, eliminating recurring N+1 patterns.
- Rebuilt asset delivery on **Cloudflare R2** with automatic WebP conversion and a 1-year edge cache with authorized, URL-precise purge — serving a multilingual site to visitors in 50+ countries.
- Built **Playwright** end-to-end coverage for auth flows and API security paths: sessions, authorization boundaries, rate-limit behavior.
- Traced two production failures in **third-party integrations** to root cause — form submissions blocked only in production by the provider's **Cloudflare bot protection**, and site analytics reporting to another agency's **Google Analytics** property after access was lost — and coordinated the fixes with the owning teams.

<div align="center">

| 🔐 Identity & Auth | 🛡️ Security-First APIs | ⚡ Performance | ⚙️ Distributed Systems |
| :---: | :---: | :---: | :---: |
| Multi-tenant auth services, session handling, access-control boundaries | Hardening the full request lifecycle — not just the login endpoint | Query plans, payload size, edge caching, latency budgets | Moving from framework-level work toward runtime and infrastructure depth |

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

</div>

## `02` — Selected Work

<div align="center">

<a href="https://github.com/cemdenizdemir/nestjs-microservices-api">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=cemdenizdemir&repo=nestjs-microservices-api&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB" alt="NestJS Microservices API" />
</a>
<a href="https://github.com/cemdenizdemir/nextjs-auth-boilerplate">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=cemdenizdemir&repo=nextjs-auth-boilerplate&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB" alt="Auth Boilerplate" />
</a>
<a href="https://github.com/cemdenizdemir/BLOG-REPO-NAME">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=cemdenizdemir&repo=BLOG-REPO-NAME&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB" alt="Blog Platform Backend" />
</a>

</div>

**NestJS Microservices API** — Two-service system (auth + resource) communicating over the NestJS TCP transport layer, fronted by an HTTP API gateway handling routing and shared middleware. Containerized with Docker, orchestrated via docker-compose, deployed to AWS ECS through a GitHub Actions pipeline.

**Auth & Profile Boilerplate** — Production-ready authentication template with a chained middleware stack: rate limiting, security headers, auth validation, request logging. Implements OAuth-to-credentials account linking, nonce-based CSP headers, and authentication-aware redirects across server and client components.

**Blog Platform Backend (×3 stacks)** — The same blog backend built and deployed three times — **Spring Boot**, **ASP.NET Core**, and **NestJS** — with PostgreSQL data access via Spring Data JPA (Hibernate), Entity Framework Core, and TypeORM. Layered architecture, Repository / DI / DTO patterns, and RESTful APIs following each framework's own conventions. Built to compare ecosystems on equal terms rather than in theory.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

</div>

## `03` — AI-Assisted Engineering

I use LLMs as a structured part of my engineering workflow, not as autocomplete. Each recurring review discipline is encoded as a versioned prompt, adapted from primary sources — vendor engineering guidance and practitioner writing (e.g. Anthropic, Cloudflare, Andrej Karpathy) — and attributed per file.

<div align="center">

| Concern | What the prompt enforces |
| :--- | :--- |
| 🛡️ **Security** | Threat-models the change: authorization boundaries, injection surfaces, secrets handling, mapped to OWASP Top 10 / API Top 10 |
| ⚡ **Performance** | N+1 detection, index coverage, payload size, cache headers, per-endpoint latency budget |
| 🏛️ **Architecture** | Trade-offs stated before code — consistency, coupling, failure modes — in an ADR-style output |
| 🪙 **Token efficiency** | Context scoping to the minimal file set, model tier and reasoning-effort selection per task |
| 🧹 **Clean code** | Naming, function size, SOLID violations, dead code, missing tests |

</div>

**Ground rules**

- **AI proposes, I decide.** Every generated change passes type checks, tests, and my own review before merge.
- **Same threat model for my own tooling.** No secrets or customer data in prompts; least-privilege permissions for agents — prompt injection and excessive agency (OWASP LLM Top 10) apply to my workflow, not only to the products I build.
- **Adapted, not copied.** Each prompt links its source and records what I changed and why.

<div align="center">

<a href="https://github.com/cemdenizdemir/ai-prompt-collection">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=cemdenizdemir&repo=ai-prompt-collection&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB" alt="AI Prompt Collection" />
</a>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

## `04` — Stack

**Core**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

**Also shipped in**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![.NET](https://img.shields.io/badge/ASP.NET_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=for-the-badge&logo=trpc&logoColor=white)

**Security & Auth**

![OAuth2](https://img.shields.io/badge/OAuth2-EB5424?style=for-the-badge&logo=auth0&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Auth.js](https://img.shields.io/badge/Auth.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white)
![OWASP](https://img.shields.io/badge/OWASP-000000?style=for-the-badge&logo=owasp&logoColor=white)

**Cloud & Infrastructure**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=FF9900)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=for-the-badge&logo=firebase&logoColor=white)

**Frontend & Tooling**

![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-443E38?style=for-the-badge&logo=react&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

</div>

<details>
<summary><b>Full breakdown</b></summary>

<br>

**Languages** — TypeScript, JavaScript (ES6+), SQL, HTML5, CSS3

**Backend** — Node.js, NestJS, Express.js, REST APIs, GraphQL, tRPC · also shipped with Spring Boot and ASP.NET Core

**Frontend** — React, Next.js, Tailwind CSS, Zustand, TanStack Query

**Databases & ORMs** — PostgreSQL, MySQL, MongoDB, Redis, Prisma ORM, TypeORM, Spring Data JPA (Hibernate), Entity Framework Core

**Architecture** — Microservices, API gateway patterns, caching strategies, database replication and partitioning

**Security & Authentication** — OAuth2/OIDC, JWT, NextAuth/Auth.js, Argon2, RBAC, Zod validation, rate limiting, nonce-based CSP, OWASP Top 10, OWASP API Security Top 10, OWASP Top 10 for LLM Applications, threat modeling

**Cloud & Infrastructure** — AWS (IAM, VPC, ECS, RDS, S3, CloudFront), Azure, Cloudflare (R2, CDN edge caching and purge), Docker, Kubernetes, Vercel, Firebase

**DevOps & Testing** — GitHub Actions CI/CD, Jest, Playwright, Git, Postman

**AI-Assisted Development** — Curated, source-attributed prompt library for security review, performance, architecture, token efficiency, and clean code

<br>

*B.Sc. Computer Engineering, Haliç University — coursework in C, C++, C#, and Java.*

</details>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

</div>

## `05` — Currently Learning

<div align="center">

| | Focus |
| :--- | :--- |
| ![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white) | Concurrency primitives, standard library `net/http`, idiomatic error handling. Working through *Let's Go* / *Let's Go Further*. |
| ![Architecture](https://img.shields.io/badge/Distributed_Systems-1F6FEB?style=flat-square&logo=apachekafka&logoColor=white) | Latency budgets, Amdahl's law, horizontal scaling, reliability engineering (circuit breakers, failover), event-driven and SAGA-based architectures. |
| ![System Design](https://img.shields.io/badge/System_Design-58A6FF?style=flat-square&logo=diagramsdotnet&logoColor=white) | Quality-attribute trade-offs (SLA/SLO/SLI), REST vs. RPC, message brokers, CAP theorem, event stream processing. |
| ![Security](https://img.shields.io/badge/AI_Security-000000?style=flat-square&logo=owasp&logoColor=white) | OWASP Top 10, API Security Top 10, and Top 10 for LLM Applications — including threat modeling for agentic systems. |
| ![AWS](https://img.shields.io/badge/AWS_SAA-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900) | IAM, VPC design, ELB/ASG, RDS/Aurora, ECS/EKS, KMS, CloudWatch — toward Solutions Architect Associate scope. |
| ![Containers](https://img.shields.io/badge/Containers-326CE5?style=flat-square&logo=kubernetes&logoColor=white) | Docker multi-stage builds, Compose orchestration, Kubernetes deployments, services, persistent volumes, networking. |

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:1F6FEB,100:0D1117&height=3" width="100%" alt="divider" />

## `06` — Stats

<img height="165" src="https://github-readme-stats.vercel.app/api?username=cemdenizdemir&show_icons=true&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB&text_color=C9D1D9&hide_title=true" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=cemdenizdemir&layout=compact&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&langs_count=8" alt="Top languages" />

<br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=cemdenizdemir&bg_color=0D1117&color=58A6FF&line=1F6FEB&point=FFFFFF&area=true&hide_border=true" width="98%" alt="Activity graph" />

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58A6FF,50:1F6FEB,100:0D1117&height=120&section=footer&text=Open%20to%20backend%20and%20full-stack%20roles%20%E2%80%94%20remote%20or%20relocation&fontColor=FFFFFF&fontSize=16&fontAlignY=70" width="100%" alt="footer" />

</div>
