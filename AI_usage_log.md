# AI Usage Log

Wajib diisi sesuai kebijakan mata kuliah. Catat **setiap** penggunaan AI generatif selama proyek berlangsung, termasuk yang hasilnya akhirnya tidak dipakai.

Tiga hal yang perlu diingat:

1. AI **boleh** dipakai untuk membantu menulis dan men-debug kode, mencari referensi fungsi, serta memperbaiki bahasa laporan.  
2. Setiap angka, grafik, dan klaim **wajib dapat direproduksi dari kode tim**. Kesalahan yang berasal dari keluaran AI tetap menjadi tanggung jawab tim.  
3. AI **tidak boleh** dipakai saat kuis, tes UTS, dan oral defense.

---

| \# | Tanggal | Anggota | Alat | Tujuan | Prompt utama (ringkas) | Bagian yang dihasilkan / diubah | Diverifikasi? |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | 14/11/2026 | Salma Haniya | Claude AI | Merapikan dan fiksasi notebook M1-M2 | “Periksa file M1 (diagnosis) dan M2 (cleaning) yang udah setengah dikerjakan apakah kolom sudah sesuai dengan perintahnya, lalu koreksi dan lanjutkan workbook ini” | Koreksian seluruh file notebook M1 dan M2 | Ya – Kode sudah sesuai dengan dataset dan template, namun masih ada beberapa penyesuaian pada implementasinya. |
| 2 | 15/11/2026 | Salma Haniya | Claude AI | Debug Error NotDefined | “Kenapa bisa error” (beserta tangkapan layar) | Menambahkan fungsi catat (def catat) sebelum tahapan 1 dimulai. | Ya – fungsi catat berfungsi dan berhasil mencatat seluruh tahapan untuk digunakan pada cleaning log. |
| 3 |  |  |  |  |  |  |  |

---

## Contoh pengisian

| \# | Tanggal | Anggota | Alat | Tujuan | Prompt utama (ringkas) | Bagian yang dihasilkan / diubah | Diverifikasi? |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | 12/10/2026 | Bima | ChatGPT | Mencari cara menangani galat saat konversi tanggal | "pandas to\_datetime format hari bulan tahun" | Sel 4 pada `02_cleaning.ipynb` | Ya — hasil dibandingkan dengan konversi manual pada 20 baris contoh |
| 2 | 15/10/2026 | Rani | Claude | Memperbaiki susunan kalimat bagian keterbatasan | "perbaiki bahasa paragraf berikut tanpa mengubah isinya" | Bagian 7 laporan | Ya — isi dan angkanya tidak berubah |

## Verifikasi

Kolom terakhir bukan formalitas. Tuliskan **bagaimana** Anda memverifikasinya, bukan sekadar "ya". Keluaran AI yang dipakai tanpa diperiksa adalah risiko terbesar terhadap dimensi *ketepatan implementasi* dan *reproduktibilitas*.