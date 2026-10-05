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
| `GitHub_Profile` | STRING | Kepemilikan profil GitHub (Yes/No) | Data Pribadi Umum (Profil Publik) | Tidak ada tindakan khusus |
| `Internships` | INT | Jumlah pengalaman magang | Non-Pribadi / Pengalaman | Tidak ada tindakan khusus |
| `Leadership_Experience` | STRING | Pengalaman kepemimpinan (Yes/No) | Non-Pribadi / Pengalaman | Tidak ada tindakan khusus |
| `LinkedIn_Profile` | STRING | Kepemilikan profil LinkedIn (Yes/No) | Data Pribadi Umum (Profil Publik) | Tidak ada tindakan khusus |
| `Resume_Score` | INT | Skor kualitas resume/CV | Non-Pribadi / Evaluasi | Tidak ada tindakan khusus |
| `Communication_Skills` | INT | Skor keterampilan komunikasi (1-10) | Non-Pribadi / Soft Skill | Tidak ada tindakan khusus |
| `Teamwork` | INT | Skor kemampuan pemecahan masalah (1-10) | Non-Pribadi / Soft Skill | Tidak ada tindakan khusus |
| `Problem_Solving` | INT | Skor kemampuan kerja sama tim (1-10) | Non-Pribadi / Soft Skill | Tidak ada tindakan khusus |
| `English_Proficiency` | STRING | Tingkat kemahiran bahasa Inggris (Basic, Intermediate, Advanced) | Non-Pribadi / Soft Skill | Tidak ada tindakan khusus |
| `Interview_Score` | INT | Skor simulasi/hasil wawancara kerja | Non-Pribadi / Evaluasi | Tidak ada tindakan khusus |
| `Employability_Score` | Float | Skor gabungan kesiapan kerja | Non-Pribadi / Evaluasi | Tidak ada tindakan khusus |
| `Placement_Status` | STRING | Status kelulusan/penempatan kerja (Placed / Not Placed) | Non-Pribadi / Karir | Tidak ada tindakan khusus |
| `Company_Tier` | STRING | Kategori tingkat perusahaan (Tier 1, Tier 2, Tier 3, No Company) | Non-Pribadi / Karir | Tidak ada tindakan khusus |
| `Career_Field` | STRING | Bidang/posisi pekerjaan karir | Non-Pribadi / Karir | Tidak ada tindakan khusus |
| `Placement_Mode` | STRING | Jalur penempatan kerja (Campus Placement, Job Portal, dll) | Non-Pribadi / Karir | Tidak ada tindakan khusus |
| `Starting_Salary_USD` | INT | Gaji awal dalam USD | Data Finansial Sensitif (Quasi-identifier) | Pertahankan untuk analisis regresi / Anonimisasi saat dipublikasikan |

---
*Keterangan Kunci: PK = Primary Key, FK = Foreign Key, UK = Unique Key*
