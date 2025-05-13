# 🤖 n8n

This repository provides a Docker Compose setup to integrate [n8n](https://n8n.io/).

---

## 🧰 Prerequisites

Ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## ⚙️ Configuration

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/luizgabriel/n8n.git
cd n8n
```

### 2. Set Up Environment Variables

Create a `.env` file in the root directory of the project with the following content:

```bash
cp .env.example .env
```

---

## 🚀 Getting Started

### 1. Start the Services

In your terminal, navigate to the project directory and run:

```bash
docker compose up -d
```

This command will build and start the containers in detached mode.

### 2. Access the Applications

- **n8n**: Open your browser and navigate to [http://localhost:5678](http://localhost:5678).
