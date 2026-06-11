<p align="center">
  <picture>
    <img alt="iedora" src="https://avatars.githubusercontent.com/u/291901846" width="96" height="96" style="border-radius: 12px">
  </picture>
</p>

<h1 align="center">iedora</h1>
<p align="center"><strong>The Driver of the House.</strong></p>

<p align="center">
  <em>Scalable infrastructure · AI-integrated products · Pragmatic engineering</em>
</p>

---

## About Us

**iedora** is a software company built on the principle that technology should be durable, fast, and high-quality.

Our name comes from two roots: **ie** (家, the Japanese word for *house*) and **dora** (short for *driver* — the component that connects, commands, and powers a system). Together, iedora means **"The Driver of the House"** — the core technological engine that modernizes businesses from within.

We are a small house in Oporto and Lisboa. Patient work, quiet interfaces.

---

## What We Do

### Products

We build production-grade software for real-world operations.

Our flagship — **[menu](https://github.com/iedora/frontend)** — is a digital menu platform for the restaurant and hospitality industry: a drag-and-drop menu builder, QR code publishing, real-time analytics, and multi-language support. Designed for durability, not for demos.

### AI Training

We upskill teams and businesses in AI implementation — from foundational concepts to production deployment. Practical, hands-on programs focused on what actually works, not what's trending.

### Technical Consulting

Expert guidance on architecture, infrastructure, and software delivery. We help teams design systems that scale without complexity, and ship without compromise.

---

## Engineering Principles

Everything we build follows these commitments:

- **12-factor config** — Every service binds configuration from the environment. No hardcoded secrets, no environment-specific branches.
- **Vertical slices** — Features own their UI, loaders, and server actions. No cross-cutting data layers, no leaky abstractions.
- **Backend-owns-data** — Go services are the source of truth for all auth and persistence. The frontend is a thin typed pass-through with zero data layer.
- **Observability-first** — Every service boots OpenTelemetry at startup. Traces, metrics, and logs flow via OTLP to a Grafana LGTM stack; baggage propagates tenant, user, and request IDs through every call.
- **Integration tests first** — Core logic is tested against real dependencies (PostgreSQL via testcontainers, NATS JetStream, S3-compatible storage). Unit tests cover pure functions; everything else earns its keep through integration coverage.
- **Conventional commits** — Enforced by pre-commit hooks. Every commit message carries its intent.

---

## Our Ecosystem

| Layer | Practice |
|-------|----------|
| **Backend** | Go · chi · pgx · NATS JetStream · Ed25519 JWTs |
| **Frontend** | Next.js · React · TypeScript · Tailwind CSS · Radix UI |
| **Infrastructure** | Docker Swarm · Ansible · OpenTofu · Traefik · Authelia SSO |
| **Observability** | OpenTelemetry → Grafana LGTM |
| **Storage** | PostgreSQL · S3-compatible (R2 / MinIO) |
| **CI/CD** | GitHub Actions · Renovate |
| **Package** | Bun (workspaces) |

---

## Work with Us

We take on select projects in product development, AI implementation, and technical consulting.

Reach out at **[hello@iedora.com](mailto:hello@iedora.com)**.
