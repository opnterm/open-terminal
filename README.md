# ⚡ OpenTerminal

**A lightweight, self-hosted terminal that gives AI agents and automation tools a dedicated environment to run commands, manage files, and execute code — all through a simple API.**

> "A computer you can curl"

## Why OpenTerminal?

AI assistants are great at **writing** code, but they need somewhere safe to **run** it.

OpenTerminal is that place — a remote shell with file management, search, and full execution capabilities, accessible over a clean REST API.

### Two Ways to Run

- **Docker (Recommended)** — Isolated container with rich pre-installed toolkit (Python, Node.js, git, build tools, data science libs, ffmpeg, etc.). Perfect for AI agents.
- **Bare Metal** — Install via `pip` and run natively. Full access to your real files and environment.

## Quick Start

### Docker (Recommended)

```bash
docker run -d --name open-terminal --restart unless-stopped \
  -p 8000:8000 \
  -v open-terminal:/home/user \
  -e OPEN_TERMINAL_API_KEY=your-secret-key \
  ghcr.io/open-webui/open-terminal

Your terminal will be available at http://localhost:8000
Bare Metal (Pip)
Bashpip install open-terminal
open-terminal run --host 0.0.0.0 --port 8000 --api-key your-secret-key
Features

Clean REST API with interactive Swagger documentation
Full file system read/write access
File search and management
Native integration with Open WebUI (including file browser sidebar)
Multi-user isolation mode
Multiple Docker variants: latest, slim, and alpine
Easy pre-installation of packages via environment variables

Links

Website: https://openterminal.sh
GitHub Repository: https://github.com/opnterm/open-terminal
