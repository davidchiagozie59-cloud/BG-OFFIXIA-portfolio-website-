# BG OFFIXIA Portfolio Website

## Overview
Static single-page HTML website (no backend, no build system, no dependencies).
All CSS and JS are inline in `index.html`. External assets (fonts, Font Awesome, GSAP) are loaded via CDN.

## Running
```bash
docker compose -f docker-compose.base44.yml up -d --build
```
Served by `python3 -m http.server` on port 3000. The source is bind-mounted read-only, so edits to `index.html` are reflected on browser refresh — call `reload_preview` after changes since there is no live-reload dev server.

## Verification
```bash
curl -s http://localhost:3000/ | head -5   # should return the HTML doctype + <title>BG OFFIXIA
```

## Secrets
None required — this is a purely static site with no external service credentials.
