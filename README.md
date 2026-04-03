# 🚀 One-Click AI Agent Stack

**A one-command deployment of Flowise, Ollama, and Postgres designed to bypass installation hassle and get AI agents running locally in minutes.**

This repository provides a persistent, production-ready environment that orchestrates your low-code UI, local LLMs, and database using a single Docker Compose file. It eliminates the need to manually install Node.js, Python, or separate database engines on your host machine.

---

## 🛠️ Prerequisites

Before starting, ensure you have Docker installed on your system:

* To install Docker Desktop follow the instructions for your respective OS on : [Docker Desktop](https://www.docker.com/products/docker-desktop/)
* Linux users can choose to work on Docker Engine: [Docker Engine](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/).


---

## 🚀 Getting Started

### Windows

#### 1. Clone and Navigate
Visit [AI_Agents_Using_Flowise](https://github.com/Saleha-Abid/AI_Agents_Using_Flowise.git) and download the code as .zip. Extract it.

#### 2. Launch the Stack
* Open the **Command Prompt** in the Extracted Folder and run:
```cmd
docker compose up -d
```
#### 3. Access Flowise
Open your browser and go to: http://localhost:3000. The page will ask you for previous credentials. Enter them as:

* **Default Login:** admin@flowise.local
* **Default Password:** password123

You can then add new credential personalized to your use.

#### 4. Managing Models (Ollama)
To build AI Agents, you'll need local models such as llama3.2, etc. You must download them. In Command Prompt:

**llama3.2** (AI Model 1)
```cmd
docker exec -it ollama ollama pull llama3.2
```
**mistral** (AI Model 2)
```cmd
docker exec -it ollama ollama pull mistral
```
**nomic-embed-text** (Text Embedding)
```cmd
docker exec -it ollama ollama pull nomic-embed-text
```
---

### Linux

#### 1. Clone and Navigate
Clone this GitHUb repository. Then navigate to the the directory.
```bash
git clone https://github.com/Saleha-Abid/AI_Agents_Using_Flowise.git
cd AI_Agents_Using_Flowise
```

#### 2. Launch the Stack
This command will pull the necessary images and start all services in the background:
```bash
docker compose up -d
```
#### 3. Access Flowise
Open your browser and go to: [http://localhost:3000](http://localhost:3000). The page will ask you for previous credentials. Enter them as:

* **Default Login:** admin@flowise.local
* **Default Password:** password123

You can then add new credential personalized to your use.

#### 4. Managing Models (Ollama)
To build AI Agents, you'll need local models such as llama3.2, etc. You must download them. In the terminal:

**llama3.2** (AI Model 1)
```bash
docker exec -it ollama ollama pull llama3.2
```
**mistral** (AI Model 2)
```bash
docker exec -it ollama ollama pull mistral
```
**nomic-embed-text** (Text Embedding)
```bash
docker exec -it ollama ollama pull nomic-embed-text
```

---

### Note
When building a Agentflow in the Flowise UI, use these settings to connect the nodes:
* Ollama Base URL: http://ollama:11434
(Note: Do not use localhost here; the containers communicate via the internal Docker network name ollama.)
* Postgres Details:
**User**: flowise_user
**Password**: flowise_password
**DataBase**: flowise_db

### Maintenance
* Stop the services (keep the data)
```bash
docker compose stop
```
* Remove containers (keep the data)
```bash
docker compose down
```
