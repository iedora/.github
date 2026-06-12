<p align="center">
  <picture>
    <img alt="iedora" src="https://avatars.githubusercontent.com/u/291901846" width="96" height="96" style="border-radius: 12px">
  </picture>
</p>

<h1 align="center">iedora</h1>
<p align="center"><strong>The Driver of the House.</strong></p>

---

## About Us

**iedora** is a software company. We build tools for restaurants: digital menus, QR code publishing, analytics. Small team based in Portugal.

Our name comes from two roots: **ie** (家, Japanese for *house*) and **dora** (short for *driver*). Together, iedora means "The Driver of the House": the engine that modernizes a business from the inside.

---

## What We Do

### Products

Our flagship is **[menu](https://github.com/iedora/frontend)**: a drag-and-drop menu builder, QR code publishing, real-time analytics, multi-language support. Free for one restaurant.

### AI Training

We run hands-on AI training for teams. From basic concepts to production deployment. Focused on what works, not what is trending.

### Technical Consulting

Architecture, infrastructure, software delivery. We help teams design systems that scale without adding complexity.

---

## Engineering Principles

- **12-factor config**: Every service reads config from the environment. No hardcoded secrets.
- **Vertical slices**: Features own their UI, loaders, and server actions. No leaky abstractions.
- **Backend-owns-data**: Go services are the source of truth. The frontend is a typed pass-through.
- **Observability-first**: OpenTelemetry at startup. Traces, metrics, logs to Grafana LGTM.
- **Integration tests first**: Core logic tested against Postgres, NATS, S3. Unit tests cover pure functions.
- **Conventional commits**: Enforced by pre-commit hooks.

---

## Our Ecosystem

| Layer | Practice |
|-------|----------|
| **Backend** | Go, chi, pgx, NATS JetStream, Ed25519 JWTs |
| **Frontend** | Next.js, React, TypeScript, Tailwind CSS, Radix UI |
| **Infrastructure** | Docker Swarm, Ansible, OpenTofu, Traefik, Authelia SSO |
| **Observability** | OpenTelemetry to Grafana LGTM |
| **Storage** | PostgreSQL, S3 (R2 / MinIO) |
| **CI/CD** | GitHub Actions, Renovate |
| **Package** | Bun workspaces |

---

## Work with Us

Select projects in product development, AI implementation, and technical consulting.

[hello@iedora.com](mailto:hello@iedora.com)
[+351 917 140 356](tel:+351917140356)
