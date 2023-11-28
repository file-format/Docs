{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CPIO - Format File Arsip Unix CPIO",
  "description":"Belajar mengetahui apa itu file CPIO dan API yang dapat membuat dan membuka file CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Apa itu file CPIO?

File CPIO adalah file arsip yang dibuat dalam format Copy In Copy Out (CPIO) Unix. Ini mirip dengan format file TAR selain itu tidak terkompresi. File CPIO dapat menyimpan file perangkat, tautan simbolik, dan atribut file yang diperluas.

## Format File CPIO

Arsip CPIO dibuat sebagai file biner yang tidak dapat dibaca manusia. Ini menyimpan koleksi file dan direktori. Isi arsip CPIO diidentifikasi dengan informasi metadata seperti nama file, izin, kepemilikan, dan cap waktu. Informasi metadata ini juga disimpan dalam file arsip untuk akses lateral oleh sistem.

## Format Arsip CPIO

File CPIO terdiri dari satu atau lebih file anggota yang digabungkan. Setiap file dalam arsip terdiri dari header opsional diikuti dengan isi file seperti yang disebutkan dalam header. Arsip tersebut berisi header lain di bagian akhir yang dijelaskan oleh file kosong bernama TRAILER!!.

### Jenis Arsip CPIO

Ada dua jenis arsip CPIO. Ini berbeda hanya pada gaya headernya.

* Arsip ASCII - Arsip CPIO ini memiliki header yang dapat dicetak yang menjadi bagian dari arsip CPIO jika arsip itu sendiri terdiri dari file ASCII
* Arsip Biner - Arsip CPIO ini memiliki header biner.

## Bekerja dengan Arsip CPIO

### Bagaimana Cara Membuat Arsip CPIO?

Anda dapat membuat CPIO pada sistem mirip Unix menggunakan perintah **cpio**. Perintah berikut akan menemukan semua file dan direktori di direktori saat ini dan subdirektorinya. Output ini kemudian disalurkan ke perintah cpio yang akan menghasilkan arsip CPIO baru bernama archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Bagaimana Cara Mengekstrak File dari Arsip CPIO?

Perintah berikut mengekstrak file dari arsip yang ada.

```
cpio -id < archive_cpio.cpio
```
Ini akan membaca file archive.cpio dari input standar dan mengekstrak file ke direktori saat ini.


## Referensi

* [CPIO - Oleh Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [Format File CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

