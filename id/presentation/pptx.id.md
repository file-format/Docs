{
  "date" : "2019-12-13",
  "keywords" :[ "file pptx", "format file pptx", "apa itu file pptx", "file", "contoh pptx", "ekstensi file pptx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PPTX dan API yang dapat membuat dan membuka file PPTX.",
  "title" :"PPTX - Format Berkas Presentasi PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PPTX?

File dengan ekstensi PPTX adalah file presentasi yang dibuat dengan aplikasi Microsoft PowerPoint yang populer. Berbeda dengan versi sebelumnya dari format file presentasi PPT yang biner, format PPTX didasarkan pada format file presentasi terbuka XML Microsoft PowerPoint. File presentasi adalah kumpulan slide di mana setiap slide dapat terdiri dari teks, gambar, format, animasi, dan media lainnya. Slide ini disajikan kepada audiens dalam bentuk tayangan slide dengan pengaturan presentasi khusus.

## Sejarah Singkat

Format file PPTX diperkenalkan pada tahun 2007 dan menggunakan standar Open XML yang diadaptasi oleh Microsoft pada tahun 2000. Sebelum PPTX, format file yang umum digunakan adalah PPT yang merupakan format file biner murni. Jenis file baru telah menambahkan keunggulan ukuran file kecil, lebih sedikit perubahan korupsi dan representasi gambar yang diformat dengan baik. Pada awal tahun 2000, Microsoft memutuskan untuk melakukan perubahan untuk mengakomodasi standar **Office Open XML**. Pada tahun 2007, format file baru ini menjadi bagian dari Office 2007 dan dijalankan di versi baru Microsoft Office juga.

## Spesifikasi Format File PPTX

File yang dihasilkan dengan format file Office Open XML adalah kumpulan file XML bersama dengan file lain yang menyediakan tautan antara semua file penyusunnya. Koleksi ini sebenarnya adalah arsip terkompresi yang dapat diekstraksi untuk melihat isinya. Untuk melakukannya, cukup ganti nama ekstensi file PPTX dengan zip dan ekstrak untuk mengamati kontennya (Lihat [spesifikasi format file PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) oleh Microsoft).

Bagian berikut menjelaskan masing-masing bagian ini.

### [Content_Types].xml

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstrak. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini. Berikut adalah tipe konten untuk bagian slide:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Jika bagian baru perlu ditambahkan ke paket, hal itu dapat dilakukan dengan menambahkan bagian baru dan memperbarui hubungan apa pun di dalam file .rels. Perlu diingat bahwa untuk perubahan tersebut, Content_Types.xml juga harus diperbarui.

### \_rels (Folder) ###

Hubungan antara bagian lain dan sumber daya di luar paket dikelola oleh bagian hubungan. Folder Hubungan berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian utama file PPTX terdapat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan ke dokumen kantor utama yang terletak sebagai ppt/presentation.xml dan bagian lain dalam docProps sebagai properti inti dan tambahan.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
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

* [[MS-PPTX] - Format File PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

