# OllamaBroker Pro 🚀

A lightweight, production-ready Windows load balancer and request queuing system designed specifically for **Ollama** backend servers. Prevent your local LLM instances from crashing due to VRAM overflow or simultaneous user requests.

---

## 🛒 Get OllamaBroker Pro
OllamaBroker Pro is distributed as a standalone Windows executable (`.exe`). No Python installation or Docker required.

👉 **[Buy OllamaBroker Pro on Gumroad ($19)](https://mazeikadm.gumroad.com/l/gdpjxw)** *(👉 Įklijuok savo tikslią nuorodą čia!)*

---

## 🔥 Key Features

* **Smart Request Queuing (FIFO):** Handles concurrent API requests and processes them sequentially to protect your GPU/VRAM from crashing.
* **Load Balancing:** Automatically distributes incoming requests across multiple Ollama backend servers.
* **Failover Protection:** If one Ollama instance goes offline, the broker instantly redirects traffic to available backends without dropping user sessions.
* **Zero Dependencies:** Fully compiled `.exe` – works out of the box on standard Windows environments.

---

## 🛠️ Configuration Example (`config.json`)

To set up your cluster, simply create a `config.json` file next to the executable:

```json
{
  "backends": [
    "[http://127.0.0.1:11434](http://127.0.0.1:11434)",
    "[http://192.168.1.50:11434](http://192.168.1.50:11434)"
  ]
}
