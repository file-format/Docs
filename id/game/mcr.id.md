{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Pelajari tentang format file MCR dan API yang dapat membuat dan membuka file MCR.",
  "title": "MCR - Format File Wilayah Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-idr"
}
},
  "lastmod": "2022-12-14"
}

## Apa itu file MCR?

Format file Minecraft MCR adalah format data yang digunakan oleh Minecraft untuk menyimpan potongan medan Dunia Minecraft. Ini didasarkan pada format NBT (Named Binary Tag), yang dikembangkan oleh pengembang mesin permainan sumber terbuka populer, Minecraft Forge. Jenis file MCR diperkenalkan pada awalnya dan kemudian digantikan oleh [MCA file format](/game/mca/).

## Format File MCR

Format file MCR disusun sebagai serangkaian tag biner bernama, yang masing-masing berisi tipe data tertentu. Tag tingkat atas adalah tag Level, yang berisi semua data untuk satu level permainan. Di dalam tag Level, ada beberapa tag bernama lain yang menyimpan berbagai jenis data, seperti tag Data, yang menyimpan informasi tentang dunia game, dan tag Entitas dan TileEntities, yang menyimpan data tentang masing-masing objek permainan dan entitas ubin di dunia.

## Apa yang ada di dalam Format File MCR?

Dalam format file Minecraft MCR, suatu wilayah adalah area blok dunia game berukuran 32x32. Format MCR membagi dunia game menjadi beberapa wilayah untuk mengelola data dengan lebih efisien dan memungkinkan pemuatan dan penyimpanan level game lebih cepat. Setiap wilayah disimpan dalam file terpisah, dan format file MCR menggunakan sistem koordinat untuk mengidentifikasi posisi setiap wilayah dalam dunia game. Koordinat suatu wilayah ditentukan oleh blok koordinat pojok kiri bawah wilayah tersebut. Misalnya, suatu wilayah dengan koordinat (-1,0) akan terletak satu wilayah di sebelah kiri dan nol wilayah di bawah asal dunia game.

## Spesifikasi Format File MCR

Spesifikasi format file MCR tersedia untuk umum. Spesifikasi format NBT yang menjadi dasar format MCR tersedia di situs web Minecraft Forge. Selain itu, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) juga memiliki informasi mendetail tentang format file MCR, termasuk strukturnya dan berbagai tipe data yang didukungnya.

### Data Terkompresi dalam File MCR

Format file Minecraft MCR mendukung kompresi. Format file MCR didasarkan pada [NBT format](https://minecraft.fandom.com/wiki/NBT_format) yang memungkinkan data disimpan dalam bentuk terkompresi. Hal ini membantu mengurangi ukuran file MCR dan membuatnya lebih efisien untuk ditransfer dan disimpan. Ini adalah fitur penting dari format file MCR karena memungkinkan pemain berbagi data medan Minecraft World yang besar dengan orang lain.

## Referensi

* [Editor Dunia untuk Minecraft](https://www.mcedit.net/)

* [Tentang Minecraft](https://www.minecraft.net/)

* [Format File Wilayah](https://minecraft.fandom.com/wiki/Region_file_format)

* [Format NBT](https://minecraft.fandom.com/wiki/NBT_format)


