# OllamaBroker Pro 🚀

An enterprise-grade, high-performance Windows load balancer and request queuing system designed specifically for **Ollama** backend servers. Eliminate local LLM server crashes and manage multi-user traffic seamlessly.

---

## 🛒 Get OllamaBroker Pro
OllamaBroker Pro is distributed as a standalone Windows executable (`.exe`). No Python installation, complex registries, or Docker environments are required.

👉 **[Buy OllamaBroker Pro on Gumroad ($19)](https://mazeikadm.gumroad.com/l/gdpjxw)**

---

## 📝 Product Overview

Deploying open-source Large Language Models (LLMs) locally via Ollama is a game-changer for data privacy and cost reduction. However, anyone trying to scale Ollama for multi-user environments quickly hits a major technical bottleneck: **Ollama lacks a native request queuing and load-balancing infrastructure.** When multiple developers, employees, or AI agents send requests to a single Ollama instance simultaneously, the system attempts to process them all at once. This leads to immediate VRAM overflow, extreme latency, and ultimate server crashes. 

**OllamaBroker Pro fixes this exact issue.**

OllamaBroker Pro acts as an intelligent, high-performance middleware layer positioned directly between your AI applications (such as Open WebUI, custom Python scripts, or corporate chatbots) and your Ollama backend infrastructure. Written in highly optimized asynchronous Python (`FastAPI` & `asyncio`) and compiled into a standalone, dependency-free Windows executable, it provides robust traffic management with virtually zero resource overhead.

---

## 🔥 Key Features

* **Deterministic FIFO Request Queuing:** Instead of letting concurrent API requests overwhelm your GPU, OllamaBroker Pro safely holds incoming traffic in a structured queue. It feeds requests to your hardware sequentially, maximizing throughput while keeping your hardware safely within its VRAM limits.
* **Dynamic Load Balancing:** Scale horizontally with ease. Simply add multiple Ollama backend instances across your local network (LAN) or cloud virtual private servers (VPS). The broker automatically distributes incoming inference loads evenly across all active machines.
* **Seamless Failover Protection:** If a specific Ollama node goes offline due to a network glitch or system failure, the broker instantly detects the dropout and reroutes active user sessions to healthy nodes in real time. Your users experience zero downtime.
* **Zero Dependencies:** Designed specifically for quick enterprise deployment. Just unpack the ZIP file, configure your IP list, and run.

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
🚀 Quick Start (After Purchase)
Download and extract your broker.zip from Gumroad.

Set your unique Gumroad license key as an environment variable in PowerShell:

PowerShell
$env:OLLAMA_BROKER_LICENSE="Your-Gumroad-License-Key"
Launch the broker:

PowerShell
.\broker.exe
Change your AI applications (like Open WebUI or custom scripts) to point to the Broker's port instead of direct Ollama ports.

📧 Support & Contact
For license validation issues, feature requests, or enterprise inquiries, feel free to contact us at mazeikadm@gmail.com.
