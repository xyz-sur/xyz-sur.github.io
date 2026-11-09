---
title: Portofolio
icon: fas fa-briefcase
order: 1
---

<meta http-equiv="refresh" content="0; url=/portofolio/">
<script>
  if (window.location.pathname.includes('/tabs/projects')) {
    window.location.replace('/portofolio/');
  }
</script>

<div class="alert alert-info border border-info border-opacity-25 rounded-3 p-3 mb-4 font-mono small d-flex justify-content-between align-items-center">
  <span><i class="fas fa-external-link-alt me-2"></i> Ingin melihat portofolio interaktif versi lengkap?</span>
  <a href="/portofolio/" class="btn btn-sm btn-info rounded-pill px-3 fw-bold text-dark text-nowrap">Buka Portofolio Lengkap &rarr;</a>
</div>

# 🚀 Portofolio Rekayasa Sistem, Layanan & Proyek GitHub

Koleksi lengkap seluruh infrastruktur produksi, sistem otomasi, repositori kode sumber terbuka, dan layanan korporat yang dikembangkan oleh **Bang Mansur**:

---

## 🛡️ I. Layanan Bisnis & Solusi Produksi

### 1. 📶 Setting & Perbaikan Jaringan WiFi / LAN Kantor
* **Cakupan:** Kantor ruko, kafe, homelab, dan instansi.
* **Teknologi:** MikroTik RouterOS, Ubiquiti UniFi, Cisco, Tailscale Mesh VPN.
* **Kapabilitas:** Pembagian bandwidth cerdas (QoS anti-lag), multi-WAN load balancing & auto failover (koneksi tetap hidup saat salah satu ISP putus), segmentasi VLAN terisolasi, serta VPN tunnel aman antar-cabang.

### 2. 🛡️ Audit Keamanan Website & Penanganan Anti-Hack
* **Cakupan:** Web e-commerce, portal instansi, API backend, dan server publik.
* **Teknologi:** OWASP Top 10 Security Audit, Cloudflare WAF & Zero-Trust, Nginx Hardening, Linux Kernel sysctl tuning.
* **Kapabilitas:** Audit celah SQLi/XSS/RCE, mitigasi DDoS/Bot traffic, pemulihan website pasca-serangan deface atau malware, dan penerapan arsitektur *Zero-Leak Credentials*.

### 3. 🤖 Bot WhatsApp & Telegram Otomatisasi Bisnis
* **Cakupan:** Customer Service 24/7, bot transaksi produk digital, dan notifikasi CRM.
* **Teknologi:** Node.js (Baileys WhatsApp Engine), Python (Telethon AsyncIO), Webhook Queue, SQLite/D1.
* **Kapabilitas:** Balas pesan instan, order otomatis, sinkronisasi tiket Chatwoot Omnichannel dua arah, dan pencegahan duplikasi pesan (*anti-spam*).

### 4. 💳 Integrasi Gerbang Pembayaran QRIS Dinamis Otomatis
* **Cakupan:** Web toko online, bot transaksi, dan platform top-up.
* **Teknologi:** Webhook Settlement, QRIS Dinamis (BCA, BRI, Mandiri, BNI, e-Wallet), Real-time Mutasi API.
* **Kapabilitas:** Generate QR code unik per transaksi, verifikasi lunas otomatis dalam hitungan detik tanpa perlu upload bukti transfer atau cek mutasi rekening manual.

### 5. 🖥️ Setup Server Proxmox VE, VPS & Backup Cloud Anti-Ransomware
* **Cakupan:** Server on-premise kantor dan cloud VPS Ubuntu/Debian.
* **Teknologi:** Proxmox VE 8, Linux Containers (LXC), ZFS Storage Pool, Rclone, Backblaze B2, AES-256 GPG.
* **Kapabilitas:** Virtualisasi server hemat resource, isolasi jaringan dual-NIC, dan pencadangan otomatis terenkripsi harian jam 00:00 WIB ke cloud offsite.

### 6. 🎓 Konsultasi IT Privat, Bimbingan Coding & Asistensi Riset Komputer S2
* **Cakupan:** Developer pemula/menengah dan mahasiswa pascasarjana.
* **Materi:** Arsitektur backend, otomasi agen AI, metodologi eksperimen sains komputer, asistensi tesis S2, serta penulisan paper publikasi standar SINTA 2 / Scopus.

### 7. 📱 Layanan Pengecekan IMEI & Validasi CEIR Telekomunikasi
* **Tautan:** [cekimei.my.id](https://cekimei.my.id) | Bot: `@cekceirbot`
* **Kapabilitas:** Sistem pengecekan status pendaftaran legalitas nomor IMEI perangkat resmi ke database Bea Cukai dan Kemenperin secara otomatis melalui bot dan website.

### 8. ⚡ Server Pulsa, Paket Data & Gateway PPOB H2H
* **Tautan:** [apiaing.msr.my.id](https://apiaing.msr.my.id)
* **Kapabilitas:** Distributor produk digital tangan pertama (pulsa nasional, paket data kuota, token PLN, voucher game) yang beroperasi 24 jam via API H2H terintegrasi.

### 9. 📋 Sistem Manajemen Tugas & Laporan Operasional WorkIT
* **Tautan:** [workit.msr.my.id](https://workit.msr.my.id)
* **Teknologi:** Cloudflare Workers, Cloudflare D1 Serverless Database, Tailwind CSS.
* **Kapabilitas:** Manajemen koordinasi kerja tim General Affairs & IT, pencatatan absensi, dan generator teks rekap WhatsApp berformat rapi siap kirim.

---

## 💻 II. Repositori GitHub & Proyek Open-Source

### 1. 🤖 [xyz-sur / telegram-tele-id-bot](https://github.com/xyz-sur/telegram-tele-id-bot)
* **Kategori:** *Edge Computing / Telegram Engine*
* **Deskripsi:** Bot Telegram berkecepatan tinggi untuk membaca User ID, detail chat, status keanggotaan, dan mesin broadcast informasi yang dideploy di Cloudflare Workers Edge.
* **Stack:** JavaScript, Cloudflare Workers API, Cloudflare D1.

### 2. 💳 [xyz-sur / qiospay-automation](https://github.com/xyz-sur/qiospay-automation)
* **Kategori:** *Fintech Payment Gateway*
* **Deskripsi:** Script otomasi integrasi pembayaran QRIS dinamis multi-bank dengan pengecekan callback webhook instan dan sinkronisasi zona waktu WIB.
* **Stack:** Python, Node.js, Express, REST API.

### 3. 🐧 [xyz-sur / openwrt-build](https://github.com/xyz-sur/openwrt-build)
* **Kategori:** *Embedded Linux & Networking*
* **Deskripsi:** Toolchain kompilasi kustom firmware OpenWrt dan kernel Linux yang dioptimalkan untuk modem stick Snapdragon MSM8916 (UZ801) dan router TP-Link.
* **Stack:** C, Shell Script, Makefile, OpenWrt SDK.

### 4. 👾 [xyz-sur / Agent-Pixels](https://github.com/xyz-sur/Agent-Pixels)
* **Kategori:** *Autonomous AI Agent Simulation*
* **Deskripsi:** Dashboard simulasi visual bergaya pixel art (*Pixel Office SOC*) untuk memantau status runtime, aktivitas percakapan, dan alokasi resource agen AI otonom di server.
* **Stack:** HTML5 Canvas, JavaScript, CSS3.

### 5. ⌚ [xyz-sur / mi_fitness_data_bridge](https://github.com/xyz-sur/mi_fitness_data_bridge)
* **Kategori:** *Wearable Telemetry & Health Ops*
* **Deskripsi:** Jembatan ekstraksi data detak jantung, pola tidur, dan telemetri kesehatan dari perangkat wearable ke dashboard analitik lokal.
* **Stack:** Python, SQLite, JSON Schema.

---

## 🏢 III. Arsitektur Infrastruktur & Homelab Mandiri

* **Proxmox Cluster ServerVoo:** Menjalankan 17 container LXC terisolasi (Chatwoot, Nextcloud, Nezha Telemetry, CCTV MediaMTX, Duitx Fleet) dan 2 Virtual Machine.
* **9Router AI Inference Gateway:** Layanan lokal port `20128` untuk load balancing dan failover multi-provider LLM berkecepatan tinggi dengan latensi terendah.
* **Jaringan Mesh Tailscale:** Jaringan privat terenkripsi WireGuard menghubungkan seluruh server homelab, workstation Parrot OS, dan VPS cloud tanpa port forwarding publik yang rentan.
