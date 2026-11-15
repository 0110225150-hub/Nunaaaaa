# [Analisis Pola Penjualan Toko Ritel]

## Deskripsi Proyek
Proyek ini merupakan analisis data eksploratif (Exploratory Data Analysis/EDA) terhadap dataset Retail Store Sales yang bertujuan untuk memahami pola penjualan toko ritel. Analisis dilakukan dengan mengeksplorasi data transaksi berdasarkan kategori produk, jumlah pembelian, total pengeluaran, metode pembayaran, lokasi, dan waktu transaksi. Hasil eksplorasi disajikan melalui visualisasi data untuk menemukan pola, tren, serta insight yang dapat membantu memahami karakteristik penjualan dan perilaku pelanggan.

## Identitas Kelompok:
**Program studi:** Teknik Informatika\
**Mata Kuliah:** Exploratory Data Analyst\
**Semester:** Ganjil 2026/2027

## Anggota:
|Anggota|NIM|Peran Utama|
|----|----|----|
|Labibah Nurrahmah|0110225176|Koordinator|
|Salma Haniya Rahma|0110225150|Data Engineer|
|Trisa Dhiya Nasywa|0110225049|Analis Data|
|Indah Nurul Ayni|0110225121|Penulis|

|Peran|Tanggung Jawab Utama|
|---------|-----------|
|Koordinator|Menjaga jadwal, memimpin rapat tim, mengunggah pengumpulan ke LMS, menjadi penghubung dengan dosen|
|Data Engineer|Akuisisi data, pembersihan, pipeline, menjaga data/raw tetap utuh, menulis cleaning_log.md|
|Analis|Analisis univariat, bivariat, multivariat, pemilihan teknik, pengecekan asumsi|
|Penulis|Kualitas grafik, penyusunan laporan, slide, dan alur cerita temuan|

## Pembagian Peran
|Milestone|Koordinator|Data Engineer|Analis|Penulis|
|---------|-----------|-------------|------|-------|
|M1|Labibah|Salma|Trisa|Nurul|
|M2|Trisa|Salma|Nurul|Labibah|
|M3|Nurul|Trisa|Labibah|Salma|
|M4|Salma|Labibah|Nurul|Trisa|

## Latar Belakang
Data penjualan merupakan informasi penting dalam kegiatan usaha ritel. Melalui data transaksi, dapat diketahui barang yang banyak dibeli, jumlah pembelian, harga, serta pola pengeluaran pelanggan. Namun, data tersebut perlu dieksplorasi agar dapat memberikan gambaran yang lebih jelas mengenai aktivitas penjualan.

Proyek ini menggunakan metode Exploratory Data Analysis (EDA) untuk mengidentifikasi pola dan karakteristik penjualan pada dataset Retail Store Sales. Analisis ini penting untuk memahami kecenderungan transaksi sekaligus menemukan permasalahan kualitas data.

Hasil analisis diharapkan dapat memberikan informasi yang bermanfaat bagi pemilik dan pengelola toko ritel dalam mengevaluasi penjualan serta menjadi bahan pertimbangan dalam pengambilan keputusan bisnis.

## Pertanyaan Analisis
1. Bagaimana distribusi penjualan berdasarkan kategori dan jenis barang (Item)?
2. Bagaimana pola jumlah pembelian dan total pengeluaran di setiap transaksi?
3. Apakah ada perbedaan nilai transaksi berdasarkan kategori barang?
4. Bagaimana hubungan penggunaan diskon dengan jumlah pembelian dan nilai transaksi?

## Tujuan Analisis
- Mengidentifikasi pola dan tren penjualan toko ritel.
- Mengetahui kategori produk dengan penjualan tertinggi.
- Menganalisis perilaku pembelian dan pengeluaran pelanggan.
- Mengidentifikasi metode pembayaran dan lokasi transaksi yang paling banyak digunakan.
- Mengetahui pola penjualan berdasarkan waktu.
- Menghasilkan insight sebagai dasar pengambilan keputusan bisnis.

## Sumber Data
|Keterangan|Informasi|
|----------|---------|
|Nama Dataset|Retail Store Sales|
|Sumber Dataset|Kaggle|
|Ukuran|12.575 baris x 11 kolom|
|Lisensi/Izin|CC BY-SA 4.0|
|Tanggal Unduh|12 November 2026|

Kamus data lengkap: data_dictionary.md 

## Penanganan Data Pribadi
| No. | Kolom | Kategori Data | Tindakan Penanganan |
|---|---|---|---|
| 1 | Transaction ID | Bukan data pribadi | Dipertahankan untuk membedakan transaksi. |
| 2 | Customer ID | Pengenal langsung (identifier pelanggan) | Dilakukan hashing atau pseudonimisasi sebelum data dipublikasikan. |
| 3 | Category | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 4 | Item | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 5 | Price Per Unit | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 6 | Quantity | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 7 | Total Spent | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 8 | Payment Method | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |
| 9 | Location | Bukan data pribadi | Dipertahankan karena hanya menunjukkan kategori lokasi transaksi. |
| 10 | Transaction Date | Quasi-identifier | Dapat digeneralisasi menjadi bulan atau periode jika kombinasi data berisiko mengidentifikasi pelanggan. |
| 11 | Discount Applied | Bukan data pribadi | Dipertahankan untuk keperluan analisis. |

## Struktur Repository
```text
Nunaaaaa/
│
├── dataset/
│   ├── raw/
│   │   └── retail_store_sales.csv
│   │
│   └── processed/
│       └── data_bersih.csv
│
├── notebooks/
│   ├── 01_data_quality.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_univariate_analysis.ipynb
│   ├── 04_multivariate_analysis.ipynb
│   ├── 05_advanced_analysis.ipynb
│   │
│   ├── pertemuan2/
│   │   ├── P02_Praktikum_Labibah_Nurrahmah.ipynb
│   │   ├── P02_Praktikum_Salma.ipynb
│   │   └── P02_Praktikum_Trisa_Dhiya_Nasywa_Colab.ipynb
│   │
│   ├── pertemuan3/
│   │   ├── P03_Praktikum_Pertemuan3_LabibahNurrahmah.ipynb
│   │   ├── P03_Praktikum_Salma.ipynb
│   │   └── P03_Praktikum_TrisaDhiyaNasywa.ipynb
│   │
│   └── pertemuan4/
│       ├── P04_Praktikum_Salma.ipynb
│       ├── P04_Workbook_Mandiri_Labibah_Nurrahmah.ipynb
│       └── P04_Workbook_Mandiri_Trisa.ipynb
│
├── .gitignore
├── AI_usage_log.md
├── README.md
├── cleaning_log.md
└── data_dictionary.md
```
