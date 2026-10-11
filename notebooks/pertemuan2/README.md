1.  Berapa baris dan kolom? Apa satuan tiap barisnya (satu baris = satu apa)?
    - Total data di dataset ini memiliki 50.000 baris dan 29 kolom.
    - Satuan tiap baris: 1 baris = 1 data profil/rekam jejak akademis dan karir seorang mahasiswa (diidentifikasi oleh Student_ID).

2. Kolom mana yang numerik, kategorikal, dan tanggal?
   - Numerik (16 Kolom):age, Attendance_Percentage, Study_Hours_Per_Week, CGPA, Programming_Skill, Projects_Completed, Certifications, Hackathons, Internships, Resume_Score, Communication_Skills, Teamwork, Problem_Solving, Interview_Score, Employability_Score, Starting_Salary_USD
   - Kategorikal (13 Kolom): Student_ID, Gender, University_Year, Major, Academic_Performance, GitHub_Profile, Leadership_Experience, LinkedIn_Profile, English_Proficiency, Placement_Status, Company_Tier, Career_Field, Placement_Mode
   - Tanggal: Tidak ada kolom bertipe tanggal/waktu dalam dataset  ini.

3. Kolom mana yang bermasalah (kosong, tipe salah, nilai tidak konsisten)?
   - Data Kosong: Tidak ada
   - Tipe Data Salah: tidak ada yang salah secara teknis, namun kolom kategorikal biner seberti GITHUB_Profile, Leadership_Experience, dan Linkedln_Profile bernilai teks ("Yes"/"No") sehingga perlu diubah menjadi biner (0/1) saat tahap preprocessing/modelling.
   - Nilai Tidak Konsisten:
     - Data ini bersifat buatan (synthetic) sehingga distribusinya rapi tanpa outlier ekstrem atau sesuai dengan logika bisnis.
     - Kolom Starting_Salary_USD untuk mahasiswa dengan status Nol Placed diisi angka 0, sehingga sudah sesuai dengan logika bisnis.

4. Apakah data ini cukup untuk menjawab pertanyaan analisi tim? Jika belum, apa yang kurang?
   - Sudah cukup, terutama untuk kebutuhan:
     - Memprediksi status penerimaan kerja mahasiswa (Placement_Status).
     - Melihat pengaruh faktor akademis dan soft skill terhadap gaji awal (Starting_Salary_USD).
     - Memprediksi tingkatan perusahaan (Company_Tier) penerima.
       
    - Beberapa keterbatasan data yang perlu diperhatikan:
      - Tidak ada data waktu/tahun: Tanpa adanya tahun kelulusan, tren antar-periode tidak bisa dianalisis.
      - Tidak ada informasi lokasi: Lokasi kampus maupun area kerja tifak tercantum.
      - Sifat daya buatan: Sebagai synthetic data, pola antar-variabel bisa jadi terlalu ideal dibanding lokasi kondisi lapangan.
     

**NAMA ANGGOTA**
- Salma Haniya Rahma 0110225150
- Trisa Dhiya Nasywa 0110225049
- Indah Nurul Hasibuan 0110225121
- Labibah Nurrahmah 0110225176
