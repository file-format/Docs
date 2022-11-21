{
  "date" : "2020-03-16",
  "keywords" :[ "Berkas IFC", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file IFC dan API yang dapat membuat dan membuka file IFC.",
  "title" :"Format File IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file IFC?

File dengan ekstensi IFC mengacu pada format file Industry Foundation Classes (IFC) yang menetapkan standar internasional untuk mengimpor dan mengekspor objek bangunan dan propertinya. Format file ini menyediakan interoperabilitas antara aplikasi perangkat lunak yang berbeda. Spesifikasi untuk format file ini dikembangkan dan dikelola oleh buildingSMART International sebagai Standar Datanya. Tujuan akhir dari format file IFC adalah untuk meningkatkan komunikasi, produktivitas, waktu pengiriman, dan kualitas sepanjang siklus hidup bangunan.

Karena standar yang ditetapkan untuk objek umum dalam industri bangunan, ini mengurangi hilangnya informasi selama transmisi dari satu aplikasi ke aplikasi lainnya. IFC dapat menyimpan data untuk geometri, kalkulasi, kuantitas, manajemen fasilitas, penetapan harga, dll. untuk berbagai profesi (arsitek, kelistrikan, HVAC, struktural, medan, dll.).

## Sejarah Singkat ##

Inisiatif IFC diambil pada tahun 1994 oleh Autodesk untuk mendukung pengembangan aplikasi terintegrasi dan termasuk perusahaan seperti Honeywell, Butler Manufacturing, dan AT&T. Pada tahun 1995, keanggotaan dibuka untuk siapa saja dan namanya diubah menjadi International Alliance for Interoperability. Niat nirlaba adalah untuk menerbitkan Kelas Yayasan Industri (IFC) sebagai model produk AEC. Pada tahun 2005, namanya diubah lagi dan buildSMART sekarang mempertahankannya.

## Format File IFC ##

Format file IFC telah mengalami beberapa perubahan di masa lalu untuk mencapai spesifikasi format file v4. Beberapa perubahan minor terjadi dari waktu ke waktu serta yang telah dijadikan bagian dari spesifikasi sebagai Adendum. Berikut adalah daftar berbagai versi spesifikasi file yang telah dipublikasikan sebelumnya.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (Maret 2013) ifcXML2x3 (Juni 2007)
* IFC2x3 (Februari 2006) ifcXML2 untuk IFC2x2 add1 (RC2)
* IFC2x2 Adendum 1 (Juli 2004)ifcXML2 untuk IFC2x2 (RC1)
* IFC 2x2IFC 2x Tambahan 1ifcXML1 untuk IFC2x dan
* Tambahan IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Versi terbaru dari spesifikasi format file IFC selalu tersedia di situs web buildingSMART dan pengembang harus berkonsultasi dengan ini untuk semua jenis aplikasi yang mereka rencanakan untuk dikembangkan. Saat artikel ini ditulis, spesifikasi versi 4 adalah yang terbaru yang tersedia secara online.

### Format File Data IFC ###

Format file IFF mendukung pertukaran data antar aplikasi menggunakan format berbeda seperti yang tercantum di bawah ini:

**IFC:** Ini adalah format pertukaran IFC default dan menggunakan struktur file fisik STEP menurut ISO 10303-21. Format file ini memiliki ekstensi file .ifc dan merupakan format IFC yang paling banyak digunakan.

**IFC-XML:** Ini adalah versi format file XML dari IFC yang dapat dibuat langsung oleh aplikasi pengirim sesuai struktur ISO 10303-28, juga disebut STEP-XML. Format file IFC-XML dianggap cocok untuk interoperabilitas di antara alat XML. Dibandingkan dengan format file IFC, ukuran IFC-XML 300-400% lebih besar.

**IFC-ZIP:** Ini adalah versi terkompresi [ZIP](/id/compression/zip/) dari IFC atau IFC-XML di mana salah satu file ini berada di direktori utama arsip zip. Format ini memampatkan file .ifc hingga 60-80% dan file XML .ifc hingga 90-95%.

### Arsitektur IFC ###

Spesifikasi IFC mencakup istilah, konsep, dan item spesifikasi data yang berasal dari penggunaan dalam disiplin, perdagangan, dan profesi sektor industri manajemen fasilitas dan konstruksi. Istilah dan konsep menggunakan kata bahasa Inggris biasa, item data dalam spesifikasi data mengikuti konvensi penamaan.

nama item data untuk jenis, entitas, aturan, dan fungsi dimulai dengan awalan "Ifc" dan dilanjutkan dengan kata bahasa Inggris dalam konvensi penamaan CamelCase (tanpa garis bawah, huruf pertama pada kata dalam huruf besar); nama atribut dalam entitas mengikuti konvensi penamaan CamelCase tanpa awalan; definisi kumpulan properti yang merupakan bagian dari standar ini dimulai dengan awalan "Pset_" dan dilanjutkan dengan kata bahasa Inggris dalam konvensi penamaan CamelCase; definisi kumpulan kuantitas yang merupakan bagian dari standar ini dimulai dengan awalan "Qto_" dan dilanjutkan dengan kata bahasa Inggris dalam konvensi penamaan CamelCase.

Arsitektur skema data IFC mendefinisikan empat lapisan konseptual, masing-masing skema individu ditugaskan ke satu lapisan konseptual.

**Lapisan sumber daya** — lapisan terendah menyertakan semua skema individu yang berisi definisi sumber daya, definisi tersebut tidak menyertakan pengidentifikasi unik global dan tidak boleh digunakan secara terpisah dari definisi yang dideklarasikan pada lapisan yang lebih tinggi;

**Lapisan inti** — lapisan berikutnya mencakup skema kernel dan skema ekstensi inti, yang berisi definisi entitas paling umum, semua entitas yang ditentukan pada lapisan inti, atau di atasnya membawa id unik global dan secara opsional pemilik dan informasi riwayat;

**Lapisan interoperabilitas** — lapisan berikutnya mencakup skema yang berisi definisi entitas yang khusus untuk produk umum, proses, atau spesialisasi sumber daya yang digunakan di beberapa disiplin ilmu, definisi tersebut biasanya digunakan untuk pertukaran antardomain dan berbagi informasi konstruksi;

**Lapisan domain** — lapisan tertinggi mencakup skema yang berisi definisi entitas yang merupakan spesialisasi produk, proses, atau sumber daya khusus untuk disiplin tertentu, definisi tersebut biasanya digunakan untuk pertukaran intra-domain dan berbagi informasi.

## Referensi ##

* [Kelas Foundation Industri - Oleh Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

