{
  "date" : "2019-10-11",
  "keywords" :[ "file potx", "format file potx", "apa itu file potx", "file", "contoh potx", "ekstensi file potx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Templat Presentasi Microsoft PowerPoint",
  "description":"Pelajari tentang format file POTX dan API yang dapat membuat dan membuka file POTX.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file POTX?

File dengan ekstensi .POTX mewakili presentasi template Microsoft PowerPoint yang dibuat dengan Microsoft PowerPoint 2007 ke atas. Format ini dibuat untuk menggantikan format file [POT](/id/presentation/pot/) yang didasarkan pada format file biner dan didukung dengan PowerPoint 97-2003. File yang dihasilkan dapat digunakan untuk membuat presentasi yang memiliki tata letak yang sama dan pengaturan lain yang diperlukan untuk diterapkan ke file baru. Pengaturan ini dapat mencakup gaya, latar belakang, palet warna, font, dan default. File tersebut dibuat untuk membuat file template siap pakai untuk penggunaan resmi.

## Sejarah Singkat ##

Pada awal tahun 2000, Microsoft memutuskan untuk melakukan perubahan untuk mengakomodasi standar **Office Open XML**. Dokumen, dari berbagai jenis, di bawah Standar baru ini diidentifikasi dengan menambahkan "X" dalam ekstensinya, dengan "X" untuk XML. Pada tahun 2007, format file baru ini menjadi bagian dari Office 2007 dan dijalankan di versi baru Microsoft Office juga. Jenis file baru telah menambahkan keunggulan ukuran file kecil, lebih sedikit perubahan korupsi dan representasi gambar yang diformat dengan baik.

## Spesifikasi Format File ##

File yang dihasilkan dengan format file Office Open XML adalah kumpulan file XML bersama dengan file lain yang menyediakan tautan antara semua file penyusunnya. Koleksi ini sebenarnya adalah arsip terkompresi yang dapat diekstraksi untuk melihat isinya. Untuk melakukannya, cukup ganti nama ekstensi file POTX dengan zip dan ekstrak untuk mengamati isinya.

Bagian berikut menjelaskan masing-masing bagian ini.

### [Content_Types].xml ###

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstrak. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini. Berikut adalah tipe konten untuk bagian slide:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jika bagian baru perlu ditambahkan ke paket, hal itu dapat dilakukan dengan menambahkan bagian baru dan memperbarui hubungan apa pun di dalam file .rels. Perlu diingat bahwa untuk perubahan tersebut, Content_Types.xml juga harus diperbarui.

### \_rels (Folder) ###

Hubungan antara bagian lain dan sumber daya di luar paket dikelola oleh bagian hubungan. Folder Hubungan berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian utama file PPTX terdapat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan ke dokumen kantor utama yang terletak sebagai ppt/presentation.xml dan bagian lain dalam docProps sebagai properti inti dan tambahan.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Setiap bagian dari dokumen yang merupakan sumber dari satu atau lebih relasi akan memiliki bagian relasinya sendiri di mana setiap bagian relasi tersebut ditemukan di dalam \_rels sub-folder dari bagian tersebut dan diberi nama dengan menambahkan '.rels' ke nama dari bagian. Bagian konten utama (presentation.xml) memiliki bagian hubungan sendiri (presentation.xml.rels). Ini berisi hubungan ke bagian lain dari konten seperti slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, serta URI untuk tautan eksternal.

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
* slideLayouts
* slideMaster

dan file xml berikut:

* presentasi.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referensi ##

* [[MS-PPTX] - Format File PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

