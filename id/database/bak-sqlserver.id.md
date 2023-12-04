{
"tanggal": "12-06-2023",
  "keywords": [
"memanggang",
"membuat file",
"Cadangan Basis Data Microsoft SQL Server",
"apa itu file bak",
"cara membuka file bak",
"mengajukan",
"ekstensi file bak",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File BAK - Cadangan Basis Data Microsoft SQL Server",
  "description":"Pelajari tentang format Cadangan BAK SQL Server dan API yang dapat membuat dan membuka file BAK.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent" : "database"
}
},
"mod terakhir": "12-06-2023"
}

## Apa itu file BAK?

File ".bak", dalam konteks Microsoft SQL Server, adalah format file cadangan yang digunakan untuk menyimpan salinan database SQL Server. File-file ini berisi cuplikan database pada titik waktu tertentu, termasuk skema, data, dan informasi terkait lainnya. Mereka dihasilkan menggunakan fungsionalitas pencadangan dan pemulihan bawaan SQL Server dan melayani beberapa tujuan penting:

1. **Pemulihan Data:** File .bak menyediakan sarana untuk memulihkan database jika terjadi kehilangan data, kerusakan, atau masalah lainnya. Dengan memulihkan database dari file .bak, Anda dapat mengembalikannya ke keadaan sebelumnya, meminimalkan waktu henti dan kehilangan data.

2. **Migrasi dan Kloning:** File cadangan sering kali digunakan untuk memigrasikan database antar server atau membuat salinan database untuk tujuan pengujian, pengembangan, atau pelaporan. Mereka menawarkan cara yang konsisten dan efisien untuk memindahkan database antar lingkungan.

3. **Pemulihan Point-in-Time:** SQL Server memungkinkan Anda melakukan pemulihan point-in-time menggunakan file .bak. Ini berarti Anda dapat memulihkan database ke momen tertentu, yang dapat menjadi sangat penting untuk kepatuhan terhadap peraturan atau audit data.

4. **Pemulihan Bencana:** File .bak adalah bagian penting dari perencanaan pemulihan bencana. Mereka memastikan bahwa data Anda aman dan dapat dipulihkan dengan cepat jika terjadi kegagalan perangkat keras, bencana alam, atau peristiwa bencana lainnya.

## Buat file .BAK di SQL Server

Untuk membuat file .bak di SQL Server, Anda biasanya menggunakan perintah SQL Server Management Studio (SSMS) atau Transact-SQL (T-SQL) seperti BACKUP DATABASE atau BACKUP LOG. Berikut adalah contoh sederhana bagaimana Anda dapat membuat cadangan database menggunakan T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Pulihkan file .BAK di SQL Server

Untuk memulihkan database dari file .bak, Anda dapat menggunakan perintah RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Bagaimana cara membuka file BAK di SQL Server?

Untuk membuka dan mengakses data yang disimpan dalam file ".bak", Anda biasanya perlu memulihkannya ke contoh Microsoft SQL Server. Berikut langkah umum untuk membuka file ".bak" menggunakan SQL Server Management Studio (SSMS):

1. **Luncurkan SQL Server Management Studio**: Buka SSMS di komputer Anda. Anda biasanya dapat menemukannya di Start Menu atau dengan mencari "SQL Server Management Studio."

2. **Sambungkan ke Instans SQL Server**: Di SSMS, sambungkan ke instans SQL Server tempat Anda ingin memulihkan database. Anda memerlukan izin yang diperlukan untuk melakukan operasi ini.

3. **Pulihkan Basis Data**:

A. Di panel Object Explorer di sisi kiri, perluas instans SQL Server.

B. Perluas simpul "Database".

C. Klik kanan pada "Database" dan pilih "Pulihkan Database".

4. **Tentukan Sumber dan Tujuan**:

A. Di halaman "Umum" pada kotak dialog "Pulihkan Basis Data", masukkan nama untuk basis data baru di bidang "Ke basis data". Ini akan menjadi nama database yang dipulihkan.

B. Di bagian "Sumber", pilih "Perangkat" sebagai jenis media cadangan.

C. Klik tombol "..." di sebelah kolom "Perangkat" untuk menelusuri file ".bak" yang ingin Anda pulihkan.

D. Pilih file ".bak" yang ingin Anda buka dan klik "OK."

5. **Opsi Pemulihan**: Tinjau dan konfigurasikan opsi pemulihan sesuai kebutuhan. Anda dapat menentukan apakah akan menimpa database yang sudah ada, mengatur opsi pemulihan, dan lainnya. Pastikan untuk mengatur opsi ini sesuai dengan kebutuhan Anda.

6. **Mulai Pemulihan**: Setelah Anda mengonfigurasi opsi pemulihan, klik tombol "OK" di kotak dialog "Pulihkan Basis Data". SQL Server akan memulai proses pemulihan.

7. **Akses Database yang Dipulihkan**: Setelah pemulihan berhasil, Anda dapat mengakses database yang dipulihkan di SQL Server Management Studio sama seperti database lainnya. Anda bisa menjalankan kueri, melihat tabel, dan bekerja dengan data dalam database.

## File BAK lainnya

Berikut jenis file lain yang menggunakan ekstensi file **.bak**.

**Basis Data**
- [BAK - File Cadangan Basis Data](/id/database/bak/)
- [BAK - Aksi Swiftpage! Pencadangan Basis Data](/id/database/bak-act/)

**Permainan**
- [BAK - Dunia Terraria atau Cadangan Pemain](/id/game/bak-terraria/)

**Lain-lain**
- [BAK - File Cadangan](/id/misc/bak-backup/)
- [BAK - Cadangan Bookmark Chromium](/id/misc/bak-chromium/)
- [BAK - Cadangan Skor Akhir 2012](/id/misc/bak-finale/)
- [BAK - Cadangan MobileTrans](/id/misc/bak-mobiletrans/)
- [BAK - Pencadangan Proyek Video VEGAS](/id/misc/bak-vegas/)

**Pengaturan**
- [BAK - Cadangan Peluncur Holo](/id/settings/bak-holo/)

## Referensi
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
