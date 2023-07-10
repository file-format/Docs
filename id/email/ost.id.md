{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Format Berkas Penyimpanan Outlook",
  "description":"Pelajari tentang format file OST dan API yang dapat membuat dan membuka file OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file OST?

File Penyimpanan OST atau Offline mewakili data kotak surat pengguna dalam mode offline di mesin lokal setelah pendaftaran dengan Exchange Server menggunakan Microsoft Outlook. Ini secara otomatis dibuat pada penggunaan pertama Microsoft Outlook setelah terhubung dengan server. Setelah file dibuat, data disinkronkan dengan server email sehingga tersedia secara offline juga jika terputus dari server email. File OST dapat item kotak surat pengguna seperti email, kontak, informasi kalender, catatan, tugas, dan data serupa lainnya. Pengguna dapat membuat email dan item data lainnya dalam file OST meskipun tidak ada koneksi ke server, tetapi ini tidak akan disinkronkan dengan server. Setelah koneksi dibuat, file lokal disinkronkan kembali dengan server sehingga server dan salinan lokal berada pada tingkat informasi yang sama.

## Format File OST

Format file OST (Tabel Penyimpanan Offline) dan [PST](/id/email/pst/) (Tabel Penyimpanan Pribadi) terdiri dari format File Folder Pribadi (PFF) yang terkait dengan penyimpanan email, kontak, dan janji temu pengguna. Data dalam file PFF disimpan dalam little-endian dengan semua tanggal dan waktu direpresentasikan sebagai FILETIME dalam UTC. [MS-PST] mendefinisikan dua jenis PFF:

* Format ANSI 32-bit
* Format Unicode 64-bit

Format file PST [spesifikasi](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), seperti yang tersedia dari Microsoft, juga berlaku untuk format file OST gratis dan lisensi paten yang tidak dapat dibatalkan melalui Janji Spesifikasi Terbuka. Ini terdiri dari elemen-elemen yang dapat dibedakan berikut ini:

* Fle header
* File data tajuk
* Node cabang indeks
* Indeks daun simpul
* (File) indeks offset
* (Item) indeks deskriptor
* Deskriptor lokal
* Jenis tabel barang

### Informasi Tajuk

Struktur HEADER file OST terletak di awal file dengan offset 0. Ini berisi informasi metadata tentang file OST dan informasi ROOT untuk mengakses struktur data Lapisan NDB yang dijelaskan di atas. Struktur HEADER berbeda untuk versi Unicode dan ANSI dari Format File OST.

Header dimulai dengan kata ajaib 4-byte **!BDN** yang diwakili oleh byte (0x21, 0x42, 0x44, 0x4E). Nomor ajaib 2-byte lainnya, **SM** (0x53, 0x4D), terletak di offset 8 dari awal file. Informasi versi (ANSI atau Unicode) terletak pada offset 10 dari awal file. Nilai hex (0x17) menentukan file Unicode OST sementara 0x0E atau 0x0F mewakili format file ANSI.

|Bidang|Deskripsi
---|---|
|dwMagic (4 byte)|HARUS berupa "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 byte)|Nilai CRC 32-bit dari 471 byte data mulai dari wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|HARUS berupa "{ 0x53, 0x4D }".
|wVer (2 byte)|Versi format file. Nilai ini HARUS 14 atau 15 jika file tersebut adalah file ANSI PST, dan HARUS 23 jika file tersebut adalah file Unicode PST.
|wVerClient (2 byte)|Versi format berkas klien. Versi yang sesuai dengan format yang dijelaskan dalam dokumen ini adalah 19. Pembuat file PST baru berdasarkan dokumen ini HARUS menginisialisasi nilai ini ke 19.
|bPlatformCreate (1 byte)|Nilai ini HARUS disetel ke 0x01.
|bPlatformAccess (1 byte)|Nilai ini HARUS disetel ke 0x01.
|dwReserved (8 byte)|
|bidUnused (hanya Unicode 8 byte)|Padding yang tidak digunakan ditambahkan saat format file PST Unicode dibuat.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|Halaman selanjutnya BID. Halaman memiliki penghitung khusus untuk mengalokasikan nilai bidIndex. Nilai bidIndex untuk BID halaman dialokasikan dari penghitung ini.
|bidNextB (hanya ANSI 4 byte): |BID Berikutnya. Nilai ini adalah penghitung monoton yang menunjukkan BID yang akan ditetapkan untuk blok yang dialokasikan berikutnya. Nilai BID naik dengan kelipatan 4. Untuk detail lebih lanjut, lihat bagian 2.2.2.2.
|dwUnique (4 bytes)|Ini adalah nilai yang meningkat secara monoton yang dimodifikasi setiap kali struktur HEADER file PST diubah. Fungsi dari nilai ini adalah untuk memberikan nilai yang unik, dan untuk memastikan bahwa CRC HEADER berbeda setelah setiap modifikasi header.
|rgnid[](128 byte)|Suatu array tetap berisi 32 NID, masing-masing sesuai dengan salah satu dari 32 kemungkinan NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
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

## Referensi

* [Format File Folder Pribadi Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Spesifikasi Format File Folder Pribadi](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

