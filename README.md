# 🏍️ Surabaya Motorcycle Workshops: Web Scraping & Exploratory Data Analysis (EDA)

Proyek pengumpulan dan analisis data bengkel sepeda motor di wilayah Surabaya menggunakan **Python, Web Scraping, Pandas, dan Statistika Deskriptif**. Data dikumpulkan dari dua situs web referensi, yaitu Autofun dan Jejak Piknik, untuk menyusun direktori bengkel yang mencakup informasi nama, alamat, kontak, rating, jumlah ulasan, dan komentar pengguna sesuai ketersediaan data pada masing-masing sumber.

## 📌 Latar Belakang

Informasi mengenai bengkel sepeda motor sering tersebar di berbagai platform digital dengan format yang berbeda-beda. Kondisi ini membuat proses pengumpulan dan perbandingan informasi bengkel menjadi kurang praktis apabila dilakukan secara manual.

Proyek ini memanfaatkan teknik *web scraping* untuk mengumpulkan informasi bengkel secara terstruktur, dilanjutkan dengan proses pembersihan data dan Exploratory Data Analysis (EDA) menggunakan Python.

## 🎯 Tujuan Proyek

1. **Pengumpulan Data:** Mengotomatisasi ekstraksi informasi bengkel sepeda motor dari situs Autofun dan Jejak Piknik.
2. **Data Cleaning:** Membersihkan dan merapikan data hasil ekstraksi agar lebih terstruktur dan siap dianalisis.
3. **Data Transformation:** Mengubah data mentah menjadi tabel menggunakan Pandas DataFrame.
4. **Exploratory Data Analysis:** Menganalisis karakteristik data melalui statistika deskriptif, termasuk rating dan jumlah ulasan bengkel.

## 🛠️ Teknologi dan Tools

| Teknologi | Kegunaan |
|---|---|
| Python | Bahasa pemrograman utama |
| Requests | Mengirim HTTP request untuk mengambil halaman web |
| BeautifulSoup4 | Melakukan parsing HTML dan mengekstrak informasi |
| Pandas | Membersihkan, mengolah, dan menyusun data |
| Jupyter Notebook | Lingkungan pengembangan dan dokumentasi analisis |

## 🔄 Alur Pengerjaan

### 1. Web Scraping

**Sumber 1 — Autofun**

Mengumpulkan data dari direktori bengkel di wilayah Surabaya, meliputi:
- Nama bengkel
- Alamat
- Nomor telepon
- Rating
- Jumlah ulasan (*review*)
- Komentar pengguna

**Sumber 2 — Jejak Piknik**

Mengumpulkan data tambahan dari artikel atau direktori rekomendasi bengkel di Surabaya, meliputi:
- Nama bengkel
- Alamat
- Nomor telepon
- Ulasan atau deskripsi bengkel

Informasi yang berhasil diekstrak bergantung pada ketersediaan data di masing-masing situs.

### 2. Data Cleaning dan Transformasi

Data hasil scraping diproses untuk meningkatkan konsistensi dan keterbacaan sebelum dianalisis. Tahapan yang dilakukan meliputi:

- Membersihkan karakter teks yang tidak diperlukan.
- Merapikan format nomor telepon dan ulasan.
- Menyusun hasil ekstraksi ke dalam struktur tabel.
- Mengonversi data menjadi Pandas DataFrame.

### 3. Exploratory Data Analysis (EDA)

Analisis dilakukan menggunakan fungsi `.describe()` pada variabel numerik yang relevan, khususnya rating dan jumlah ulasan bengkel.

Parameter statistik yang dianalisis meliputi:

| Parameter | Keterangan |
|---|---|
| Count | Jumlah data numerik yang valid |
| Mean | Nilai rata-rata |
| Std | Simpangan baku untuk menggambarkan persebaran data |
| Min | Nilai minimum |
| 25% | Kuartil pertama |
| 50% | Median atau kuartil kedua |
| 75% | Kuartil ketiga |
| Max | Nilai maksimum |

Analisis ini memberikan gambaran awal mengenai karakteristik rating dan jumlah ulasan bengkel berdasarkan data yang berhasil dikumpulkan.

## 📊 Hasil Analisis

### Dataset 1 — Autofun

| Indikator | Hasil |
|---|---:|
| Jumlah bengkel | 9 |
| Rata-rata rating | 4,51 dari 5,00 |
| Rata-rata jumlah ulasan | 299,3 ulasan per bengkel |

Dataset Autofun memuat informasi bengkel di Surabaya beserta rating dan jumlah ulasan yang tersedia. Berdasarkan hasil pengolahan, rata-rata rating bengkel dalam dataset adalah **4,51/5,00**, dengan rata-rata sekitar **299,3 ulasan per bengkel**.

### Dataset 2 — Jejak Piknik

| Indikator | Hasil |
|---|---|
| Jumlah data direktori | 14 bengkel |
| Cakupan informasi | Nama, alamat, nomor kontak, dan deskripsi yang tersedia |
| Jenis bengkel | Bengkel resmi AHASS, bengkel press velg, restorasi, dan modifikasi |

Dataset Jejak Piknik melengkapi direktori bengkel dengan berbagai jenis layanan dan spesialisasi. Kelengkapan informasi setiap bengkel mengikuti data yang tersedia pada sumber referensi.

**Catatan:** Kedua dataset berasal dari sumber berbeda. Jumlah data tersebut tidak otomatis menunjukkan jumlah bengkel unik karena potensi duplikasi antar-sumber belum dapat dipastikan tanpa pemeriksaan lebih lanjut.

## 📁 Struktur Repository

```text
surabaya-motorcycle-workshops-scraper-eda/
├── Hasil Coding.pdf/
│   └── File  code hasil scraping
├── Code.ipynb/
│   └── Code utama untuk scraping dan EDA
├── README.md

```

## 🚀 Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/<username>/surabaya-motorcycle-workshops-scraper-eda.git
cd surabaya-motorcycle-workshops-scraper-eda
```

Ganti `<username>` dengan nama akun GitHub pemilik repository.

### 2. Instal Dependencies

Pastikan Python sudah terinstal, kemudian jalankan:

```bash
pip install -r requirements.txt
```

Jika file `requirements.txt` belum tersedia atau belum berisi daftar pustaka, gunakan:

```bash
pip install pandas requests beautifulsoup4
```

### 3. Jalankan Jupyter Notebook

Buka folder proyek melalui VS Code atau JupyterLab, kemudian jalankan notebook di dalam folder `notebook/` secara berurutan mulai dari proses scraping hingga analisis statistik.

Pastikan koneksi internet tersedia saat mengambil data dari situs web sumber. Struktur halaman web dapat berubah sehingga proses scraping mungkin memerlukan penyesuaian.

## 📦 Dependencies

Contoh isi file `requirements.txt`:

```text
pandas
requests
beautifulsoup4
```

## ⚠️ Catatan Penggunaan

- Proyek ini menggunakan informasi yang tersedia secara publik pada situs referensi.
- Pengambilan data perlu memperhatikan ketentuan penggunaan situs, kebijakan akses otomatis, dan pembatasan permintaan.
- Informasi kontak dan ulasan dapat berubah sewaktu-waktu sehingga perlu diverifikasi kembali jika digunakan untuk keperluan operasional.
- Hasil analisis merepresentasikan dataset yang dikumpulkan dan tidak otomatis mewakili seluruh bengkel sepeda motor di Surabaya.

## 👩‍💻 Ringkasan Proyek

Proyek ini menunjukkan penerapan proses pengolahan data dari tahap pengumpulan hingga analisis awal, dengan mengintegrasikan teknik web scraping, data cleaning, transformasi data, dan statistika deskriptif menggunakan Python.

**Fokus utama:** Web Scraping · Data Collection · Data Cleaning · Pandas · Exploratory Data Analysis · Descriptive Statistics
