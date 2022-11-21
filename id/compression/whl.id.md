{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File WHL - File Paket Roda Python",
  "description":"Pelajari tentang format file WHL dan API yang dapat membuat dan membuka file WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Apa itu file WHL?

File WHL (Roda) adalah file paket distribusi yang disimpan dalam format roda Python. Ini adalah instalasi format standar distribusi Python dan berisi semua file dan metadata yang diperlukan untuk instalasi. File WHL juga berisi informasi tentang versi dan platform Python yang didukung oleh file roda ini. Mirip dengan file setup [MSI](/id/executable/msi/), format file WHL adalah format siap-instal yang memungkinkan menjalankan paket instalasi tanpa membangun distribusi sumber.

## Format File WHL

Format file WHL adalah arsip [ZIP](/id/compression/zip/) (.zip) yang berisi semua file instalasi dan metadata yang diperlukan oleh installer untuk instalasi paket. File WHL ini dapat diekstraksi menggunakan opsi unzip atau aplikasi perangkat lunak dekompresi standar seperti WinZIP dan WinRAR.

### Konvensi Nama File WHL

File WHL diberi nama sesuai konvensi berikut.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Contoh nama file WHL adalah sebagai berikut.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `kriptografi` adalah nama paket.
* `2.9.2` adalah versi paket kriptografi. Versi adalah string yang sesuai dengan PEP 440 seperti 2.9.2, 3.4, atau 3.9.0.a3.
* `cp35` adalah tag Python dan menunjukkan implementasi dan versi Python yang diminta roda.
* `abi3` adalah tag ABI. ABI adalah singkatan dari antarmuka biner aplikasi.
* `macosx_10_9_x86_64` adalah tag platform, yang kebetulan cukup banyak.

## Referensi

* [Apa Itu Python Wheels dan Mengapa Anda Harus Peduli?](https://realpython.com/python-wheels/)
* [Roda Python](https://pypi.org/project/wheel/)

