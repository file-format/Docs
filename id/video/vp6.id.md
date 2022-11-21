{
  "date" : "2021-02-15",
  "keywords" :[ "file vp6", "format file vp6", "apa itu file vp6", "file", "contoh vp6", "ekstensi file vp6", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Berkas Video TrueMotion",
  "description":"Pelajari tentang format file VP6 dan API yang dapat membuat dan membuka file VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Apa itu file VP6?

VP6 adalah format video kompresi lossy yang diperkenalkan oleh teknologi On2 pada Mei 2003. Ini adalah bagian dari rangkaian codec video yang dikembangkan oleh TrueMotion termasuk V3, V4 dan V5. Format ini digunakan segera di bidang penyiaran seperti laporan BBC dan perangkat lunak QuickLink. VP6 digantikan oleh VP7 Codec pada Januari 2005 dengan kompatibilitas kompresi yang lebih baik.

## Format File VP6

Spesifikasi lengkap untuk file V6 tidak tersedia untuk umum. On2 membuat spesifikasinya untuk publik pada awalnya tetapi segera ini dibuat tidak tersedia untuk pengguna umum. Dokumentasi tidak resmi dari format file VP6 tersedia di [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) yang dapat dirujuk untuk referensi pengembang.

### Blok Makro (MB)

Mirip dengan MPEG-2, MPEG-4 bagian 2 dan 10, setiap frame video dari file VP6 terdiri dari array 16x16 macroblocks (MB). Setiap MB dapat berada dalam salah satu mode berikut:

* IntraMB
* Inter MB, null MV, referensi bingkai sebelumnya
* Inter MB, MV diferensial, referensi bingkai sebelumnya
* Inter MB, empat MV, referensi bingkai sebelumnya
* Inter MB, MV 1, referensi bingkai sebelumnya
* Inter MB, MV 2, referensi bingkai sebelumnya
* Inter MB, null MV, referensi bingkai yang di-bookmark
* Inter MB, MV diferensial, referensi bingkai yang ditandai
* Inter MB, MV 1, referensi bingkai yang di-bookmark
* Inter MB, MV 2, referensi bingkai yang di-bookmark

### Tajuk Bingkai

Header bingkai VP6 adalah seperti yang ditunjukkan di bawah ini yang mengikuti pengepakan bit big-endian.

|Sintaks|Jumlah bit|Jenis|Symantec|
---|---|---|---|
|frame_mode|1|Enum|0x0 menandakan intra frame|
|qp |6 |Tidak ditandatangani |Parameter kuantisasi rentang valid 0..63|
|penanda| 1| Konstan| 0=VP61/62, 1=VP60|
|jika (frame_mode == 0) { | 0 | |sama dengan INTRA_FRAME|
|versi |5| Konstan| 6=VP60/61, 7=VP60(Seni Elektronik), 8=VP62|
|versi2 |2| Konstan |0=VP60, 3=VP61/62|
|jalin |1| Boolean |true (1) berarti interlace akan digunakan|
|jika (penanda==1 atau versi2==0) {||||
|offset |16 |Tidak ditandatangani| buffer offset sekunder (byte yang relevan untuk memulai buffer)|
|}||||
|redup_y |8| Tidak ditandatangani| Tinggi makroblok video|
|dim_x |8| Tidak ditandatangani| Lebar makroblok video|
|render_y |8 |Tanpa tanda tangan |Tampilkan tinggi video|
|render_x |8 |Tidak ditandatangani |Tampilkan lebar video|
|}lain{||||
|jika (penanda==1 atau versi2==0) {||||
|offset |16 |Unsigned |Secondary buffer offset (bytes releative to start of buffer)|
|}||||
|}||||

## Referensi

* [Wikipedia VP6](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

