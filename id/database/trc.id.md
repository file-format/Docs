{
  "date" : "2021-08-24",
  "keywords" :[ "file trc", "format file trc", "apa itu file trc", "file", "contoh trc", "ekstensi file trc", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file TRC dan API yang dapat membuat dan membuka file TRC.",
  "title" :"TRC - File Pelacakan SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Apa itu file TRC?
File dengan ekstensi .trc berisi hasil penelusuran aktivitas database server Microsoft SQL. File-file ini dibuat oleh perangkat lunak SQL Server Profiler; biasanya dikemas dengan perangkat lunak Microsoft SQL Server. Administrator basis data dapat menganalisis urutan pernyataan basis data dan dapat meninjau log pelacakan jika ada dugaan kesalahan atau peringatan. File-file ini biasanya terletak di folder LOG khas MSSQL di dalam direktori Program Files pada sistem operasi Windows.

## format file TRC
Format file TRC digunakan oleh SQL Server Profiler untuk secara otomatis menghasilkan jejak baru dari pernyataan yang baru saja dieksekusi oleh MS SQL server. SQL Server Profiler menggunakan template default untuk semua pelacakan baru. Namun, perangkat lunak menyertakan beberapa templat yang telah ditentukan sebelumnya untuk memantau jenis acara tertentu. SQL Server Profiler juga dapat digunakan untuk membuat template yang menentukan kelas kejadian dan kolom data untuk disertakan dalam pelacakan.

### Template Standar
Berikut adalah daftar beberapa template standar yang disertakan dalam SQL Server Profiler:
- **SP_Counts**: Merekam perilaku eksekusi prosedur tersimpan dari waktu ke waktu.
- **Standar**: Titik awal umum untuk membuat pelacakan.
- **TSQL**: Menangkap semua pernyataan Transact-SQL yang dikirimkan ke SQL Server oleh klien dan waktu yang dikeluarkan.
- **TSQL_Duration**: Menangkap semua pernyataan Transact-SQL yang dikirimkan ke SQL Server oleh klien, waktu eksekusinya, dan mengelompokkannya berdasarkan durasi.
- **TSQL_Grouped**: Gunakan untuk menyelidiki kueri dari klien atau pengguna tertentu.
- **TSQL_Locks**: Gunakan untuk memecahkan masalah kebuntuan, mengunci waktu habis, dan mengunci kejadian eskalasi.
- **TSQL_Replay**: Gunakan untuk melakukan penyetelan berulang, seperti pengujian tolok ukur.
- **TSQL_SPs**: Gunakan untuk menganalisis langkah-langkah komponen prosedur tersimpan.
- **Penyetelan**: Gunakan untuk menghasilkan output pelacakan yang dapat digunakan Penasihat Penyetelan Mesin Database sebagai beban kerja untuk menyetel basis data.
### Korelasikan pelacakan dengan data Log Kinerja Windows
SQL Server Profiler dapat digunakan untuk membuka log kinerja Microsoft Windows, untuk memilih penghitung yang akan dikorelasikan dengan pelacakan, dan menampilkan penghitung kinerja yang dipilih di samping pelacakan di MS SQL Server Profiler GUI. Untuk menunjukkan data log kinerja yang berkorelasi dengan peristiwa pelacakan yang dipilih, bilah merah vertikal di panel jendela data Monitor Sistem dari SQL Server Profiler.


## Referensi ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

