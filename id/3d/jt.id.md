{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "file", "ekstensi", "format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file JT dan API yang dapat membuat dan membuka file JT.",
  "title" :"JT - Format File Jupiter Tessellation",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file JT?

**JT** (Jupiter Tessellation) adalah format data 3D berstandar ISO yang efisien, berfokus pada industri, dan fleksibel yang dikembangkan oleh Siemens PLM Software. Domain CAD mekanik dari Aerospace, industri otomotif, dan Alat Berat menggunakan JT sebagai format visualisasi 3D paling terkemuka.

Format JT adalah grafik adegan yang mendukung atribut dan node yang spesifik untuk CAD. Teknik kompresi canggih digunakan untuk menyimpan data segi (segitiga). Format ini disusun untuk mendukung atribut visual, informasi produk dan manufaktur (PMI), dan Metadata. Ada dukungan yang baik untuk streaming konten yang tidak sinkron. Dalam industri mekanik berat, para profesional menggunakan file JT dalam solusi CAD dan program perangkat lunak manajemen siklus hidup produk (PLM) untuk memeriksa geometri barang yang rumit.

Karena JT mendukung hampir semua format CAD 3D penting, perakitannya dapat menangani berbagai kombinasi yang dikenal sebagai "multi-CAD". Rakitan multi-CAD ini selalu dikelola dengan baik dan mutakhir karena sinkronisasi antara file deskripsi produk CAD asli dengan file JT terkait terjadi secara otomatis. File JT awalnya ringan, sehingga dianggap cocok untuk kolaborasi internet. Perusahaan Berkolaborasi melalui pengiriman visualisasi 3D melalui media jauh lebih mudah dibandingkan dengan file CAD asli yang "berat". Selain itu, file JT memastikan banyak fitur keamanan yang membuat pembagian kekayaan intelektual lebih aman.

## Sejarah Singkat Format File JT

Engineering Animation, Inc. dan Hewlett Packard adalah perancang asli JT, yang mengembangkan format tersebut sebagai perangkat Direct Model. Setelah EAI diakuisisi oleh UGS Corp. JT menjadi bagian dari suite UGS. Awal tahun 2007, UGS mengumumkan JT sebagai format 3D master mereka. Pada tahun yang sama, Siemens AG membeli UGS dan menjadi Perangkat Lunak PLM Siemens. Siemens menggunakan JT sebagai format interoperabilitas umum dan format arsip data. Pada tahun 2009, ISO menerima spesifikasi JT untuk publikasi sebagai ISO Publicly Available Specification (PAS). Pada pertengahan tahun 2010, ProSTEP iViP mengumumkan bahwa pada tingkat industri, JT dan STEP AP 242 XML dapat digunakan bersama untuk mencapai keuntungan maksimum dalam data. skenario pertukaran. Pada tahun 2012, JT secara resmi dinyatakan sebagai format visualisasi 3D berstandar ISO (ISO 14306:2012 (ISO JT V1)).

## Format File JT ##

Semua objek dalam format JT direpresentasikan melalui pengidentifikasi objek dan referensi antar objek ditangani melalui pengidentifikasi objek yang direferensikan. Integritas referensi objek ini dapat dipertahankan melalui penunjuk yang tidak berputar/berputar.

File JT disusun sebagai rangkaian blok dan blok Header selalu merupakan blok data pertama dalam file. Serangkaian segmen data dan segmen TOC segera mengikuti blok header. Satu segmen Data (6 Segmen LSG) memiliki file JT yang sesuai referensi selalu ada. Segmen TOC berisi informasi lokasi dari semua Segmen Data lainnya dari file tersebut.

{{< figure src="../JT-1.png" alt="Format File JT" >}}

### Kepala Berkas ###

File Header adalah blok pertama dalam hierarki data file JT. Informasi pembuatan versi dan informasi lokasi TOC terlampir di dalam header yang memfasilitasi loader dalam membaca file. Isi header file disusun sebagai berikut.

### Segmen TOC ###

Segmen TOC harus ada di dalam file dan berisi informasi identifikasi dan lokasi dari semua segmen data lainnya. Lokasi sebenarnya dari Segmen TOC ditentukan oleh bidang TOC Offset dari header file. Setiap Segmen Data yang dapat dialamatkan secara individual diwakili oleh entri TOC di segmen TOC.

### Segmen Data ###

File JT menentukan semua data yang disimpan dalam Segmen Data. Beberapa Segmen Data dapat memampatkan semua byte data informasi yang tersisa di dalam segmen tersebut. Segmen data memiliki struktur berikut:

![alt text](../JT-2.png "JT Data Segment")

Tabel berikut menjelaskan berbagai jenis segmen data:

|Nama|Deskripsi
---|---|
|LSG segment|Terdiri dari kumpulan objek yang terhubung melalui referensi terarah untuk membentuk LSG (directed acyclic graph structure)
|Bentuk LOD segmen|berisi data yang menentukan untuk bentuk geometris (misalnya simpul, normal, poligon, dll)
|Segmen JT B-Rep|Memiliki elemen untuk data yang mewakili batas geometris yang tepat untuk bagian individu dalam format JT B-Rep.
|XT B-Rep segmen|Memiliki elemen untuk data untuk mewakili batas geometris yang tepat untuk bagian individu dalam format representasi batas
|Segmen wireframe|Data merepresentasikan wireframe 3D yang presisi untuk bagian tertentu yang ditentukan oleh elemen yang terdapat di segmen ini.
|Segmen Data Meta|Memungkinkan untuk menyimpan metadata di segmen yang dapat dialamatkan berbeda.
|Segmen JT ULP|Memiliki elemen untuk data yang mewakili batas geometris semi-presisi untuk bagian individu dalam format JT ULP.
|JT LWPA segment|Berisi elemen yang menentukan data analitik untuk bagian tertentu. LWPA menyertakan kumpulan permukaan analitik dalam definisi b-rep dari bagian tersebut.

## Kompresi ##

Persyaratan transmisi dan penyimpanan model 3D lebih menuntut, sehingga file JT dapat memanfaatkan kompresi. Model data JT dapat terdiri dari file yang berbeda menggunakan teknik kompresi yang berbeda tetapi proses kompresi transparan untuk pengguna data JT.

Sejauh ini, JT Open Toolkit (sebagai standar) dan kompresi lanjutan adalah dua teknik kompresi yang digunakan oleh file JT. JT Open Toolkit menggunakan algoritme kompresi lossless yang mudah, sedangkan kompresi lanjutan menggunakan teknik kompresi khusus domain yang lebih halus yang mengarah ke kompresi geometri lossy. Aplikasi klien lebih menyukai kompresi tingkat lanjut daripada menggunakan kompresi standar, karena kompresi tingkat lanjut menghasilkan rasio kompresi yang cukup tinggi. Kompatibilitas mundur dengan aplikasi tampilan file JT biasa dipertahankan melalui penyediaan kompresi standar. Bentuk kompresi harus kompatibel dengan versi format file JT yang dapat dilihat saat file JT dibuka menggunakan editor teks dan dilampirkan dalam informasi header ASCII.

## Referensi ##

* [Referensi Format File JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (format visualisasi)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

