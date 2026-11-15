# Cleaning Log

**Tim:** Nunaaaaa

**Dataset:** retail_store_sales.csv (data sintetis), 12.575 baris × 11 kolom

**Terakhir diperbarui:** 15 November 2026

Catatan: ini rencana dari diagnosis di 01_quality.ipynb. Kolom "Baris terdampak" dan hasil sebelum–sesudah diisi di M2 setelah pembersihan dijalankan.

## Urutan langkah

| # | Langkah | Kolom | Baris terdampak | Keputusan | Alasan |
|---|---|---|---|---|---|
| 1 | Perbaiki tipe data | Transaction Date, Discount Applied, Quantity | 12.575 / 8.376 / 11.971 | datetime (%Y-%m-%d), boolean, Int64 | Tanggal masih teks sehingga tak bisa diagregasi per bulan; Quantity desimal hanya karena ada nilai kosong, semua nilainya bulat |
| 2–4 | Spasi, placeholder, seragamkan kategori | semua kolom teks | 0 | Tidak ada tindakan | Jumlah unik sebelum dan sesudah dirapikan sama |
| 5 | Tangani duplikat | semua | 0 | Tidak ada tindakan | Tidak ada duplikat baris maupun Transaction ID |
| 6 | Nilai mustahil | Price, Quantity, Total | 0 | Tidak ada tindakan | Tidak ada nilai ≤ 0; Total = Price × Quantity cocok di 11.362 baris lengkap |
| 7a | Nilai kosong | Price Per Unit | 609 | Hitung dari Total ÷ Quantity | Hubungan itu terbukti valid di semua baris lengkap |
| 7b | Nilai kosong | Item | 1.213 | Pulihkan dari Category + Price (setelah 7a) | Kombinasi Category + Price unik untuk 200 dari 200 item |
| 7c | Nilai kosong | Quantity, Total Spent | 604 | Biarkan kosong, tandai baris | Hilang bersamaan, tidak bisa dihitung dari kolom lain; mengarang nilai menyesatkan |
| 7d | Nilai kosong | Discount Applied | 4.199 | Kategori "Tidak diketahui" | Kosong tampak acak (uji Mann-Whitney p > 0,05); tidak boleh diasumsikan False |

## Yang sengaja TIDAK diubah

| Masalah | Mengapa dibiarkan | Akibat bagi analisis |
|---|---|---|
| Quantity dan Total kosong (604 baris) | Tidak bisa dipulihkan tanpa mengarang | Baris ini dikeluarkan dari hitungan jumlah dan pendapatan |

## Pertanyaan yang belum terjawab

- [ ] Apakah data sintetis diterima dosen untuk M1–M5?
- [ ] Mengapa Price dan Item selalu kosong bersamaan (609 baris)? Perlu dicek ke sumber dataset.
- [ ] Apakah baris dengan Quantity dan Total kosong boleh dikeluarkan dari analisis pendapatan?
