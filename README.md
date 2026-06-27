# Monitoring SE2026

Monitoring SE2026 adalah aplikasi dasbor (dashboard) berbasis web yang dirancang khusus untuk **Monitoring Progres Pendataan Lapangan Sensus Ekonomi 2026 (SE2026)**. Aplikasi ini memberikan visualisasi data secara _real-time_ untuk memantau kinerja Petugas Pendataan Lapangan (PPL) dan Pengawas Menengah Lapangan (PML).

## ✨ Fitur Utama

- **Pembaruan Data Otomatis:** Mengambil data langsung secara dinamis (client-side fetching) dari Google Sheets tanpa memerlukan backend atau database server tambahan.
- **Peringkat Produktivitas (Leaderboard):** Menampilkan daftar petugas terproduktif berdasarkan rata-rata akumulasi data harian.
- **Visualisasi Progres Harian:** Menampilkan grafik tren data submit dan draf per hari untuk memantau fluktuasi kinerja lapangan.
- **Pelacak Target:** Membandingkan perolehan data _Submit_ dan _Draf_ dengan beban _Target_ (Muatan Prelist) secara otomatis.
- **Sistem Apresiasi:** Menyoroti petugas yang paling aktif memberikan kontribusi (Bintang Progres).
- **Desain Modern & Responsif:** Dibangun menggunakan antarmuka modern yang nyaman dilihat di layar komputer maupun perangkat seluler.

## 🚀 Teknologi yang Digunakan

Aplikasi ini dibangun menggunakan arsitektur frontend modern:
- **[React](https://react.dev/) & [Vite](https://vitejs.dev/):** Kerangka kerja dan _build tool_ utama yang super cepat.
- **[Tailwind CSS](https://tailwindcss.com/):** Sistem styling berbasis utilitas untuk desain antarmuka yang dinamis.
- **[Recharts](https://recharts.org/):** Library untuk pembuatan grafik dan visualisasi data yang interaktif.
- **[Lucide React](https://lucide.dev/):** Koleksi ikon yang konsisten dan elegan.
- **Google Sheets API (gviz):** Sebagai _headless CMS_ / sumber data utama (No-SQL approach).

## 🛠️ Cara Menjalankan di Komputer Lokal (Localhost)

Ikuti langkah-langkah berikut untuk menjalankan aplikasi ini di komputer Anda sendiri:

**Prasyarat:** Pastikan Anda telah menginstal [Node.js](https://nodejs.org/).

1. **Clone repositori ini (atau unduh kodenya)**
   ```bash
   git clone https://github.com/ahmadrahman79/Prasasti-SE2026.git
   cd Prasasti-SE2026
   ```

2. **Instal dependensi library**
   ```bash
   npm install
   ```

3. **Jalankan server lokal (Development)**
   ```bash
   npm run dev
   ```
   Aplikasi akan berjalan di `http://localhost:3000/` (atau port lain yang tertera di terminal).

## 🌍 Cara Mengubah Sumber Data (Google Sheets)

Sumber data aplikasi ini terhubung ke sebuah Google Sheet secara terbuka. Jika Anda ingin mengganti sumber datanya:
1. Buat Google Sheet Anda sendiri dengan format kolom yang persis sama.
2. Pastikan setelan "Bagikan" (Share) Google Sheet Anda diatur ke **"Siapa saja yang memiliki link" (Pelihat)**.
3. Ambil **ID Spreadsheet** Anda (karakter acak panjang di dalam URL Google Sheet).
4. Buka file `src/App.tsx`, cari konstanta `DEFAULT_SPREADSHEET_ID`, dan ganti dengan ID Anda.

## 📝 Catatan Rilis
- Integrasi parsing CSV yang kuat untuk mencegah pergeseran kolom saat terdapat karakter koma di dalam nama/teks.
- Dideploy melalui [Vercel](https://vercel.com/) untuk pembaruan berkelanjutan tanpa batas.

---
*Dibuat untuk kelancaran Sensus Ekonomi 2026.*
