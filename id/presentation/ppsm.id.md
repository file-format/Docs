{
  "date" : "2019-10-11",
  "keywords" :[ "file ppsm", "format file ppsm", "apa itu file ppsm", "file", "contoh ppsm", "ekstensi file ppsm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - File Presentasi PowerPoint Berkemampuan Makro",
  "description":"Pelajari tentang format file PPSM dan API yang dapat membuat dan membuka file PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PPSM?

File dengan ekstensi PPSM mewakili format file Peragaan Slide yang diaktifkan Makro yang dibuat dengan Microsoft PowerPoint 2007 atau lebih tinggi. Format file serupa lainnya adalah [PPTM](/id/presentation/pptm/) yang berbeda dalam pembukaan dengan Microsoft PowerPoint dalam format yang dapat diedit alih-alih dijalankan sebagai Peragaan Slide. Saat dijalankan sebagai peragaan slide, file PPSM menampilkan slide presentasi dengan konten utuh dalam peragaan slide dan dalam mode hanya-baca secara default. File PPSM masih bisa diedit di Microsoft PowerPoint dengan membukanya di PowerPoint.

## Format File ##

Format file PPSM diperkenalkan dengan PowerPoint 2007 dan didasarkan pada format file OpenXML yang menggunakan kombinasi XML dan [ZIP](/id/compression/zip/) untuk menyimpan kontennya. File yang dihasilkan dengan format file Office Open XML adalah kumpulan file XML bersama dengan file lain yang menyediakan tautan antara semua file penyusunnya. Koleksi ini sebenarnya adalah arsip terkompresi yang dapat diekstraksi untuk melihat isinya. Untuk melakukannya, cukup ganti nama ekstensi file PPSM dengan zip dan ekstrak untuk mengamati isinya.

Bagian berikut menjelaskan masing-masing bagian ini.

### [Content_Types].xml ###

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstrak. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini. Berikut adalah tipe konten untuk bagian slide:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jika bagian baru perlu ditambahkan ke paket, hal itu dapat dilakukan dengan menambahkan bagian baru dan memperbarui hubungan apa pun di dalam file .rels. Perlu diingat bahwa untuk perubahan tersebut, Content_Types.xml juga harus diperbarui.

### \_rels (Folder) ###

Hubungan antara bagian lain dan sumber daya di luar paket dikelola oleh bagian hubungan. Folder Hubungan berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian penting dari file presentasi dimuat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan ke dokumen kantor utama yang terletak sebagai ppt/presentation.xml dan bagian lain dalam docProps sebagai properti inti dan tambahan.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Setiap bagian dari dokumen yang merupakan sumber dari satu atau lebih relasi akan memiliki bagian relasinya sendiri di mana setiap bagian relasi tersebut ditemukan dalam sub-folder \_rels dari bagian tersebut dan diberi nama dengan menambahkan '.rels' ke nama relasi bagian. Bagian konten utama (presentation.xml) memiliki bagian hubungan sendiri (presentation.xml.rels). Ini berisi hubungan ke bagian lain dari konten seperti slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, serta URI untuk tautan eksternal.

#### Hubungan Eksplisit ####

Untuk hubungan eksplisit, sumber daya direferensikan menggunakan atribut Id dari a<Relationship> elemen. Artinya, Id di sumber memetakan langsung ke Id dari item relasi, dengan referensi eksplisit ke target.

Misalnya, slide mungkin berisi hyperlink seperti ini:
```
<a:hlinkClick r:id#"rId2">
```
R:id#"rId2" mereferensikan hubungan berikut dalam bagian hubungan untuk slide (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Relasi Implisit ####

Untuk hubungan implisit, tidak ada referensi langsung ke `<Relationship> id`. Sebaliknya, referensi dipahami.

### folder ppt ###

Ini adalah folder utama yang berisi semua detail tentang isi Presentasi. Secara default, ini memiliki folder berikut:

* \_rels
* tema
* slide
* slideLayout
* slideMaster

dan file xml berikut:

* presentasi.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referensi ##

* [Format File Presentasi OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

