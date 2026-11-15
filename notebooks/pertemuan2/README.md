1. Berapa baris dan kolom? Apa satuan tiap barisnya?
   - Dataset memiliki 12.575 baris dan 11 kolom.
   - Satuan baris: 1 baris = 1 transaksi penjualan (diidentifikasi oleh Transaction ID).

2. Kolom mana yang numerik, kategorikal, dan tanggal?
   - Numerik (3): Price Per Unit, Quantity, Total Spent.
   - Kategorikal (7): Transaction ID, Customer ID, Category, Item, Payment Method, Location, Discount Applied.
   - Tanggal (1): Transaction Date (saat ini bertipe teks).

3. Kolom mana yang bermasalah?
   - Data kosong: Item 1.213 (9,6%), Price Per Unit 609 (4,8%), Quantity 604 (4,8%), Total Spent 604 (4,8%), Discount Applied 4.199 (33,4%). Sebanyak 4.996 baris memiliki minimal satu nilai kosong.
   - Tipe salah: Transaction Date bertipe teks (seharusnya datetime), Discount Applied bertipe campuran (seharusnya boolean).
   - Nilai tidak konsisten: tidak ditemukan. Tidak ada baris duplikat, penulisan kategori seragam, dan Total Spent = Price Per Unit × Quantity cocok di semua 11.362 baris lengkap.

4. Apakah data cukup untuk menjawab pertanyaan analisis?
   - Cukup untuk analisis deskriptif pola transaksi menurut kategori, metode pembayaran, lokasi, dan waktu.
   - Keterbatasan: data bersifat sintetis, kolom numerik hanya tiga (Total Spent turunan dari dua kolom lain), tidak ada informasi demografi pelanggan, dan data kosong cukup besar sehingga perlu penanganan.
     

**NAMA ANGGOTA**
- Salma Haniya Rahma 0110225150
- Trisa Dhiya Nasywa 0110225049
- Indah Nurul Hasibuan 0110225121
- Labibah Nurrahmah 0110225176
