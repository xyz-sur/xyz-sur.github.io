---
title: "Rekayasa Jaringan: Optimasi QoS MikroTik RouterOS & Esensi Kalkulasi Subnetting CIDR"
date: 2026-11-09 09:30:00 +0700
categories: [Networking, RouterOS]
tags: [mikrotik, qos, subnetting, cidr, bandwidth, network-engineering]
description: "Panduan mendalam arsitektur pembagian bandwidth adil (QoS) menggunakan Simple Queue Burst di MikroTik dan kalkulasi efisiensi subnet mask IPv4."
pin: true
---

# 📶 Rekayasa Bandwidth: Dari Teori Subnetting ke Implementasi Nyata

Dalam manajemen infrastruktur jaringan kantor, kafe, maupun *data center*, dua tantangan terbesar seorang *Network Engineer* adalah efisiensi alokasi alamat IP (*IP Address Exhaustion*) dan pencegahan perebutan bandwidth antar-pengguna (*Bufferbloat & Bandwidth Hogging*).

Artikel ini mengulas penerapan teknis perancangan alokasi CIDR IPv4 serta formula konfigurasi **MikroTik Simple Queue Burst** agar koneksi tetap responsif bagi seluruh pengguna.

---

## 🧮 1. Esensi Alokasi Subnetting CIDR (Classless Inter-Domain Routing)

Sering kali administrator jaringan menerapkan prefix subnet `/24` (254 host) secara seragam di seluruh segmen. Hal ini menyebabkan pemborosan ruang alamat IP dan memperlebar *broadcast domain*, yang pada akhirnya membebani CPU perangkat router switch.

### Perbandingan Efisiensi CIDR:
* **Point-to-Point Tunnel (VPN / Router-to-Router):** Gunakan prefix `/30` (4 IP, 2 usable host) atau `/31` (RFC 3021).
* **Segmentasi Server Terisolasi (DMZ / Proxmox VM):** Prefix `/28` (16 IP, 14 usable host) atau `/27` (32 IP, 30 usable host).
* **VLAN Karyawan / Hotspot Tamu:** Prefix `/23` (512 IP, 510 usable host) untuk kantor skala menengah dengan alokasi DHCP pool yang leluasa.

> 💡 **Tip:** Anda dapat menggunakan utilitas interaktif [IPv4 Subnet Calculator](/tools/subnet-calculator/) yang telah saya sediakan di web ini untuk menghitung secara instan *Network Address, Broadcast Address, Wildcard Mask,* serta rentang *Usable Host*.

---

## ⚡ 2. Optimasi Bandwidth dengan MikroTik Simple Queue Burst

Masalah umum pada pembagian bandwidth kantor: jika bandwidth dibatasi secara statis (misalnya 5 Mbps per user), pengguna akan merasa loading web atau unduhan file kecil terasa lambat. Namun jika tidak dibatasi, satu pengguna yang mendownload file besar atau streaming resolusi 4K akan melumpuhkan koneksi pengguna lainnya.

Solusi tepatnya adalah menerapkan **Burst Mechanism**.

### Cara Kerja Algoritma Burst MikroTik
Burst memungkinkan pengguna melampaui batas kecepatan maksimal (*Max Limit*) selama durasi singkat di awal sesi (misal saat membuka halaman web atau mengunduh gambar), lalu otomatis turun ke batas normal saat trafik berlangsung secara kontinu.

### Parameter Kunci:
1. **Max Limit:** Kecepatan batas normal jangka panjang pengguna (misal `10 Mbps`).
2. **Burst Limit:** Kecepatan puncak yang diizinkan selama burst aktif (rekomendasi: `1.5x` s.d. `2x` Max Limit, misal `15 Mbps`).
3. **Burst Threshold:** Batas ambang rata-rata trafik untuk mematikan mode burst (rekomendasi: `0.75x` Max Limit, misal `7.5 Mbps`).
4. **Burst Time:** Rentang jendela waktu (dalam detik) di mana router menghitung kecepatan rata-rata pengguna.

### Contoh Script Konfigurasi RouterOS:

```routeros
# Penerapan Simple Queue dengan Burst untuk segmen Kantor
/queue simple
add name="Queue-Staff-VLAN10" target=192.168.10.0/24 \
    max-limit=10M/10M \
    burst-limit=16M/16M \
    burst-threshold=7M/7M \
    burst-time=16s/16s \
    queue=pcq-upload-default/pcq-download-default \
    priority=8/8
```

> ⏱️ Untuk menghitung estimasi waktu transfer file dan simulasi formula Burst MikroTik di atas, gunakan tool [Bandwidth & Transfer Calculator](/tools/bandwidth-calculator/).

---

## 🛡️ 3. Kesimpulan

Dengan memadukan perancangan subnetting CIDR yang presisi dan penerapan QoS MikroTik berbasis *Burst Rate*, latensi jaringan kantor dapat ditekan ke tingkat minimal, mencegah lonjakan *ping jitter*, dan memaksimalkan kepuasan seluruh pengguna jaringan.
