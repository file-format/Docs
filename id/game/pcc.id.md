{
  "date" : "2021-09-08",
  "keywords" :[ "file pcc", "format file pcc", "apa itu file pcc", "file", "contoh pcc", "ekstensi file pcc", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PCC Mass Effect dan API yang dapat membuat dan membuka file PCC.",
  "title" :"PCC - File Paket Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Apa itu file PCC?

File dengan .pcc adalah file [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) yang berisi data game untuk mengubah konten game seperti model, tekstur, dan kamar. Mass Effect 2 dan 3 adalah game penembak pertama berdasarkan mesin game Unreal Engine 3. Gim ini awalnya dikembangkan oleh [Bioware](https://www.bioware.com/about/) yang menyimpan sebagian besar sumber daya gim dalam format file PCC milik mereka. Bioware diakuisisi oleh Electronic Arts, penerbit hiburan interaktif global terkemuka.

## Format File PCC - Informasi Lebih Lanjut

File PCC berisi struktur terkompresi dan/atau tidak terkompresi yang berkontribusi pada organisasi file secara keseluruhan.

### Struktur PCC Terkompresi

File PCC terkompresi terdiri dari tabel dan data yang disegmentasi menjadi potongan-potongan. Setiap potongan berisi sejumlah variabel blok terkompresi.

* `Chunks Header` - Header umum 16 byte, berisi informasi tentang potongan.
* `Chunk Header` - Header 16 byte yang berisi informasi tentang data terkompresi mentah yang terdapat dalam bentuk blok.

### Struktur PCC Tidak Terkompresi

File PCC yang tidak terkompresi dibagi menjadi lima bagian berikut.

* `Header` - berisi informasi dasar tentang struktur file PCC.
* `Tabel Nama` - berisi nama yang ditemukan di dalam paket termasuk kelas impor, ekspor, dan properti ekspor.
* `Import Table` - berisi semua kelas dan objek yang diimpor oleh PCC.
* `Export Table` - berisi semua objek yang disimpan dalam paket. Setiap ekspor dapat bervariasi dalam ukuran.

## Referensi

* [Me3Explorer - Format File PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Game Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

