{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - File Kabinet Windows",
  "description":"Pelajari tentang format file CAB dan API yang dapat membuat dan membuka file CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu file CAB? ##

File dengan ekstensi .cab milik file kabinet windows yang termasuk dalam kategori file sistem. Ini adalah file yang disimpan dalam format file arsip dalam versi Microsoft Windows yang mendukung algoritme data terkompresi, seperti [LZX](/id/compression/lzx/), Quantum, dan [ZIP](/id/compression/zip/ ). File ini sangat penting digunakan saat pengguna atau pengembang ingin memuat dan berbagi data dan file instalasi perangkat lunak. Fitur kompresi data lossless dan sertifikasi digital yang disertakan dalam file ini menjadikan file ini sempurna untuk menyimpan dan berbagi file semacam itu. Ini mendukung penginstal Microsoft yang berbeda seperti Penginstal Perangkat, SetUp API, dan AdvPak.

## Sejarah Singkat ##

File CAB adalah jenis file kompresi data yang dikembangkan oleh Microsoft. Awalnya disebut "Berlian", tetapi kemudian dikenal sebagai file CAB, kependekan dari kata "Kabinet".

## Spesifikasi Teknis ##

File CAB biasanya dapat berisi maksimal 65535 folder, yang masing-masing dapat berisi maksimal 65536 file. Mekanisme penyimpanan file CAB hemat ruang dan waktu karena menyimpan setiap folder sebagai blok terkompresi alih-alih mengompresi dan menyimpan setiap file secara terpisah. Folder kosong tidak dapat disimpan di folder arsip CAB. File CAB pertama kali dikembangkan oleh Microsoft dan digunakan di berbagai installer, seperti InstallShield dengan format yang sedikit berbeda. File CAB umumnya terhubung ke program yang mengekstraksi sendiri. File Microsoft CAB mudah dikenali karena penanda uniknya yang membantu mengidentifikasi format. Penanda unik untuk semua file Microsoft CAB adalah awalan empat kata, MSCF. Melihat kode ini, pengguna dapat dengan mudah membedakan file Microsoft CAB dari file lain dan menggunakannya sesuai dengan kompresor atau versi. File dapat dikompresi dengan lebih banyak data instalasi perangkat lunak, atau data yang ada dapat didekompresi menggunakan perangkat lunak yang tepat.


## Contoh CAB ##

Contoh berikut mengilustrasikan hubungan antara file dan folder dalam struktur file CAB:

{{< figure src="../cab.png" alt="Format File CAB" >}}

## Referensi ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
