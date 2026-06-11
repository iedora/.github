<p align="center">
  <picture>
    <img alt="iedora" src="https://avatars.githubusercontent.com/u/291901846" width="96" height="96" style="border-radius: 12px">
  </picture>
</p>

<h1 align="center">iedora</h1>
<p align="center"><strong>Self-hosted multi-tenant SaaS for restaurants to build digital drag-and-drop menus.</strong></p>

---

## Architecture

| Repo | Language | Purpose |
|------|----------|---------|
| [`backend`](https://github.com/iedora/backend) | Go | Microservices: auth, menu, admin, audit, billing |
| [`web`](https://github.com/iedora/web) | TypeScript | Next.js 16 frontend — product dashboard, public menus, brand landing |
| [`infra`](https://github.com/iedora/infra) | HCL / Ansible | Self-hosted deployment: Docker Swarm, OpenTofu, Authelia SSO |

## Tech stack

| Layer | Technology |
|-------|------------|
| **Backend** | Go 1.25 · chi/v5 · pgx · NATS JetStream · Ed25519 JWTs |
| **Frontend** | Next.js 16 · React 19 · TypeScript · Tailwind CSS v4 · Radix UI · dnd-kit |
| **Infrastructure** | Docker Swarm · Ansible · OpenTofu · Traefik · Authelia |
| **Observability** | OpenTelemetry (traces + metrics + logs) → Grafana LGTM |
| **Storage** | PostgreSQL 18 · S3-compatible (Cloudflare R2 / MinIO) |
| **CI/CD** | GitHub Actions · Renovate |
| **Package manager** | Bun (workspaces) |

## Microservices

| Service | Port | Role |
|---------|------|------|
| **auth** | 8080 | JWT (Ed25519) + session management, user/tenant CRUD, service-to-service grant |
| **menu** | 8084 | Restaurant menu CRUD, publishing, QR codes, analytics, uploads |
| **admin** | 8082 | Staff BFF — server-rendered HTML via Go templ + HTMX |
| **audit** | 8081 | NATS JetStream consumer, transactional outbox audit log |
| **billing** | 8083 | Plan gating, Stripe integration |

## Quick start

```bash
git clone https://github.com/iedora/web.git
cd web
bun install
bun run dev:up    # Boot Go backend + Postgres + NATS + MinIO
bun run dev       # Next.js dev server on :3000
```

The app runs two hostnames from a single Next.js container:
- **menu.iedora.com** — product dashboard + public menus
- **iedora.com** — brand landing page

## Principles

- **Backend owns data & auth** — Go services are the source of truth; the TypeScript frontend is a thin typed pass-through with zero data layer.
- **Vertical slices** — features own their UI, loaders, and server actions. No cross-cutting layers.
- **12-factor config** — every service binds config from the environment.
- **Observability-first** — every service boots OpenTelemetry SDK; baggage propagates tenant, user, and request IDs through the full call chain.
- **Conventional commits** — enforced by pre-commit hooks.
