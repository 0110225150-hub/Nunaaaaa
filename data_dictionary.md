# Data Dictionary - [Student Career Success]

Dokumen ini berisi informasi dan deskripsi lengkap mengenai struktur data, tabel, serta kolom (field) yang digunakan dalam proyek ini.

## Daftar Isi
- [Tabel: Users](#tabel-users)
- [Tabel: Orders](#tabel-orders)


## Tabel: Orders
Menyimpan informasi transaksi pembelian yang dilakukan oleh pengguna.

| Nama Kolom | Tipe Data | Nullable | Deskripsi | Kategori Data Pribadi | Tindakan Penangan |
| :--- | :--- | :---: | :---: | :--- | :--- |
| `Student_ID` | Object | No | ID unik pengenal mahasiswa | Identitas Langsung (Direct Identifier) | Pseudonimisasi / Anonimisasi / Hapus sebelum pemodelan |
| Age | INT | No | Usia mahasiswa (tahun) | Data Pribadi Umum (Quasi-identifier) | Pertahankan / Kelompokkan dalam rentang usia |
| Gender | STRING | No | Jenis kelamin (Male, Female, Other) | Data Pribadi Umum (Sensitif) | Pertahankan / Agregasi jika ada risiko diskriminasi |
| University_Year | STRING | No | Tingkat studi (Freshman, Sophomore, Junior, Senior) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| Major | STRING | No | Program studi / Jurusan mahasiswa | Non-Pribadi / Akademik | Tidak ada tindakan khusus |

---
*Keterangan Kunci: PK = Primary Key, FK = Foreign Key, UK = Unique Key*
