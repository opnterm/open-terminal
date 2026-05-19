# ⚡ OpenTerminal

**A lightweight, self-hosted terminal that gives AI agents and automation tools a dedicated environment to run commands, manage files, and execute code — all through a simple API.**

> A computer you can curl.

---

## Why OpenTerminal?

AI assistants are great at writing code, but they need a safe place to **run** it.

OpenTerminal provides a clean, secure, and simple remote terminal accessible via REST API.

### Two Ways to Run

- **🐳 Docker (Recommended)** — Sandboxed environment with rich tools pre-installed.
- **💻 Bare Metal** — Install via pip and run natively on your machine.

### Features

- Clean REST API with interactive Swagger docs (/docs)
- Full file system read/write access
- File search and management
- Native Open WebUI integration (with file browser sidebar)
- Multi-user isolation mode
- Multiple Docker variants: latest, slim, alpine
- Easy package pre-installation via environment variables

### Links

- Website → https://openterminal.sh
- GitHub → https://github.com/opnterm/open-terminal

## Quick Start

### Docker (Recommended)

```bash
docker run -d --name open-terminal --restart unless-stopped \
  -p 8000:8000 \
  -v open-terminal:/home/user \
  -e OPEN_TERMINAL_API_KEY=your-secret-key \
  ghcr.io/open-webui/open-terminal

pip install open-terminal
open-terminal run --host 0.0.0.0 --port 8000 --api-key your-secret-key
