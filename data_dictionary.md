# Data Dictionary - [Student Career Success]

Dokumen ini berisi informasi dan deskripsi lengkap mengenai struktur data, tabel, serta kolom (field) yang digunakan dalam proyek ini.

## Daftar Isi
- [Tabel: Users](#tabel-users)
- [Tabel: Orders](#tabel-orders)


## Tabel: Orders
Menyimpan informasi transaksi pembelian yang dilakukan oleh pengguna.

| Nama Kolom | Tipe Data | Nullable | Kunci (Key) | Deskripsi | Kategori Data Pribadi |
| :--- | :--- | :---: | :---: | :--- | :--- |
| `Student_ID` | Object | No | PK | ID unik pengenal mahasiswa | Identitas Langsung (Direct Identifier) |
| `user_id` | INT | No | FK | Menghubungkan ke `id` di tabel `users` | `1` |
| `total_price` | DECIMAL(10,2)| No | - | Total harga pesanan | `150000.00` |
| `status` | ENUM | No | - | Status pesanan: `PENDING`, `PAID`, `SHIPPED`, `CANCELLED` | `PAID` |
| `ordered_at` | TIMESTAMP | No | - | Waktu saat pesanan dibuat | `2026-10-05 09:00:00` |

---
*Keterangan Kunci: PK = Primary Key, FK = Foreign Key, UK = Unique Key*
