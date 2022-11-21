{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MPG",
  "keywords" :[ "MPG", "file", "ekstensi", "format", "format video", "apa itu format file mpg", "format file mpg", "pemutar file mpg", "kompresi mpeg", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Pelajari tentang format file MPG dan API yang dapat membuat dan menunjukkan cara membuka file MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Apa itu format file MPG? ##

File dengan ekstensi .mpg milik grup ekstensi file untuk kompresi audio dan video MPEG-1 atau MPEG-2. Video MPEG-1 Bagian 2 tidak mudah tersedia, dan ekstensi ini (format file MPG) biasanya mengarah ke aliran program MPEG yang ditentukan dalam MPEG-1 dan MPEG-2, atau aliran transport MPEG yang ditentukan dalam MPEG-2 . Ekstensi lain seperti .m2ts juga ada yang menentukan wadah yang akurat, dalam hal ini, MPEG-2 TS, tetapi ini memiliki sedikit relevansi dengan media MPEG-1. [.mp3](https://docs.fileformat.com/audio/mp3/) adalah ekstensi paling umum untuk file yang berisi audio MP3. File MP3 adalah aliran audio mentah yang khas; cara tradisional untuk menandai file MP3 adalah dengan menulis aliran data ke segmen "sampah" dari setiap frame, yang menyimpan informasi media tetapi dibuang oleh **pemutar file mpg**. Ini adalah teknik serupa yang digunakan untuk menandai file AAC, tetapi saat ini kurang didukung.

## Kompresi MPEG ##

Nama MPEG adalah singkatan dari Moving Pictures Experts Group. MPEG adalah alat untuk kompresi video, yang melibatkan kompresi gambar dan suara, serta sinkronisasi keduanya.
Saat ini ada beberapa standar MPEG.

- MPEG-1 diusulkan untuk kecepatan data menengah, dengan urutan 1,5 Mbit/detik.
- MPEG-2 diusulkan untuk kecepatan data tinggi minimal 10 Mbit/detik.
- MPEG-3 diusulkan untuk kompresi HDTV tetapi ternyata berlebihan dan digabungkan dengan MPEG-2.
- MPEG-4 diusulkan untuk kecepatan data yang sangat rendah kurang dari 64 Kbit/detik.


## Aliran program format file MPG ##

Aliran program adalah wadah untuk multiplexing audio digital, video, dan lainnya. Format Stream Program ditentukan dalam bagian pertama MPEG-1 (ISO/IEC 11172-1) dan bagian pertama MPEG-2, Sistem (standar ISO/IEC 13818-1/ITU-T H.222.0). Aliran Program MPEG-2 berbasis analog dan mirip dengan lapisan Sistem ISO/IEC 11172 dan kompatibel ke depan.

### Detail pengkodean ###

Berikut adalah detail pengkodean format header paket MPEG-2 Program Stream parsial:

| Nama | Jumlah bit | Deskripsi |
---|---|---|
| sinkronkan byte | 32 | 0x000001BA |
| bit penanda | 2 | 01b untuk versi MPEG-2. Bit penanda untuk versi MPEG-1 adalah 4 bit dengan nilai 0010b. |
| Jam sistem [32..30] | 3 | Referensi Jam Sistem (SCR) bit 32 hingga 30 |
| penanda bit | 1 | 1 Bit selalu disetel. |
| Jam sistem [29..15] | 15 | Jam sistem bit 29 hingga 15 |
| penanda bit | 1 | 1 Bit selalu disetel. |
| Jam sistem [14..0] | 15 | Jam sistem bit 14 hingga 0 |
| penanda bit | 1 | 1 Bit selalu disetel. |
| ekstensi SCR | 9 | |
| penanda bit | 1 | 1 Bit selalu disetel. |
| laju bit | 22 | Dalam satuan 50 byte per detik. |
| bit penanda | 2 | 11 Bit selalu disetel. |
| dipesan | 5 | dicadangkan untuk penggunaan mendatang |
| panjang isian | 3 | |
| isian byte | 8 * panjang isian | |
| tajuk sistem (opsional) | 0 atau lebih | jika kode mulai tajuk sistem mengikuti: 0x000001BB |

Tabel berikut menunjukkan format header sistem parsial:

| Nama | Jumlah byte | Deskripsi |
---|---|---|
| sinkronkan byte | 4 | 0x000001BB |
| panjang tajuk | 2 | |
| tingkat terikat dan bit penanda | 3 | |
| terikat audio dan bendera | 1 | |
| bendera, bit penanda, dan video terikat | 1 | |
| Pembatasan laju paket dan byte yang dipesan | 1 | |


## Referensi ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



