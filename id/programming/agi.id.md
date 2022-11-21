{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AGI - Format File Antarmuka Gateway Asterisk",
  "description":"Pelajari tentang apa itu format file AGI dengan contoh dan API yang dapat membuat dan membuka file AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Apa itu file AGI?

File AGI adalah file skrip yang digunakan oleh sistem telepon sumber terbuka, Asterisk. Ini berisi informasi yang dapat digunakan untuk mengotomatiskan proses dan dialplan Asterisk. Menggunakan file skrip AGI, koneksi dapat dibuat dengan database relasional seperti PostgreSQL atau MySQL. Selain itu, skrip AGI juga dapat digunakan untuk mengakses sumber daya eksternal lainnya. Skrip AGI dapat menyerahkan kendali dialplan ke skrip AGI eksternal, memungkinkan Asterisk untuk melakukan tugas yang kompleks.

## Format File AGI - Informasi Lebih Lanjut

File skrip AGI disimpan sebagai file teks dan dapat dibuka di editor teks apa pun untuk membuat perubahan.

### Pola Standar Komunikasi AGI

Skrip AGI memuat variabel dan nilainya dikirim ke sana oleh Asterisk. Tampilan umum dari variabel-variabel ini adalah sebagai berikut.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Variabel-variabel ini diikuti oleh baris kosong yang dikirimkan oleh Asterisk, yang menunjukkan bahwa skrip AGI dapat mengendalikan dialplan sekarang.

### Bahasa pemrograman untuk File Script AGI

Skrip AGI biasanya dapat ditulis dalam Perl, [PHP](/id/programming/php/), [C](/id/programming/c/), Pascal, atau Bourne Shell.

## Referensi

* [Skrip Asterisk AGI](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

