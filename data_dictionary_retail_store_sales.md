# Kamus Data (Data Dictionary)

## Dataset: Retail Store Sales

### 1. Informasi Dataset

  -----------------------------------------------------------------------
  Informasi                           Keterangan
  ----------------------------------- -----------------------------------
  Nama dataset                        `retail_store_sales.csv`

  Jumlah baris                        12.575

  Jumlah kolom                        11

  Rentang tanggal transaksi           2022-01-01 sampai 2025-01-18

  Format file sumber                  CSV (`.csv`)

  Sumber dataset                      Belum dicantumkan di dalam file
                                      CSV; perlu dilengkapi dari sumber
                                      asli

  Lisensi                             Tidak tercantum di dalam file CSV;
                                      perlu diperiksa dari sumber asli
  -----------------------------------------------------------------------

### 2. Deskripsi Kolom

  --------------------------------------------------------------------------------------------------------
             No. Nama Kolom           Tipe Data pada CSV   Deskripsi         Satuan /          Jumlah Data
                                                                             Format                 Kosong
  -------------- -------------------- -------------------- ----------------- -------------- --------------
               1 `Transaction ID`     Object (teks)        Identitas unik    Kode/ID                     0
                                                           untuk setiap      transaksi      
                                                           transaksi                        
                                                           penjualan.                       

               2 `Customer ID`        Object (teks)        Identitas         Kode/ID                     0
                                                           pelanggan yang    pelanggan      
                                                           melakukan                        
                                                           transaksi.                       

               3 `Category`           Object (kategori)    Kategori produk   Kategori                    0
                                                           yang dibeli       produk         
                                                           pelanggan.                       

               4 `Item`               Object               Nama barang atau  Nama produk             1.213
                                      (teks/kategori)      produk yang                      
                                                           dibeli.                          

               5 `Price Per Unit`     Float64 (numerik)    Harga untuk satu  Mata uang                 609
                                                           unit barang.      tidak          
                                                                             disebutkan di  
                                                                             dataset        

               6 `Quantity`           Float64 (numerik)    Jumlah unit       Unit/barang               604
                                                           barang yang                      
                                                           dibeli dalam                     
                                                           transaksi. Nilai                 
                                                           yang teramati                    
                                                           berupa bilangan                  
                                                           bulat 1--10.                     

               7 `Total Spent`        Float64 (numerik)    Total nilai       Mata uang                 604
                                                           pengeluaran untuk tidak          
                                                           transaksi/baris   disebutkan di  
                                                           tersebut.         dataset        

               8 `Payment Method`     Object (kategori)    Metode pembayaran Jenis metode                0
                                                           yang digunakan    pembayaran     
                                                           pelanggan.                       

               9 `Location`           Object (kategori)    Kanal atau lokasi Online /                    0
                                                           transaksi         In-store       
                                                           dilakukan.                       

              10 `Transaction Date`   Object (teks         Tanggal ketika    Format                      0
                                      tanggal)             transaksi         `YYYY-MM-DD`   
                                                           dilakukan.                       

              11 `Discount Applied`   Object               Informasi apakah  True / False            4.199
                                      (kategori/boolean)   diskon diterapkan                
                                                           pada transaksi.                  
  --------------------------------------------------------------------------------------------------------

### 3. Nilai Kategori yang Teramati

**`Category`** - Patisserie - Milk Products - Butchers - Beverages -
Food - Furniture - Electric household essentials - Computers and
electric accessories

**`Payment Method`** - Digital Wallet - Credit Card - Cash

**`Location`** - Online - In-store

**`Discount Applied`** - True - False - Kosong (missing value)

### 4. Ringkasan Pemeriksaan Data

  -----------------------------------------------------------------------
  Kolom                               Informasi
  ----------------------------------- -----------------------------------
  `Price Per Unit`                    Nilai teramati berkisar 5 sampai
                                      41.

  `Quantity`                          Nilai teramati berkisar 1 sampai
                                      10; tersimpan sebagai float pada
                                      CSV.

  `Total Spent`                       Nilai teramati berkisar 5 sampai
                                      410.

  `Transaction Date`                  Tanggal paling awal 2022-01-01 dan
                                      paling akhir 2025-01-18.

  `Discount Applied`                  Memiliki 4.199 nilai kosong. Nilai
                                      kosong tidak otomatis dianggap
                                      `False`; perlu ditentukan
                                      berdasarkan konteks dataset.
  -----------------------------------------------------------------------

### 5. Catatan

1.  Tipe data di atas menggambarkan tipe yang terbaca saat CSV dimuat
    menggunakan pandas. Tipe data dapat berubah setelah proses
    pembersihan, misalnya `Transaction Date` dapat dikonversi menjadi
    tipe datetime.
2.  Mata uang untuk `Price Per Unit` dan `Total Spent` tidak dijelaskan
    di dalam file, sehingga tidak boleh diasumsikan sebagai Rupiah atau
    mata uang tertentu sebelum sumber dataset dikonfirmasi.
3.  Nilai kosong pada `Item`, `Price Per Unit`, `Quantity`,
    `Total Spent`, dan `Discount Applied` perlu ditinjau pada tahap data
    quality/cleaning. Jangan mengisi atau menghapusnya tanpa alasan yang
    dicatat.
4.  `Customer ID` merupakan pengenal pelanggan. Perhatikan ketentuan
    privasi dan lisensi sebelum membagikan dataset ke repositori publik.
5.  Lengkapi bagian sumber dataset dan lisensi berdasarkan halaman
    tempat dataset asli diperoleh.

------------------------------------------------------------------------

*Kamus data ini menjelaskan arti dan karakteristik setiap kolom pada
dataset. Perubahan yang dilakukan terhadap data selama proses
pembersihan dicatat secara terpisah di `cleaning_log.md`.*
