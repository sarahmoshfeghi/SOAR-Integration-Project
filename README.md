# SOAR Integration Lab 🚀

## 🔍 Overview
This project is a fully integrated SOAR environment designed to simulate real-world security operations. It combines key tools like:
- 🐝 TheHive (Case Management)
- 🧠 Cortex (Automated Analysis)
- 🛰️ MISP (Threat Intelligence Sharing)
- 🔄 Shuffle (Security Automation & Playbooks)

All services run on a single machine using Docker Compose, creating a portable and easily deployable lab environment.

---

## 🏗️ Architecture
```plaintext
[ Shuffle ] ↔ [ TheHive ] → [ Cortex ] → [ MISP ]

