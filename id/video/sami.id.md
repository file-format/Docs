{
"tanggal": "16-05-2023",
  "keywords": [
"file sami",
"apa itu file sami",
"contoh file sami",
"mengajukan",
"ekstensi file sami",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File SAMI - File Pertukaran Subjudul dan Metadata",
  "description":"Pelajari tentang format SAMI dan API yang dapat membuat dan membuka file SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent": "video"
}
},
"mod terakhir": "16-05-2023"
}

## Apa itu file SAMI?

File dengan ekstensi ".sami" biasanya mengacu pada file Subtitle dan Metadata Interchange (SAMI). SAMI adalah format teks yang digunakan untuk menampilkan subtitle atau teks tertutup dalam video. Ini pada awalnya dikembangkan oleh Microsoft untuk Windows Media Player mereka.

File SAMI berisi informasi waktu dan konten teks untuk subtitle atau teks, memungkinkannya untuk disinkronkan dengan pemutaran video. Format ini mendukung opsi pemformatan dasar seperti gaya font, warna, dan posisi subtitle di layar.

File SAMI biasanya berupa file teks biasa dan dapat dibuka serta diedit menggunakan editor teks. Isi file SAMI biasanya mencakup bagian header yang memberikan informasi tentang file tersebut, diikuti dengan entri subjudul individual dengan waktu dan teksnya masing-masing.

Berikut ini contoh tampilan file SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

File SAMI biasanya digunakan bersama dengan pemutar video atau pemutar media yang mendukung tampilan subtitle, seperti Windows Media Player atau VLC Media Player. Pemutar membaca file SAMI dan menyinkronkan subtitle dengan konten video, memungkinkan pemirsa membaca teks sambil menonton video.

## Tag HTML yang didukung

File SAMI (Subtitles And Metadata Interchange) mendukung serangkaian tag mirip HTML untuk memformat dan menata subtitle. Berikut beberapa tag umum yang didukung oleh SAMI:

- ``<SAMI> :`` Elemen root yang merangkum seluruh file SAMI.
- ``<HEAD> :`` Berisi informasi header untuk file SAMI.
<html>- ``<TITLE> :`` Menentukan judul file SAMI. </html>
- ``<BODY> :`` Melampirkan entri subtitle dan informasi waktunya.
- ``<SYNC> :`` Mewakili titik sinkronisasi untuk entri subtitle. Ini menentukan waktu di mana subtitle harus ditampilkan.
- ``<P> :`` Melampirkan konten teks sebenarnya dari subtitle. Biasanya digunakan dalam a<SYNC> memblokir.
<html>- `` <FONT>:`` Mendefinisikan properti font untuk teks terlampir. Atribut seperti Warna, Wajah, Ukuran, dan Gaya dapat digunakan untuk mengubah tampilan font.</font>
- ``<BR> :`` Menyisipkan jeda baris dalam subtitle.
<html>- `` <B>:`` Menampilkan teks terlampir dalam huruf tebal.</b>
<html>- `` <I>:`` Menampilkan teks terlampir dalam huruf miring.</i>
<html>- `` <U>:`` Menampilkan teks terlampir yang digarisbawahi.</u>
- ``<C> :`` Menentukan posisi atau perataan teks subtitle pada layar. Ini mendukung atribut seperti Tengah, Tengah, Kiri, Kanan, Atas, Bawah, dan kombinasinya.
- ``<LANG> :`` Menentukan kode bahasa untuk teks subtitle. Ini membantu dalam mengidentifikasi bahasa subtitle.

Ini adalah beberapa tag dasar yang didukung oleh file SAMI. Penting untuk dicatat bahwa SAMI tidak mendukung keseluruhan tag dan atribut HTML. Tag yang didukung terutama berfokus pada gaya dan posisi subjudul daripada menyediakan penataan dokumen atau interaktivitas yang ekstensif.

## Referensi
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

