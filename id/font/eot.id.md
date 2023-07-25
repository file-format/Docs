{
  "date" : "2020-08-20",
  "keywords" :[ "file eot", "format file eot", "apa itu file eot", "file", "contoh eot", "ekstensi file eot", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Format File Font TrueType",
  "description":"Pelajari tentang Format File EOT dan API untuk membuat dan membuka file EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Apa itu file EOT?

File dengan ekstensi .eot adalah font OpenType yang tertanam dalam dokumen. Ini sebagian besar digunakan dalam file web seperti halaman Web. Itu dibuat oleh Microsoft dan didukung oleh Produk Microsoft termasuk file presentasi PowerPoint [.pps](/id/presentation/pps). File tersebut bukan penggunaan utama dan semacam dokumen pendamping dengan dokumen utama atau halaman web. Mirip dengan font OTF, EOT mendukung kerangka Postscript dan TrueType untuk mesin terbang. File EOT berukuran lebih kecil karena dikompresi menggunakan kompresi LZ. EOT menggunakan alat Microsoft untuk membuat font dari font TTF/OTF yang ada.

## Sejarah Singkat

Font EOT diajukan ke W3C pada tahun 2007 sebagai bagian dari CSS3 tetapi karena persyaratannya untuk diinstal secara permanen pada sistem jarak jauh menjadi alasan penolakannya. Itu dikirim ulang pada Maret 2008, tetapi W3C akhirnya memilih [Web Font Format](/id/font/woff/) (WOFF) yang kemudian distandarisasi.

## Format File EO

Detail format file EOT dapat ditemukan di [halaman pengiriman W3](https://www.w3.org/Submission/EOT/#FileFormat) dan menguraikan struktur yang digunakan oleh format font ini. EOT terdiri dari satu struktur EMBEDDEDFONT yang memberikan informasi dasar yang cukup tentang nama font dan karakter yang didukung. Pengemasan informasi ini memungkinkan Agen Pengguna untuk menghindari pembongkaran, dekompresi, atau penginstalan font jika sudah ada di mesin.

### Struktur EMBEDDEDFONT
Struktur EMBEDDEDFONT telah mengalami tiga kali revisi, dengan penambahan data tambahan di akhir struktur pada setiap revisi. Revisi terakhir dari struktur EMBEDDEDFONT seperti yang digambarkan di bawah ini.

|Tipe Data|Nama Entri|Deskripsi|
---|---|---|
|unsigned long|EOTSize|Total panjang struktur dalam byte (termasuk data string dan font)|
|unsigned long|FontDataSize|Panjang font OpenType (FontData) dalam byte|
|unsigned long|Versi|Nomor versi format ini - 0x00020002|
|unsigned long|Flags|Processing Flags|
|byte[10]|FontPANOSE|Nilai PANOSE untuk font ini - Lihat http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Di Windows ini diturunkan dari TEXTMETRIC.tmCharSet. Nilai ini menentukan set karakter font. DEFAULT_CHARSET (0x01) menunjukkan tidak ada preferensi. - Lihat https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Jika bit untuk ITALIC diatur di OS/2.fsSelection, nilainya akan menjadi 0x01 - Lihat http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|Nilai bobot untuk font ini - Lihat http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Type flags yang memberikan informasi tentang izin penyematan - Lihat http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Nomor ajaib untuk berkas EOT - 0x504C. Digunakan untuk memeriksa kerusakan data.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bit 32-63) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Lihat http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Lihat https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - harus 0|
|unsigned long|Reserved2|Reserved - harus 0|
|unsigned long|Reserved3|Reserved - harus 0|
|unsigned long|Reserved4|Reserved - harus 0|
|unsigned short|Padding1|Padding untuk menjaga keselarasan panjang. Nilai pengisi harus selalu disetel ke 0x0000.|
|unsigned short|FamilyNameSize|Jumlah byte yang digunakan oleh array FamilyName|
|byte|FamilyName[FamilyNameSize]|Array karakter UTF-16 sepanjang byte FamilyNameSize. Ini adalah string Keluarga Font bahasa Inggris yang ditemukan di tabel nama font (name ID = 1) - Lihat http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Padding value harus selalu disetel ke 0x0000.|
|unsigned short|StyleNameSize|Jumlah byte yang digunakan oleh StyleName|
|byte|StyleName[StyleNameSize]|Array karakter UTF-16 sepanjang byte StyleNameSize. Ini adalah string Subfamili Font bahasa Inggris yang ditemukan di tabel nama font (name ID = 2) - Lihat http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Padding value harus selalu disetel ke 0x0000.|
|unsigned short|VersionNameSize|Jumlah byte yang digunakan oleh VersionName|
|bytes|VersionName[VersionNameSize]|Array karakter UTF-16 sepanjang byte VersionNameSize. Ini adalah string versi bahasa Inggris yang ditemukan di tabel nama font (name ID = 5) - Lihat http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Padding value harus selalu disetel ke 0x0000.|
|unsigned short|FullNameSize|Jumlah byte yang digunakan oleh FullName|
|byte|FullName[FullNameSize]|Array karakter UTF-16 sepanjang byte FullNameSize. Ini adalah string nama lengkap bahasa Inggris yang ditemukan di tabel nama font (name ID = 4) - Lihat http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Padding value harus selalu disetel ke 0x0000.|
|unsigned short|RootStringSize|Jumlah byte yang digunakan oleh array RootString|
|byte|RootString[RootStringSize]|Array karakter UTF-16 sepanjang byte RootStringSize.|
|unsigned long|RootStringCheckSum|RootString CheckSum nilai. Lihat algoritma untuk memproses RootStringChecksum di bawah ini.|
|unsigned long|EUDCCodePage|Nilai halaman kode diperlukan untuk dukungan font EUDC.|
|unsigned short|Padding6|Padding value harus selalu disetel ke 0x0000.|
|unsigned short|SignatureSize|Jumlah byte yang digunakan oleh array Signature. Saat ini dicadangkan dan harus disetel ke 0x0000.|
|byte|Signature[SignatureSize]|Saat ini dicadangkan. Jika SignatureSize adalah 0x0000 tidak ada panjang untuk array ini.|
|unsigned long|EUDCFlags|Memproses flag untuk font EUDC. Nilai umum mungkin TTEMBED_XORENCRYPTDATA dan TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Jumlah byte yang digunakan oleh array Signature.|
|byte|EUDCFontData[EUDCFontSize]|Jumlah byte yang digunakan untuk data font EUDC. Jika EUDCFontSize adalah 0x00000000 tidak ada panjang untuk array ini.|
|byte|FontData[FontDataSize]|Data font untuk file EOT ini. Data dapat dikompresi atau dienkripsi XOR seperti yang ditunjukkan oleh flag pemrosesan.|

## Referensi

* [Format File EOT](https://www.w3.org/Submission/EOT/)
* [Jenis Terbuka Tertanam](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Penyematan Font](https://en.wikipedia.org/wiki/Font_embedding)

