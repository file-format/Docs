{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file _XLSX dan API yang dapat membuat dan membuka file _XLSX.",
  "title" :"Apa itu file _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Apa itu file _XLSX?

File dengan ekstensi .\_xlsx sebenarnya adalah file [XLSX](/id/spreadsheet/xlsx/) yang diganti namanya oleh beberapa aplikasi lain. Hal ini dapat terjadi dalam kasus tertentu ketika nama file berisi . di akhir nama file. File \_XLSX dapat dibuka di Microsoft Excel mirip dengan file XLSX dengan mengganti namanya menjadi ekstensi .xlsx.

## Format File _XLSX - Informasi lebih lanjut

File _XLSX tidak berbeda dengan file XLSX dan menggunakan standar Open XML yang diadopsi oleh Microsoft pada tahun 2000. Sebelum XLSX, [XLS](/id/spreadsheet/xls/) adalah format file utama yang digunakan untuk bekerja dengan spreadsheet Excel untuk menyimpan dokumen dalam format biner. Format file berbasis XML baru ini hadir dengan keunggulan seperti ukuran file kecil, ketahanan terhadap kerusakan file, dan representasi gambar yang diformat dengan baik. Format file berbasis XML baru ini menjadi bagian dari Office 2007 dan dilakukan di versi baru Microsoft juga.

## \_Spesifikasi Format Berkas XLSX

Karena file \_XLSX adalah file XLSX yang diubah namanya, ia memiliki spesifikasi yang sama dengan file aslinya. Ini hanyalah file arsip yang didasarkan pada format file arsip [ZIP](/id/compression/zip/). Jika Anda ingin melihat isi arsip ini, cukup ganti nama file menjadi ekstensi .zip dan ekstrak untuk melihat file penyusun buku kerja Excel ini. Buku kerja kosong, saat diekstrak ke filenya, memiliki file dan folder konstituen berikut.

### [Content_Types].xml

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstraksi. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini.

### \_rels (Folder)

Ini adalah folder Hubungan yang berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian penting dari file Xlsx terdapat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan ke dokumen kantor utama yang terletak sebagai xl/workbook.xml dan bagian lain dalam docProps sebagai properti inti dan tambahan.

### docProps

Folder ini berisi properti dokumen secara keseluruhan. Ini termasuk satu set properti inti, satu set properti yang diperluas atau khusus aplikasi dan pratinjau thumbnail dokumen. Buku kerja kosong memiliki dua file di folder ini yaitu app.xml dan core.xml. core.xml berisi informasi seperti penulis, tanggal dibuat dan disimpan, dan dimodifikasi. App.xml berisi informasi tentang konten file.

### xl (Map)

Ini adalah folder utama yang berisi semua detail tentang isi buku kerja. Secara default, ini memiliki folder berikut:

* \_rels
* tema
* lembar kerja

dan file xml berikut:

* style.xml
* buku kerja.xml

## Referensi

* [MS-XLSX - Format File .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

