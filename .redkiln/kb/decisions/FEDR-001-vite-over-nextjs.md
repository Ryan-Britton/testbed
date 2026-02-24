# FEDR-001: Vite + React over Next.js

**Status:** Accepted
**Date:** 2025-01-31
**Deciders:** Architecture Review

## Context

The console is a dashboard-style SPA for managing AI agent pipelines. Key requirements: rapid iteration with AI-assisted development, real-time streaming and WebSocket support, no SEO requirements.

Options considered:
1. **Next.js** — Full-featured React framework with SSR/SSG
2. **Vite + React** — Lightweight build tool with fast HMR

## Decision

**Chose Vite + React** without a meta-framework.

## Rationale

1. **Sub-100ms HMR** — Critical for rapid iteration with AI assistants
2. **Simpler mental model** — No server/client component boundaries to reason about
3. **Better AI comprehension** — AI tools understand vanilla React patterns more reliably than Next.js conventions
4. **No SSR/SSG needed** — Private dashboard, not a public marketing site
5. **Lighter weight** — No framework overhead for features we don't need

## Consequences

### Positive

- Faster development iteration cycles
- Simpler codebase, easier AI-assisted development
- Full control over routing and data fetching patterns
- Smaller bundle, faster initial load for authenticated users

### Negative

- No built-in SSR if SEO is ever needed (unlikely for this app)
- Must configure routing separately (using React Router v7)
- No API routes (backend is separate FastAPI service)

## References

- [Vite Documentation](https://vite.dev/)
