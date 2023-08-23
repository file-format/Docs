{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "file", "ekstensi", "format file", "Excel Open XML Macro", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file XLTM dan API yang dapat membuat dan membukanya.",
  "title" :"Apa itu file XLTM?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file XLTM?

Ekstensi file XLTM mewakili file yang dihasilkan oleh Microsoft Excel sebagai file template yang mendukung Makro. File XLTM mirip dengan [XLTX](/id/spreadsheet/xltx/) dalam struktur selain itu nanti tidak mendukung pembuatan file template dengan makro. File template semacam itu digunakan untuk membuat dan mengatur tata letak, pemformatan, dan pengaturan lainnya bersama dengan makro untuk memfasilitasi pembuatan file XLSX yang serupa.

## Sejarah Singkat ##

Pada awal tahun 2000, Microsoft memutuskan untuk melakukan perubahan untuk mengakomodasi standar **Office Open XML**. Dokumen, dari berbagai jenis, di bawah Standar baru ini diidentifikasi dengan menambahkan "X" dalam ekstensinya, dengan "X" untuk XML. Pada tahun 2007, format file baru ini menjadi bagian dari Office 2007 dan dijalankan di versi baru Microsoft Office juga. Jenis file baru telah menambahkan keunggulan ukuran file kecil, lebih sedikit perubahan korupsi dan representasi gambar yang diformat dengan baik.

## Spesifikasi Format File XLTM ##

File XLTM didasarkan pada format file Office OpenXML dan menggunakan XML dan [ZIP](/id/compression/zip/) untuk mengurangi ukuran file. Ini dapat dibuka dengan Microsoft Excel dengan mengklik dua kali file tersebut. Organisasi file dalam format file XLTM dapat diamati dengan mengganti nama file menjadi ZIP dan kemudian mengekstrak isinya ke disk.

### [Content_Types].xml ###

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstrak. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini.

### \_rels (Folder) ###

Ini adalah folder Hubungan yang berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian utama file Xltx terdapat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan dengan dokumen kantor utama yang terletak sebagai xl/workbook.xml dan bagian lain dalam docProps sebagai inti dan properti yang diperluas.

### docProps ###

Folder ini berisi properti dokumen secara keseluruhan. Ini termasuk satu set properti inti, satu set properti yang diperluas atau khusus aplikasi dan pratinjau thumbnail dokumen. Buku kerja kosong memiliki dua file di folder ini yaitu app.xml dan core.xml. core.xml berisi informasi seperti penulis, tanggal dibuat dan disimpan, dan dimodifikasi. App.xml berisi informasi tentang konten file.

### xl (Folder) ###

Ini adalah folder utama yang berisi semua detail tentang isi buku kerja. Secara default, ini memiliki folder berikut:

* \_rels
* tema
* lembar kerja

dan file xml berikut:

* style.xml
* buku kerja.xml

## Referensi ##

* [Format File MS-XLSX](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

