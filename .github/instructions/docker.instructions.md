---
description: "Dockerfile and Docker Compose containerization conventions."
applyTo: "**/Dockerfile*,**/docker-compose*.{yml,yaml}"
---

- Non-Root Execution: run container application processes as an explicit non-root user; never bake credentials, tokens, or `.env` files into image layers.
- Context Hygiene: maintain a `.dockerignore` file excluding local build outputs (`bin/`, `obj/`, `node_modules/`), VCS (`.git/`), and sensitive local environment files.
- Network Isolation: restrict internal databases, caches, and backing services to private Docker networks; expose only public entrypoints/gateways to the host.
- Compose Reliability: specify explicit service names, healthchecks, restart policies, and named persistent volumes in Compose configurations.
