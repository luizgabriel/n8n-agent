# 🤖 n8n + WAHA (WhatsApp HTTP API) Integration

This repository provides a Docker Compose setup to integrate [n8n](https://n8n.io/) with [WAHA](https://waha.devlike.pro/), enabling automation of WhatsApp interactions through customizable workflows.

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

```env
# n8n Credentials
N8N_USER=your_n8n_username
N8N_PASSWORD=your_n8n_password
N8N_HOST=localhost

# PostgreSQL Credentials
POSTGRES_USER=n8n
POSTGRES_PASSWORD=n8n
POSTGRES_DB=n8n

# WAHA API Key
WAHA_API_KEY=your_waha_api_key
```

Replace `your_n8n_username`, `your_n8n_password`, and `your_waha_api_key` with your desired credentials.

---

## 🚀 Getting Started

### 1. Start the Services

In your terminal, navigate to the project directory and run:

```bash
docker-compose up -d
```

This command will build and start the containers in detached mode.

### 2. Access the Applications

- **n8n**: Open your browser and navigate to [http://localhost:5678](http://localhost:5678).
- **WAHA Dashboard**: Open your browser and navigate to [http://localhost:3000/dashboard](http://localhost:3000/dashboard).

---

## 🔌 Integrating WAHA with n8n

### 1. Install WAHA Node in n8n

- In n8n, navigate to **Settings** > **Community Nodes**.
- Search for `@devlikeapro/n8n-nodes-waha` and install it.

### 2. Configure WAHA Credentials in n8n

- Go to **Credentials** > **New Credential**.
- Select **WAHA API**.
- Set the **Host URL** to `http://waha:3000`.
- Set the **API Key** to the value of `WAHA_API_KEY` from your `.env` file.
- Save the credentials.

### 3. Create a Workflow

- Use the WAHA Trigger node to listen for incoming WhatsApp messages.
- Use the WAHA Send Message node to send responses.

---

## 📚 Additional Resources

- **WAHA Official Website**: [https://waha.devlike.pro/](https://waha.devlike.pro/)
- **WAHA + n8n Integration Guide**: [https://waha.devlike.pro/blog/waha-n8n/](https://waha.devlike.pro/blog/waha-n8n/)
- **WAHA n8n Nodes GitHub Repository**: [https://github.com/devlikeapro/n8n-nodes-waha](https://github.com/devlikeapro/n8n-nodes-waha)
