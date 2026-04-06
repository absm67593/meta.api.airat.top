# AGENTS.md

## Purpose
Public API for extracting webpage metadata from a provided URL.

## Repository Role
- Category: `*.api.airat.top` (public API project).
- Deployment platform: Cloudflare Workers.
- Main files: `worker.js`, `wrangler.toml`.

## API Summary
- Live endpoint: `https://meta.api.airat.top`.
- Status page: `https://status.airat.top`.
- Required param: `url` (absolute `http`/`https`).
- Routes: `/`, `/json`, `/text`, `/yaml`, `/xml`, `/health`.

## AI Working Notes
- Keep URL validation strict and return `400` for invalid input.
- Preserve key metadata fields (`title`, `description`, `canonical`, Open Graph, Twitter).
- Keep CORS enabled and health endpoint stable.
