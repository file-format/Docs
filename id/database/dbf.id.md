{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "ekstensi", "file dbf", "format file dbf", "Tipe File Basis Data", "Format File Basis Data", "apa itu file dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DBF dan API yang dapat membuat dan membuka file DBF.",
  "title" :"DBF - Berkas Basis Data dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Apa itu file DBF?
File dengan ekstensi .dbf adalah file database yang digunakan oleh aplikasi sistem manajemen database bernama **dBASE**. Awalnya, database dBASE bernama Project Vulcan; dimulai oleh **Wayne Ratliff** pada tahun 1978. Jenis file DBF diperkenalkan dengan dBASE II pada tahun 1983. Ini mengatur beberapa catatan data dengan bidang jenis Array. Software database **xBase** yang populer karena kompatibilitasnya dengan berbagai format file; juga mendukung file DBF.

## Format File DBD
Format file DBF milik sistem manajemen basis data dBASE tetapi mungkin kompatibel dengan xBase atau perangkat lunak DBMS lainnya. Versi awal file dbf terdiri dari tabel sederhana yang dapat menambahkan, memodifikasi, menghapus, atau mencetak data menggunakan rangkaian karakter ASCII. Dengan berlalunya waktu .dbf ditingkatkan, dan file tambahan ditambahkan untuk meningkatkan fitur dan kemampuan sistem database.

Dalam dBASE modern, file DBF terdiri dari header, catatan data, dan penanda EOF (End of File)

- Header berisi informasi tentang file, seperti jumlah record dan jumlah tipe field yang digunakan dalam record.
- Catatan berisi data aktual.
- Akhir file ditandai dengan satu byte, dengan nilai 0x1A.

### Tajuk berkas
Tata letak header file di dBase diberikan dalam tabel berikut:

| byte | Isi | Arti |
---|---|---|
| 0 | 1 byte | dBASE yang valid untuk file DOS; bit 0–2 menunjukkan nomor versi, bit 3 menunjukkan adanya dBASE untuk file memo DOS, bit 4–6 menunjukkan adanya tabel SQL, bit 7 menunjukkan adanya file memo apa pun (baik dBASE m PLUS atau dBASE untuk DOS) |
| 1–3 | 3 byte | Tanggal pembaruan terakhir; diformat sebagai YYMMDD |
| 4–7 | nomor 32-bit | Jumlah catatan dalam file database |
| 8–9 | nomor 16-bit | Jumlah byte di header |
| 10–11 | nomor 16-bit | Jumlah byte dalam catatan |
| 12–13 | 2 byte | Disimpan; isi dengan 0 |
| 14 | 1 byte | Bendera yang menunjukkan transaksi tidak lengkap[catatan 1] |
| 15 | 1 byte | Bendera enkripsi[catatan 2] |
| 16–27 | 12 byte | Dicadangkan untuk dBASE untuk DOS di lingkungan multi-pengguna |
| 28 | 1 byte | Bendera file produksi .mdx; 1 jika ada file produksi .mdx, 0 jika tidak |
| 29 | 1 byte | ID pengemudi bahasa |
| 30–31 | 2 byte | Disimpan; isi dengan 0 |
| 32–n [nada 3][nada 4] | masing-masing 32 byte | array deskriptor bidang (lihat di bawah untuk tata letak deskriptor) |
| n + 1 | 1 byte | 0x0D sebagai terminator array deskriptor bidang |

- Fungsi ISMARKEDO memeriksa flag ini (BEGIN TRANSACTION atur ke 1, END TRANSACTION dan ROLLBACK reset ke 0).
- Jika bendera ini disetel ke 1, pesan Database dienkripsi muncul.
- Jumlah maksimum bidang adalah 255.
- n berarti byte terakhir dalam larik deskriptor bidang.

### Larik deskriptor bidang
Tata letak deskriptor bidang di dBASE:

| byte | Isi | Arti |
---|---|---|
| 0–10 | 11 byte | Nama bidang dalam ASCII (diisi nol) |
| 11 | 1 byte | Jenis bidang. Nilai yang diizinkan: C, D, F, L, M, atau N (lihat tabel berikutnya untuk artinya) |
| 12–15 | 4 byte | Dicadangkan |
| 16 | 1 byte | Panjang bidang dalam biner (maksimum 254 (0xFE)). |
| 17 | 1 byte | Jumlah desimal bidang dalam biner |
| 18–19 | 2 byte | ID wilayah kerja |
| 20 | 1 byte | Contoh |
| 21–30 | 10 byte | Dicadangkan |
| 31 | 1 byte | Bendera bidang produksi MDX; 1 jika bidang memiliki tag indeks dalam file MDX produksi, 0 jika tidak |

### Data database
Setiap catatan dimulai dengan bendera penghapusan (1-byte). Bidang dibungkus ke dalam rekaman tanpa pemisah bidang. Semua data lapangan adalah ASCII. Bergantung pada jenis bidang, aplikasi memberlakukan pembatasan lebih lanjut. Berikut adalah jenis bidang di dBase:

| Jenis bidang | Mnemonik | Apa yang diterimanya |
-------|-----|----|
| C | Karakter | Teks ASCII apa pun (diisi dengan spasi hingga panjang bidang) |
| D | Tanggal | Angka dan karakter untuk memisahkan bulan, hari, dan tahun (disimpan secara internal sebagai 8 digit dalam format YYYYMMDD) |
| F | Titik terapung | -, ., 0–9 (kanan dibenarkan, diisi dengan spasi putih) |
| L | Logis | Y, y, N, n, T, t, F, f, atau ? (saat tidak diinisialisasi) |
| M | Memo | Teks ASCII apa pun (disimpan secara internal sebagai 10 digit yang mewakili nomor blok .dbt, rata kanan, diisi dengan spasi putih) |
| N | Numerik | -, ., 0–9 (kanan dibenarkan, diisi dengan spasi putih) |









## Referensi ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

