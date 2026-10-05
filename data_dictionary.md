# Data Dictionary - [Student Career Success]

Dokumen ini berisi informasi dan deskripsi lengkap mengenai struktur data, tabel, serta kolom (field) yang digunakan dalam proyek ini.

## Daftar Isi
- [Tabel: Users](#tabel-users)
- [Tabel: Orders](#tabel-orders)


## Tabel: Orders
Menyimpan informasi transaksi pembelian yang dilakukan oleh pengguna.

| Nama Kolom | Tipe Data | Deskripsi | Kategori Data Pribadi | Tindakan Penangan |
| :--- | :--- | :---: | :--- | :--- |
| `Student_ID` | Object | ID unik pengenal mahasiswa | Identitas Langsung (Direct Identifier) | Pseudonimisasi / Anonimisasi / Hapus sebelum pemodelan |
| `Age` | INT | Usia mahasiswa (tahun) | Data Pribadi Umum (Quasi-identifier) | Pertahankan / Kelompokkan dalam rentang usia |
| `Gender` | STRING | Jenis kelamin (Male, Female, Other) | Data Pribadi Umum (Sensitif) | Pertahankan / Agregasi jika ada risiko diskriminasi |
| `University_Year` | STRING | Tingkat studi (Freshman, Sophomore, Junior, Senior) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Major` | STRING | Program studi / Jurusan mahasiswa | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Attendance_Percentage` | INT | Persentase kehadiran kuliah (%) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Study_Hours_Per_Week` | INT | Jam belajar per minggu | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `CGPA` | Float | Indeks Prestasi Kumulatif (IPK) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Academic_Performance` | STRING | Kategori performa akademik (Poor, Average, Good, Excellent) | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Programming_Skill` | INT | Skor tingkat keahlian koding (1-10) | Non-Pribadi / Skill | Tidak ada tindakan khusus |
| `Projects_Completed` | INT | Jumlah proyek yang telah diselesaikan | Non-Pribadi / Akademik | Tidak ada tindakan khusus |
| `Certifications` | INT | Jumlah sertifikasi profesional | Non-Pribadi / Skill | Tidak ada tindakan khusus |
| `Hackathons` | INT | Skor tingkat keahlian koding (1-10) | Non-Pribadi / Skill | Tidak ada tindakan khusus |
| `Programming_Skill` | INT | Jumlah keikutsertaan kompetisi hackathon | Non-Pribadi / Skill | Tidak ada tindakan khusus |

---
*Keterangan Kunci: PK = Primary Key, FK = Foreign Key, UK = Unique Key*
