{
  "date" : "2021-07-29",
  "keywords" :[ "file pes", "format file pes", "apa itu file pes", "file", "contoh pes", "ekstensi file pes", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PES - Format Sulaman Brother PE",
  "description":"Pelajari tentang format file PES dan API yang dapat membuat dan membuka file PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Apa itu file Sulaman PES?

File bordir PES adalah file desain yang berisi instruksi untuk mesin bordir/jahit. Ini dikembangkan oleh Brother Industries untuk mesin bordir mereka tetapi kemudian diformalkan sebagai format file umum. File PES digunakan oleh mesin jahit untuk membaca petunjuk menjahit pola pada kain. File-file ini melayani dua tujuan; pertama memberikan informasi desain untuk aplikasi PE-Design yang dikembangkan oleh Brother Industries dan kedua, memberikan nama desain, warna, dan kode mesin bordir seperti "stop", "jump", dan "trim".

## Format File PES - Informasi Lebih Lanjut

File PES disimpan ke disk dalam format file biner. Ini berisi beberapa bagian yang menyimpan informasi menjahit menggunakan metode yang telah ditentukan. Format file PES adalah sebagai berikut.

* Data Versi - Memberikan informasi versi dan dapat berupa nilai `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC Seek Value - Integer little-endian 4 byte segera mengikuti data versi dan mewakili nilai pencarian untuk bagian PEC yang berisi informasi detail desain
* Bagian PSE - Berisi informasi desain yang relevan dengan Brother PE-Design dan mungkin aplikasi menjahit lainnya
* Bagian PCE - Dapat di mana saja di file PSE tetapi direferensikan oleh PEC Seek Value.

## Jenis Mesin Jahit menggunakan File PES

File PES terutama dibuat oleh Perangkat Lunak Desain-PE yang digunakan dengan mesin jahit Brother. Beberapa mesin lain yang mungkin mendukung file PES termasuk mesin bordir rumah Babylock dan Bernina.

## Bagaimana Cara Mengonversi File PSE?

Aplikasi software PE-Design dapat [mengonversi file PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) ke format lain seperti .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd, atau .xxx. Ini dapat dilakukan menggunakan aplikasi PE-Design dengan membuka file dan memilih format Konversi.

## Referensi

* [Desain PE - Manual Instruksi](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

