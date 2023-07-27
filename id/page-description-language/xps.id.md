{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Spesifikasi Kertas XML", "File", "Ekstensi", "Format File", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Format Berkas Tata Letak Halaman",
  "description":"Pelajari tentang format file XPS dan API yang dapat membuat dan membuka file XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file XPS? ##

File XPS mewakili file tata letak halaman yang didasarkan pada Spesifikasi Kertas XML yang dibuat oleh Microsoft. Ini dikembangkan sebagai pengganti format file EMF dan mirip dengan format file [PDF](/id/pdf/), tetapi menggunakan XML dalam tata letak, tampilan, dan informasi pencetakan dokumen. Faktanya, lebih dibenarkan untuk mengatakan bahwa XPS adalah upaya pada PDF, tetapi tidak bisa mendapatkan popularitas yang cukup seperti yang dimiliki oleh PDF karena berbagai alasan. Microsoft menyediakan Penulis Dokumen XPS secara default dari Windows 7 dan seterusnya untuk pembuatan file XPS. File XPS dapat dibuat dengan memilih "Microsoft XPS Document Writer" sebagai printer saat mencetak dokumen.

Penampil XPS terintegrasi sebagai bagian dari Windows Vista, Windows 7, Windows 8, dan Internet Explorer 6 atau lebih baru. File XPS menjadi hanya-baca setelah dibuat. Hal ini menambah kepercayaan pengguna terhadap dokumen yang diterima yang dikirim sebagai XPS untuk keaslian dokumen tersebut. Dokumen XPS dapat berisi satu atau lebih halaman yang dikonversi dari dokumen asli.

## Sejarah Singkat ##

Microsoft mengirimkan spesifikasi XPS ke Ecma International. Pada bulan Juni 2007, Komite Teknis Ecma 46 (TC46) dibentuk untuk mengembangkan standar berdasarkan Spesifikasi Kertas OpenXPS. Ecma International menyetujui Standar Ecma (ECMA-388) [spesifikasi XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) pada bulan Juni 2009 di Majelis Umum ke-97.

## Format File XPS ##

Format XPS terdiri dari markup XML yang menentukan komposisi dokumen dan tampilan visual setiap halaman bersama dengan aturan rendering untuk menampilkan atau mencetak dokumen. Itu menyimpan semua informasi untuk membuat ulang dokumen di sistem apa pun yang membuatnya terlepas dari sumber daya yang tersedia di sistem itu. Formatnya pada dasarnya adalah arsip ZIP dan jika Anda mengganti nama ekstensi file menjadi ZIP, Anda akan melihat file konstituen yang berisi data dokumen. Dokumen-dokumen ini meliputi:

* file halaman dokumen (.fpage) - Berisi konten dokumen dan pengaturan format dokumen. Setiap halaman dalam dokumen XPS memiliki satu file FPAGE.
* file pengaturan dokumen (.fdoc) - Menyimpan pengaturan yang termasuk dalam arsip XPS.
* file fragmen dokumen (.frag) - Menentukan pengaturan untuk file XPS aktual dan setiap halaman dalam dokumen memiliki file .fragnya sendiri.

{{< figure src="../XPS-1.png" alt="Format File XPS" >}}

File-file ini menyimpan konten dokumen sedemikian rupa sehingga jika, misalnya, seseorang tidak menginstal font yang sama di mesinnya, penampil XPS akan tetap merender font asli tersebut. Ini menyiratkan penyertaan file markup XML untuk masing-masing:

* Halaman
* Teks
* Font tertanam
* Gambar raster
* Grafik vektor 2D
* Manajemen hak digital

Format Dokumen XPS menyertakan kumpulan bagian dan hubungan yang terdefinisi dengan baik, masing-masing memenuhi tujuan tertentu dalam dokumen. Formatnya juga memperluas fitur paket, termasuk tanda tangan digital, thumbnail, dan interleaving.

Dokumen XPS tipikal terlihat seperti berikut dan dapat dianalisis berdasarkan format file XPS [spesifikasi](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Format File XPS" >}}


## Referensi ##

* [Spesifikasi Format File XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Oleh Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

