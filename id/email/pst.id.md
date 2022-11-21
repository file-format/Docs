{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Format File Penyimpanan Informasi Pribadi Outlook",
  "description":"Pelajari tentang format file PST dan API yang dapat membuat dan membuka file PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PST?

File dengan ekstensi .pst mewakili File Penyimpanan Pribadi Outlook (juga disebut Tabel Penyimpanan Pribadi) yang menyimpan berbagai informasi pengguna. Informasi pengguna disimpan dalam berbagai jenis folder yang mencakup email, item kalender, catatan, kontak, dan beberapa format file lainnya. File PST digunakan untuk mengarsipkan data email secara offline yang nantinya dapat dimuat dan dilihat di berbagai aplikasi.

## Spesifikasi Format File PST

Format File PST [spesifikasi](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) tersedia dari Microsoft sebagai lisensi paten gratis dan tidak dapat dibatalkan melalui Janji Spesifikasi Terbuka .

### Jenis Format PST

Format file PST dikategorikan dalam dua jenis berdasarkan pengkodean jenis file. File PST yang disandikan ANSI adalah format file yang lebih lama dan hanya didukung oleh Outlook 2002 dan versi sebelumnya. File tersebut memiliki batas ukuran maksimum 2 GB (2^^31^^ Bytes) dan tidak mendukung Unicode. Jenis format file yang lebih modern, berdasarkan pengkodean Unicode, menghilangkan batasan ukuran file dan dapat mencapai ukuran data maksimum 50GB.

### Organisasi Logis Format File PST

Di dasar format file PST terletak B-Tree yang membuat data diurutkan dan memungkinkan pencarian, akses berurutan, penyisipan, penghapusan, dll. dalam waktu logaritmik. Struktur keseluruhan file PST diatur dalam tiga lapisan.

![Logical layers of a PST file](/id/email/PST-1.png "Logical layers of a PST file")

`Lapisan Basis Data Node (NDB)` - Lapisan basis data simpul terletak di tingkat yang lebih rendah dari file PST dan menyertakan basis data simpul. Node ini sebenarnya mewakili fasilitas penyimpanan tingkat rendah dari format file PST. Lapisan NDB terdiri dari header, informasi alokasi file, blok, dan Btrees (Node BTree dan Block BTree) dari sudut pandang penyimpanan. Node dan Blok Lapisan NDB ditautkan melalui Data BID yang merupakan salah satu dari empat properti referensi Node yaitu NID (Node ID), NID Induk, Data BID (Block BID) dan SubNode BID.

Lapisan `Daftar, Tabel, dan Properti -` Lapisan LTP memberikan pemahaman logis tentang konsep tingkat tinggi di atas NDB. Selain elemen lainnya, lapisan LTP terutama terdiri dari Konteks Properti (PC) dan Konteks Tabel (TC). PC adalah kumpulan properti, sedangkan TC mewakili matriks dua dimensi dari kumpulan properti vs. Implementasi PC dan TC yang efisien, lapisan LTP menggunakan dua jenis struktur data berikut di atas NDB Node:

* Heap On Node (HN) - memungkinkan sub-alokasi aliran data dari sebuah node menjadi fragmen kecil berukuran variabel.
* BTree on Heap (BTH) - BTH menyediakan cara yang nyaman dan praktis untuk mencari melalui PC data, dijelaskan di atas, diimplementasikan sebagai BTH dan itulah mengapa diimplementasikan dengan membangun di dalam struktur HN.

`Lapisan Pesan -` Aturan tingkat tinggi dan logika bisnis untuk bekerja dengan file PST diimplementasikan pada lapisan ini. Keluaran logis dari lapisan ini menghasilkan objek Folder, objek Pesan, objek Lampiran, dan Properti yang dimungkinkan dengan menggabungkan lapisan LTP dan NDB. Aturan dan persyaratan, yang harus diikuti saat memodifikasi konten PST, juga ditentukan di lapisan ini.

### Organisasi Fisik Format File PST

Organisasi file tingkat tinggi dari file PST seperti yang ditunjukkan pada gambar di bawah ini. Ini hanyalah ikhtisar berbagai konsep dari elemen logis file PST.

![Physical organization of the PST file format](/id/email/PST-2.png "Physical organization of the PST file format")


#### Informasi Header PST

Struktur HEADER file PST terletak di awal file dengan offset 0. Ini berisi informasi metadata tentang file PST dan informasi ROOT untuk mengakses struktur data Lapisan NDB yang dijelaskan di atas. Struktur HEADER berbeda untuk versi Format File PST Unicode dan ANSI.

Header dimulai dengan kata ajaib 4-byte **!BDN** yang diwakili oleh byte (0x21, 0x42, 0x44, 0x4E). Nomor ajaib 2-byte lainnya, **SM** (0x53, 0x4D), terletak di offset 8 dari awal file. Informasi versi (ANSI atau Unicode) terletak pada offset 10 dari awal file. Nilai hex (0x17) menentukan file Unicode PST sementara 0x0E atau 0x0F mewakili format file ANSI.

|Bidang|Deskripsi
---|---|
|dwMagic (4 byte)|HARUS berupa "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|Nilai CRC 32-bit dari 471 byte data mulai dari wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|HARUS berupa "{ 0x53, 0x4D }".
|wVer (2 byte)|Versi format file. Nilai ini HARUS 14 atau 15 jika file tersebut adalah file ANSI PST, dan HARUS 23 jika file tersebut adalah file Unicode PST.
|wVerClient (2 byte)|Versi format berkas klien. Versi yang sesuai dengan format yang dijelaskan dalam dokumen ini adalah 19. Pembuat file PST baru berdasarkan dokumen ini HARUS menginisialisasi nilai ini ke 19.
|bPlatformCreate (1 byte)|Nilai ini HARUS disetel ke 0x01.
|bPlatformAccess (1 byte)|Nilai ini HARUS disetel ke 0x01.
|dwReserved (8 byte)|
|bidUnused (hanya Unicode 8 byte)|Padding yang tidak digunakan ditambahkan saat format file PST Unicode dibuat.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|Halaman selanjutnya BID. Halaman memiliki penghitung khusus untuk mengalokasikan nilai bidIndex. Nilai bidIndex untuk BID halaman dialokasikan dari penghitung ini.
|bidNextB (hanya ANSI 4 byte): |BID Berikutnya. Nilai ini adalah penghitung monoton yang menunjukkan BID yang akan ditetapkan untuk blok yang dialokasikan berikutnya. Nilai BID naik dengan kelipatan 4. Untuk detail lebih lanjut, lihat bagian 2.2.2.2.
|dwUnique (4 byte)|Ini adalah nilai yang meningkat secara monoton yang dimodifikasi setiap kali struktur HEADER file PST diubah. Fungsi dari nilai ini adalah untuk memberikan nilai yang unik, dan untuk memastikan bahwa CRC HEADER berbeda setelah setiap modifikasi header.
|rgnid[] (128 byte)|Suatu array tetap berisi 32 NID, masing-masing sesuai dengan salah satu dari 32 kemungkinan NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwTidak terpakai (8 byte)|Ruang tidak terpakai; HARUS diatur ke nol. Format file PST Unicode saja.
|root (Unicode: 72 byte; ANSI: 40 byte)|Struktur ROOT (bagian 2.2.2.5).
|dwAlign (4 byte)|Byte penyelarasan yang tidak digunakan; HARUS diatur ke nol. Format file PST Unicode saja.
|rgbFM (128 byte)|FMap yang tidak digunakan lagi. Ini tidak lagi digunakan dan HARUS diisi dengan 0xFF. Pembaca HARUS mengabaikan nilai byte ini.
|rgbFP (128 byte)|FPMap yang tidak digunakan lagi. Ini tidak lagi digunakan dan HARUS diisi dengan 0xFF. Pembaca HARUS mengabaikan nilai byte ini.
|bSentinel (1 byte)|HARUS diatur ke 0x80.
|bCryptMethod (1 byte)|Menunjukkan bagaimana data dalam file PST dikodekan. HARUS disetel ke salah satu nilai yang telah ditentukan sebelumnya (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved (2 byte)| Disimpan; HARUS diatur ke nol.
|bidNextB (8 byte)|Menunjukkan nilai BID berikutnya yang tersedia. Format file PST Unicode saja.
|bidNextB (HANYA Unicode: 8 byte)|BID Berikutnya. Nilai ini adalah penghitung monoton yang menunjukkan BID yang akan ditetapkan untuk blok yang dialokasikan berikutnya. Nilai BID naik dengan kelipatan 4. Untuk detail lebih lanjut, lihat bagian 2.2.2.2.
|dwCRCFull (4 byte)|Nilai CRC 32-bit dari 516 byte data mulai dari wMagicClient hingga bidNextB, inklusif. Format file PST Unicode saja.
|ullDicadangkan (8 byte)|Dicadangkan; HARUS diatur ke nol. Format file ANSI PST saja.
|dwDicadangkan (4 byte)|Dicadangkan; HARUS diatur ke nol. Format file ANSI PST saja.
|rgbReserved2 (3 byte)|
|bDicadangkan (1 byte) |
|rgbReserved3 (32 byte) |

### Perlindungan data ###

Untuk keamanan, file PST juga dapat dilindungi kata sandi yang mengharuskan aplikasi pemuatan menerapkan kata sandi sebelum dapat dilihat. Kata sandi yang diterapkan ke file PST disimpan di penyimpanan pesan. Namun, ini tidak memberikan perlindungan data yang kuat karena kata sandi dapat dihapus oleh alat yang tersedia. Selain itu, kata sandi yang ditentukan pengguna tidak digunakan sebagai bagian dari kunci untuk pengodean dan penguraian kode sandi algoritma. Dengan demikian, tidak ada manfaat melindungi data untuk diakses oleh pihak yang tidak berwenang. Penyimpanan kata sandi sebagai hash CRC-32 dari string asli juga menjadikannya metode yang lemah untuk keamanan data terhadap pendekatan brute-force.

## Referensi ##

* [Format File Folder Pribadi Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Spesifikasi Format File Folder Pribadi](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

