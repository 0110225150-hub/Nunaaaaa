
# DATA DICTIONARY
## Dataset: Retail Store Sales

## 1. Informasi Dataset

| Informasi | Keterangan |
|---|---|
| Nama Dataset | Retail Store Sales |
| Nama File | retail_store_sales.csv |
| Sumber Dataset | Kaggle |
| URL Dataset Kaggle| [Kaggle](https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning/data) |
| Jumlah Baris | 12.575 |
| Jumlah Kolom | 11 |
| Periode Data | 1 Januari 2022 – 18 Januari 2025 |
| Jenis Data | Numerik dan Kategorikal |

## 2. Deskripsi Variabel

| No. | Nama Variabel | Tipe Data | Satuan | Deskripsi | Sumber |
|---|---|---|---|---|---|
| 1 | Transaction ID | Object | ID transaksi | Kode unik yang digunakan untuk membedakan setiap transaksi penjualan. | Dataset Kaggle |
| 2 | Customer ID | Object | ID pelanggan | Kode identitas yang digunakan untuk membedakan pelanggan dalam data transaksi. | Dataset Kaggle |
| 3 | Category | Object | Kategori | Menunjukkan kelompok atau jenis produk yang dibeli pelanggan. | Dataset Kaggle |
| 4 | Item | Object | Nama produk | Menunjukkan nama barang yang tercatat dalam transaksi penjualan. | Dataset Kaggle |
| 5 | Price Per Unit | Float | Satuan mata uang belum dicantumkan | Menunjukkan harga untuk setiap satu unit produk. | Dataset Kaggle |
| 6 | Quantity | Float | Unit/barang | Menunjukkan jumlah produk yang dibeli dalam satu transaksi. | Dataset Kaggle |
| 7 | Total Spent | Float | Satuan mata uang belum dicantumkan | Menunjukkan total biaya yang dikeluarkan dalam suatu transaksi. | Dataset Kaggle |
| 8 | Payment Method | Object | Kategori | Menunjukkan metode pembayaran yang digunakan pelanggan. | Dataset Kaggle |
| 9 | Location | Object | Kategori | Menunjukkan lokasi atau jenis transaksi, yaitu Online atau In-store. | Dataset Kaggle |
| 10 | Transaction Date | Object | Tanggal (YYYY-MM-DD) | Menunjukkan tanggal ketika transaksi penjualan dilakukan. | Dataset Kaggle |
| 11 | Discount Applied | Object | Boolean (True/False) | Menunjukkan apakah diskon diterapkan pada transaksi. | Dataset Kaggle |

## 3. Klasifikasi Data Pribadi

| No. | Nama Variabel | Kategori Data | Tindakan Penanganan |
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

## 4. Catatan Dataset

1. Dataset terdiri dari 12.575 baris dan 11 kolom.
2. Beberapa variabel memiliki nilai kosong (missing values), terutama pada kolom Discount Applied.
3. Kolom Transaction Date masih tersimpan dalam tipe data object dan dapat dikonversi menjadi datetime pada tahap pengolahan data.
4. Kolom Quantity tersimpan sebagai float, meskipun nilai yang diamati berupa bilangan bulat.
5. Satuan mata uang pada Price Per Unit dan Total Spent belum dicantumkan secara eksplisit dalam dataset.
6. Penanganan data pribadi perlu dilakukan sebelum dataset dipublikasikan ke repositori yang dapat diakses umum.

