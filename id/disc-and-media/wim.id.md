{
  "date" : "2021-08-11",
  "keywords" :[ "file wim", "format file wim", "apa itu file wim", "file", "contoh wim", "ekstensi file wim", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file WIM dan API yang dapat membuat dan membuka file WIM.",
  "title" :"WIM - File Format Pencitraan Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Apa itu file WIM?
File dengan ekstensi .wim pertama kali terlihat di Windows Vista. WIM milik format pencitraan berbasis file yang biasanya diperkenalkan di Microsoft Windows Vista. Ini memungkinkan gambar disk tunggal untuk disebarkan ke berbagai platform komputer. File WIM digunakan untuk mengelola file seperti pembaruan, driver, dan komponen tanpa mem-boot ulang citra sistem operasi. File AQ WIM berisi sekumpulan file dan metadata terkait yang sangat mirip dengan format file disk lainnya.

## format file WIM
Format file WIM tidak seperti format berbasis sektor seperti VHD atau IS, sebenarnya ini berbasis file yang artinya unit dasar informasi dalam WIM adalah file. Manfaat dasar menjadi berbasis file adalah bahwa penyimpanan file tunggal yang direferensikan beberapa kali dalam pohon sistem file dan kemandirian perangkat keras. Ini mengurangi biaya pembukaan dan penutupan berbagai file secara individual, karena file disimpan di dalam satu WIM mengajukan. File WIM dapat menyimpan banyak gambar disk, yang direferensikan dengan nama uniknya atau dengan indeks numeriknya.
### Dukungan untuk algoritma kompresi
WIM mendukung rangkaian algoritme kompresi berikut dalam kecepatan menurun dan rasio menaik:
-XPRESS
- LZX
- LZMS
- Padat-kompresi.
Tiga keluarga pertama berbasis LZ77 sementara kompresi Solid diperkenalkan bersama dengan LZMS di WIMGAPI Windows 8 dan DISM Windows 8.1.
### Alat untuk format file WIM
Alat berikut biasanya mendukung format file WIM:

- **ImageX**: Alat baris perintah yang digunakan untuk mengedit, membuat, dan menerapkan image disk Windows dalam Format Pencitraan Windows. Bersama dengan WIMGAPI yang relevan, Ini didistribusikan sebagai bagian dari Kit Instalasi Otomatis Windows gratis. Dimulai dengan Windows Vista, Windows Setup menggunakan WAIK API untuk menginstal Windows.
- **DISM**: Alat yang diperkenalkan di Windows 7 dan Windows Server 2008 R2 yang dapat melakukan tugas terkait layanan pada gambar instalasi Windows, baik itu gambar online atau gambar offline di dalam folder atau file WIM. alat ini mampu memasang dan melepas gambar, menambahkan driver perangkat ke gambar offline dan menanyakan driver perangkat yang diinstal dalam gambar offline.
 




## Referensi


* [Format Pencitraan Windows - oleh Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


