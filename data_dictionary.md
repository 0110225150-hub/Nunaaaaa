# Data Dictionary - [Student Career Success]

Dokumen ini berisi informasi dan deskripsi lengkap mengenai struktur data, tabel, serta kolom (field) yang digunakan dalam proyek ini.

## Daftar Isi
- [Tabel: Users](#tabel-users)
- [Tabel: Orders](#tabel-orders)

---

## Tabel: Users
Menyimpan informasi data pengguna/akun aplikasi.

| Nama Kolom | Tipe Data | Nullable | Kunci (Key) | Deskripsi | Kategori data pribadi | tindakan penanganan
| :--- | :--- | :---: | :---: | :--- | :--- |
| `Student_ID` | Object | No | PK | ID unik untuk setiap pengguna (Auto Increment) | Identitas Langsung (Direct Identifier) | Pseudonimisasi / Anonimisasi / Hapus sebelum pemodelan |
| `Age` | INT | No | UK | Usia mahasiswa (tahun) | Data Pribadi Umum (Quasi-identifier) | Pertahankan / Kelompokkan dalam rentang usia |
| `Gender` | VARCHAR(100) | No | UK | Jenis kelamin (Male, Female, Other) | Data Pribadi Umum (Sensitif) | Pertahankan / Agregasi jika ada risiko diskriminasi |
| `University_Year` | VARCHAR(100) | No | - | Tingkat studi (Freshman, Sophomore, Junior, Senior) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Major` | VARCHAR(100) | No | - | Program studi / Jurusan mahasiswa | Non-Pribadi / Akademik | Tidak ada tindakan khusus
| `Attendance_Percentage` | INT | No | - | Persentase kehadiran kuliah (%) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Study_Hours_Per_Week` | INT | No | - | Jam belajar per minggu | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `CGPA` | Float | No | - | Indeks Prestasi Kumulatif (IPK) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Academic_Performance` | VARCHAR(100) | No | - | Kategori performa akademik (Poor, Average, Good, Excellent) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Programming_Skill` | INT | No | - | Skor tingkat keahlian koding (1-10) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Projects_Completed` | INT | No | - | Kategori performa akademik (Poor, Average, Good, Excellent) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |

---

## Tabel: Orders
Menyimpan informasi transaksi pembelian yang dilakukan oleh pengguna.

| Nama Kolom | Tipe Data | Nullable | Kunci (Key) | Deskripsi | Contoh Nilai |
| :--- | :--- | :---: | :---: | :--- | :--- |
| `id` | INT | No | PK | ID unik untuk setiap pesanan | `10025` |
| `user_id` | INT | No | FK | Menghubungkan ke `id` di tabel `users` | `1` |
| `total_price` | DECIMAL(10,2)| No | - | Total harga pesanan | `150000.00` |
| `status` | ENUM | No | - | Status pesanan: `PENDING`, `PAID`, `SHIPPED`, `CANCELLED` | `PAID` |
| `ordered_at` | TIMESTAMP | No | - | Waktu saat pesanan dibuat | `2026-10-05 09:00:00` |

---
*Keterangan Kunci: PK = Primary Key, FK = Foreign Key, UK = Unique Key*
