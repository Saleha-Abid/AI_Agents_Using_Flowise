# 🚀 One-Click AI Agent Stack

**A one-command deployment of Flowise, Ollama, and Postgres designed to bypass installation hassle and get AI agents running locally in minutes.**

This repository provides a persistent, production-ready environment that orchestrates your low-code UI, local LLMs, and database using a single Docker Compose file. It eliminates the need to manually install Node.js, Python, or separate database engines on your host machine.

---

## 🛠️ Prerequisites

Before starting, ensure you have Docker installed on your system:

* **Windows:** Install [Docker Desktop](https://www.docker.com/products/docker-desktop/). 
    * *Tip: Ensure "Use the WSL 2 based engine" is checked in Settings > General.*
* **Linux:** Install [Docker Engine](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/).
    * *Tip: Add your user to the `docker` group to avoid using `sudo` for every command.*

---

## 🚀 Getting Started

### 1. Clone & Navigate
Open your terminal (PowerShell on Windows, Bash on Linux) and run:
```bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name
