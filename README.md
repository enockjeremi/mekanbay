# Mekanbay 🔧

> Multi-tenant SaaS platform for automotive repair shops, built for the Latin American market.

Mekanbay helps repair shops manage their entire operation in one place — service orders, appointments, vehicle reception, inventory, and customer history — accessible from both web and mobile.

---

## The Problem

Most automotive repair shops in Latin America still manage their operations manually or with generic tools that weren't built for the industry. Mekanbay is designed specifically for this context: unreliable connectivity, mobile-first users, and the real workflow of a mechanic shop.

---

## Core Features

- 🏢 **Multi-tenant architecture** — each shop is fully isolated with its own data
- 📋 **Service orders** — create, track, and manage repair jobs end to end
- 📅 **Appointments** — schedule and manage customer visits
- 🚗 **Vehicle reception** — log vehicle condition on arrival
- 👥 **Customer & vehicle history** — full service records per client
- 🔔 **Real-time notifications** — keep staff and customers informed
- 📱 **Mobile app** — built for mechanics on the shop floor

---

## Tech Stack

### Backend
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### Web
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

### Mobile
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)

### Monorepo
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white)

---

## Architecture

```
mekanbay/
├── apps/
│   ├── api/          # NestJS backend (REST API)
│   ├── web/          # Next.js web application
│   └── mobile/       # React Native / Expo mobile app
├── packages/
│   ├── ui/           # Shared UI components
│   ├── types/        # Shared TypeScript types
│   └── config/       # Shared configs (ESLint, TS, Tailwind)
```

**Key architectural decisions:**
- Modular monolith on the backend: `Controller → Service → Repository` layering
- Shared-database multitenancy with tenant isolation via `workshopId`
- Dual JWT authentication (access token + refresh token)
- Standardized API response structure across all endpoints
- Prisma 7 with driver adapter pattern
- CUID for all entity IDs

---

## Status

🚧 **Currently in active development**

| Module | Status |
|---|---|
| Authentication | ✅ Complete |
| Multi-tenant architecture | ✅ Complete |
| Workshop management | 🔄 In progress |
| Service orders | 🔄 In progress |
| Appointments | 📋 Planned |
| Mobile app | 🔄 In progress |
| Web dashboard | 📋 Planned |

---

## Author

Built by [@enockjeremi](https://github.com/enockjeremi) — automotive mechanic turned full stack developer.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/enockjeremi/)

---

> *This repository contains only the project overview. The source code is private.*
