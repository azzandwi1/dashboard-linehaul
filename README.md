# 🗺️ SAPX Line Haul Network Dashboard

Visualisasi interaktif peta rute jaringan **Line Haul (Middle Mile)** SAP Express seluruh Indonesia. 

Dashboard ini menampilkan visualisasi rute berbasis Leaflet.js dengan penarikan data secara **Live** langsung dari Google Sheets.

## 🚀 Fitur Utama
- **Live Data Integration**: Menarik data rute aktual secara langsung dari Google Sheets *DATA ALL* (tanpa cache/proxy).
- **Rich Hub Metadata**: Klik marker Hub pada peta untuk melihat detail PIC Cabang, Kontak WhatsApp, Alamat Lengkap, dan tautan navigasi Google Maps.
- **Interactive Geotargeting Filters**:
  - Filter rute & hub berdasarkan **Region Geografis** (Sumatera, Jawa, Kalimantan, dll).
  - Filter interaktif dengan mengklik Hub di peta atau daftar hub untuk memunculkan rute yang terhubung langsung saja.
- **Auto-Fallbacks**: Tetap berjalan lancar menggunakan basis data lokal offline jika koneksi internet terputus.

## 💻 Cara Menjalankan Secara Lokal
Untuk menghindari kebijakan keamanan browser (CORS) saat memuat data live, jalankan proyek ini menggunakan web server lokal:

1. Buka terminal/Command Prompt di folder ini.
2. Jalankan perintah server bawaan Python:
   ```bash
   python -m http.server 8765
   ```
3. Buka browser Anda dan akses:
   👉 **[http://localhost:8765](http://localhost:8765)**

## 🛠️ Cara Merakit (Build)
Jika berkas koordinat, PIC Cabang, atau script utama diperbarui, lakukan kompilasi ulang berkas `index.html` dengan menjalankan:
```bash
python build_dashboard.py
```
*(Script ini otomatis menggabungkan seluruh database koordinat presisi dan kontak PIC Excel ke dalam satu halaman web statis).*
