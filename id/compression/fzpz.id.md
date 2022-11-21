{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File FZPZ - File Bagian Fritzing",
  "description":"Pelajari tentang apa itu file FZPZ dan API yang dapat membuat dan membuka file FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Apa itu file FZPZ?

File FZPZ adalah komponen/bagian yang digunakan dalam desain sirkuit elektronik yang dibuat dengan aplikasi desain dan prototipe sirkuit **Fritzing**. Ini adalah arsip terkompresi yang berisi file [FZP](/id/cad/fzp/) dan empat gambar [SVG](/id/image/svg/) yang menjelaskan keseluruhan bagian dalam Fritzing. Keuntungan menggunakan file ini adalah pengguna dapat membagikan file FZPZ mereka dengan masing-masing file dari sudut pandang yang dapat digunakan kembali. Berbagi bagian FZPZ membantu dalam mengintegrasikan bagian sirkuit untuk membuat desain PCB yang lebih besar dengan cepat.

## Format File FZPZ - Informasi Lebih Lanjut

File FZPZ disimpan ke disk sebagai arsip [ZIP](/id/compression/zip/) terkompresi. Anda dapat mengganti nama ekstensi dari .fzpz menjadi .zip dan menggunakan utilitas dekompresi standar seperti WinZIP untuk mengekstrak file dari arsip.

### Informasi Struktur File FZPZ

Seperti disebutkan, file FZPZ adalah file arsip yang berisi banyak file untuk representasi bagian yang digunakan dalam papan sirkuit tercetak. FZPZ berisi file-file berikut:

* `Empat file SVG` - yang mewakili gambar papan tempat memotong roti, skema, PCB, dan ikon bagian
* `FZP file` - File XML yang berisi informasi tentang properti bagian, konektor, dan bus

File-file tersebut biasanya diberi nama sebagai berikut.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Referensi ##

* [Bagian baru dengan ekstensi fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

