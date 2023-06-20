{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "file", "format", "extension", "API", "AutoCAD Sheet Set" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - File Kumpulan Lembar AutoCAD",
  "description" :"Pelajari tentang file .dst dan API yang dapat membuat dan membuka file DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Apa itu file DST?

File DST adalah file AutoCAD yang berisi asosiasi dan informasi untuk menentukan kumpulan lembar. Ini disimpan dalam folder penyimpanan set lembar default, AutoCAD Sheet Sets. File DST tidak berisi tata letak gambar yang sebenarnya tetapi merujuk ke ini dari file [DWG](/id/cad/dwg/) dan [DWT](/id/cad/dwt/) yang dipilih yang terkait dengan set sheet ini. Di lingkungan jaringan, semua anggota tim harus memiliki akses jaringan ke file terkait ini. File DST disimpan ke disk dalam format file [XML](/id/web/xml/).

## Format File DST - Informasi Lebih Lanjut

File DST dibuat dengan alat AutoDesk Sheet Set Manager (SSM). Saat file diakses oleh seseorang dalam tim, file DST dibuka sebentar lalu disimpan kembali dengan informasi yang diperbarui. Akses simultan ke file DST yang sama dikelola oleh alat SSM yang menampilkan ikon kunci saat file sedang diakses.

Pada waktu tertentu, status sheet dapat berada di salah satu status berikut.

* Lembar tersedia untuk diedit.
* Lembar terkunci.
* Lembar hilang atau ditemukan di lokasi folder yang tidak terduga.

## Referensi

* [Tentang penggunaan DST Sheet Sets](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Pelajari tentang Kumpulan Lembar](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Menguasai Set Lembar AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

