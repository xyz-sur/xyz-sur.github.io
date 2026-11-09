---
title: Utilitas & Tools
icon: fas fa-toolbox
order: 2
---

<meta http-equiv="refresh" content="0; url=/tools/">
<script>
  if (window.location.pathname.includes('/tabs/tools')) {
    window.location.replace('/tools/');
  }
</script>

<div class="alert alert-info border border-info border-opacity-25 rounded-3 p-3 mb-4 font-mono small d-flex justify-content-between align-items-center">
  <span><i class="fas fa-toolbox me-2"></i> Kunjungi portal utilitas interaktif mandiri <strong>Mansur IT Tools</strong>:</span>
  <a href="/tools/" class="btn btn-sm btn-info rounded-pill px-3 fw-bold text-dark text-nowrap">Buka Mansur IT Tools &rarr;</a>
</div>

# 🧰 Web Developer, Networking & SecOps Tools

Koleksi perangkat utilitas berbasis browser yang berjalan **100% secara client-side** langsung di browser Anda tanpa mengirimkan data atau riwayat komputasi ke server luar (*Zero-Leak Architecture*):

---

### 1. 📶 [IPv4 Subnet & CIDR Calculator](/tools/subnet-calculator/)
* **Kategori:** *Networking & SRE Operations*
* **Fungsi:** Menghitung otomatis Network IP, Broadcast IP, Subnet Mask, Wildcard, representasi biner, dan total rentang *usable hosts* untuk alokasi CIDR `/1` hingga `/32`.
* **Cocok untuk:** Konfigurasi router MikroTik, penataan VLAN, dan segmentasi Linux Bridge Proxmox VE.
* **[Buka Subnet Calculator &rarr;](/tools/subnet-calculator/)**

---

### 2. ⚡ [Network Ping & HTTP Latency Tester](/tools/ping-tester/)
* **Kategori:** *Network Diagnostic & Performance*
* **Fungsi:** Mengukur waktu respon *round-trip time* (RTT) instan dari koneksi internet browser Anda ke gateway CDN global (Cloudflare 1.1.1.1, Google 8.8.8.8, Quad9 9.9.9.9, dan GitHub CDN).
* **Cocok untuk:** Diagnostik kualitas koneksi ISP, cek latency jitter, dan deteksi rute peering lambat.
* **[Buka Ping & Latency Tester &rarr;](/tools/ping-tester/)**

---

### 3. ⏱️ [Bandwidth & File Transfer Calculator](/tools/bandwidth-calculator/)
* **Kategori:** *Bandwidth Capacity & QoS Planning*
* **Fungsi:** 
  * Menghitung estimasi durasi transfer unduh/unggah file berdasarkan kapasitas kuota bandwidth (Mbps/Gbps) dalam kondisi teoritis dan kondisi nyata (*80% real-world efficiency*).
  * **MikroTik Simple Queue Burst Assistant:** Menghitung nilai rekomendasi *Burst Limit* (1.5x) dan *Burst Threshold* (0.75x) untuk konfigurasi QoS RouterOS.
* **[Buka Bandwidth Calculator &rarr;](/tools/bandwidth-calculator/)**

---

### 4. 🏷️ [MAC Address Converter & IPv6 EUI-64 Generator](/tools/mac-formatter/)
* **Kategori:** *Hardware Identification & IPv6 Provisioning*
* **Fungsi:** 
  * Konversi instan format alamat MAC ke format standar vendor: **Linux/Unix** (`aa:bb:cc:dd:ee:ff`), **Cisco** (`aabb.ccdd.eeff`), **Windows** (`aa-bb-cc-dd-ee-ff`), dan **Raw Hex**.
  * Otomatis membuat alamat link-local IPv6 berbasis standar **EUI-64** (`fe80::...`).
  * Deteksi bit transmisi Unicast/Multicast dan administrasi OUI hardware.
* **[Buka MAC Address Converter &rarr;](/tools/mac-formatter/)**

---

### 5. 🔐 [Crypto Hasher & Secret Key Generator](/tools/crypto-hasher/)
* **Kategori:** *Cybersecurity & Cryptography*
* **Fungsi:** 
  * Kalkulasi instan hash SHA-256, SHA-512, SHA-1, dan Base64 encoding.
  * Generator kunci acak 32-byte hex dan password berkekuatan tinggi menggunakan *Cryptographically Secure Pseudorandom Number Generator (CSPRNG)* bawaan browser.
* **Keamanan:** Komputasi hash diproses lokal di memori browser pengguna, aman dari penyadapan jaringan.
* **[Buka Crypto Hasher &rarr;](/tools/crypto-hasher/)**

---

### 6. 📷 [Timemark GPS Camera Web](/tools/timemark/)
* **Kategori:** *Field Operations & Verification*
* **Fungsi:** Pengambilan foto dokumentasi dengan sematan stempel waktu presisi (WIB), alamat lokasi, serta koordinat GPS otomatis untuk kebutuhan verifikasi pekerjaan lapangan.
* **Cocok untuk:** Laporan instalasi teknis, audit perangkat jaringan, dan dokumentasi operasional GA.
* **[Buka Timemark Camera &rarr;](/tools/timemark/)**
