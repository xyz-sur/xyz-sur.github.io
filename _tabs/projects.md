---
title: Proyek
icon: fas fa-laptop-code
order: 5
---

# 🚀 Portofolio Rekayasa Sistem & Proyek Unggulan

Berikut adalah ikhtisar proyek infrastruktur, sistem otonom, dan aplikasi produksi yang telah saya kembangkan:

---

### 1. 🌐 WorkIT Operations Portal
* **Deskripsi:** Dashboard manajemen operasional dan koordinasi jadwal kerja harian tim General Affairs & IT Support.
* **Teknologi:** Cloudflare Workers, Cloudflare D1 (Serverless SQLite at the edge), Tailwind CSS, Vanilla JS.
* **Fitur Utama:** REST API sinkronisasi tiket instan, generator format rekap WhatsApp *ready-to-copas*, dan sistem otentikasi PIN aman.
* **Tautan:** [workit.msr.my.id](https://workit.msr.my.id)

---

### 2. 🖥️ ServerVoo Proxmox VE Homelab Cluster
* **Deskripsi:** Server infrastruktur mandiri berbasis Proxmox Virtual Environment yang meng-host puluhan kontainer LXC dan VM mikro.
* **Teknologi:** Proxmox VE 8, Debian/Ubuntu Linux, Linux Bridge Dual-NIC (`vmbr0`-`vmbr3`), Tailscale Mesh, Iptables NAT.
* **Layanan Utama:**
  * **CT 125:** Chatwoot CRM + WAHA Engine (Omnichannel CS Platform).
  * **CT 100:** Nextcloud Enterprise Document & HR Management.
  * **CT 106:** Nezha Server & Node Telemetry Monitoring.
  * **CT 118:** Duitx Passive Earn-App Fleet (Micro-services).
  * **CT 130:** Automated ISO/Torrent Sorter Watcher Daemon.
  * **CT 140:** High-throughput CCTV MediaMTX RTSP Gateway.

---

### 3. 🧠 9Router AI Gateway & Inference Load Balancer
* **Deskripsi:** Gerbang perutean cerdas untuk mendistribusikan inferensi multi-model LLM (Claude, Gemini, OpenAI, OpenRouter) dengan latensi terendah.
* **Teknologi:** Python, AsyncIO, Reverse Proxy, FastAPI, Systemd Service.
* **Fitur Utama:** Round-robin adaptif, otomatis fallback saat rate-limit, pemantauan status kesehatan provider, dan proteksi port lokal `20128`.

---

### 4. 🤖 Omnichannel Multi-Bot & Userbot Bridge
* **Deskripsi:** Jembatan komunikasi dua arah antara sistem tiket pelanggan (Chatwoot), WhatsApp API, dan akun Telegram personal.
* **Teknologi:** Python Telethon, Baileys Node.js, Quart Webhook, Ruby Rails Monkey-Patch.
* **Fitur Utama:** Sinkronisasi pesan real-time, penanganan pesan terhapus (*two-way message revoke*), dan pencegahan pesan ganda (*deduplication*).

---

### 5. 📡 OpenStick UZ801 Linux Micro-Server
* **Deskripsi:** Transformasi modem USB 4G LTE murah berbasis chipset Qualcomm Snapdragon 410 (MSM8916) menjadi server Linux mandiri.
* **Teknologi:** OpenWrt, Debian ARM64, Fastboot, EDL Qualcomm Tooling.
* **Fitur Utama:** Gateway VPN portabel, modem router LTE hemat daya (<2W), dan platform eksperimen edge computing.
