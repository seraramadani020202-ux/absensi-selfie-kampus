# AbsensiKu — Sistem Absensi Selfie 📸

Aplikasi web absensi berbasis selfie + validasi lokasi (geofencing simulasi), dengan tiga peran pengguna: **Mahasiswa**, **Dosen**, dan **Admin**.

🔗 **Demo Live:** akan aktif di `https://<username-kamu>.github.io/<nama-repo>/` setelah di-deploy ke GitHub Pages (lihat langkah di bawah).

## ✨ Fitur

- **Mahasiswa**
  - Absensi selfie dengan validasi radius lokasi kampus
  - Riwayat kehadiran (hadir, alfa, izin)
  - Pengajuan izin / sakit
- **Dosen**
  - Rekap kehadiran mahasiswa per status (hadir, alfa, izin)
- **Admin**
  - Kelola lokasi titik absensi (radius, aktif/nonaktif)
  - Rekap kehadiran seluruh mahasiswa
  - Manajemen pengguna
  - Persetujuan permohonan izin/sakit

## 🛠️ Teknologi

Murni **HTML, CSS, dan JavaScript (vanilla)** — tidak ada proses build, tidak ada dependency npm. Font dan ikon dimuat dari CDN:
- [Google Fonts](https://fonts.google.com/) — Plus Jakarta Sans & DM Mono
- [Tabler Icons](https://tabler.io/icons) (via jsDelivr CDN)

Karena tidak ada proses build, file ini bisa langsung dijalankan di browser atau di-deploy ke GitHub Pages tanpa konfigurasi tambahan.

## 🚀 Cara Menjalankan di Lokal

Cukup buka file `index.html` langsung di browser, **atau** jalankan local server (disarankan agar fitur kamera bekerja optimal):

```bash
# Python 3
python3 -m http.server 8000

# atau Node.js
npx serve .
```

Lalu buka `http://localhost:8000` di browser.

## 🌐 Cara Deploy ke GitHub Pages (seperti demo di atas)

1. Buat repository baru di GitHub, misal `ABSENSIKU-WEB`.
2. Upload/push file `index.html` ini ke branch `main` (pastikan nama filenya **tepat** `index.html`, huruf kecil semua).
3. Buka repo di GitHub → **Settings** → **Pages**.
4. Pada bagian **Build and deployment**:
   - Source: `Deploy from a branch`
   - Branch: `main` / folder `/ (root)`
5. Klik **Save**, tunggu 1–2 menit.
6. Situs akan aktif di:
   ```
   https://<username-kamu>.github.io/<nama-repo>/
   ```

### Lewat terminal (git)

```bash
git init
git add .
git commit -m "Initial commit: AbsensiKu web app"
git branch -M main
git remote add origin https://github.com/<username-kamu>/<nama-repo>.git
git push -u origin main
```

Setelah push, aktifkan GitHub Pages seperti langkah di atas.

## 📷 Catatan Izin Kamera

Karena GitHub Pages menggunakan HTTPS secara otomatis, fitur kamera (`getUserMedia`) akan berjalan normal — browser akan meminta izin akses kamera saat pengguna membuka layar absensi. Jika izin ditolak, aplikasi tetap berjalan dalam mode demo tanpa preview kamera live.

## 📄 Lisensi

Bebas digunakan dan dimodifikasi untuk keperluan pembelajaran maupun pengembangan lebih lanjut.
