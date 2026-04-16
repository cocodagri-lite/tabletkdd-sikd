# Data TKDD Provinsi Riau 2025

Website statis yang menampilkan data **Transfer ke Daerah dan Dana Desa (TKDD)** Provinsi Riau tahun 2025, bersumber dari [DJPK Kemenkeu](https://djpk.kemenkeu.go.id/).

## Fitur
- Tabel data interaktif dengan pencarian dan sorting
- Ringkasan total anggaran per kolom
- Data diperbarui otomatis setiap hari via GitHub Actions

## Cara Upload ke GitHub

### 1. Buat repo baru di GitHub
- Buka [github.com/new](https://github.com/new)
- Beri nama repo (contoh: `tkdd-riau`)
- Pilih **Public**
- Klik **Create repository**

### 2. Upload file-file ini
Upload semua file berikut ke repo:
```
index.html
data.csv
.github/
  workflows/
    fetch-data.yml
```

### 3. Jalankan GitHub Actions pertama kali (untuk mengisi data.csv)
- Buka tab **Actions** di repo
- Klik workflow **Update Data TKDD**
- Klik **Run workflow** → **Run workflow**
- Tunggu selesai (sekitar 30 detik)

### 4. Aktifkan GitHub Pages
- Buka **Settings** → **Pages**
- Source: pilih **Deploy from a branch**
- Branch: pilih `main` → folder `/` (root)
- Klik **Save**
- Tunggu 1-2 menit, website akan live di:
  `https://<username>.github.io/<nama-repo>/`

## Update Otomatis
GitHub Actions akan otomatis mendownload data terbaru dari DJPK setiap hari jam **08.00 WIB**.

## Sumber Data
[djpk.kemenkeu.go.id](https://djpk.kemenkeu.go.id/portal/data/tkdd?tahun=2025&provinsi=14&pemda=00)
