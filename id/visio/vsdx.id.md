{
  "date" : "2019-10-11",
  "keywords" :[ "file vsdx", "format file vsdx", "apa itu file vsdx", "file", "contoh vsdx", "ekstensi file vsdx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Pelajari tentang format file VSDX dan API yang dapat membuat dan membuka file VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file VSDX?

File dengan ekstensi .vsdx mewakili format file Microsoft Visio yang diperkenalkan dari Microsoft Office 2013 dan seterusnya. Ini dikembangkan untuk menggantikan format file biner, [.VSD](/id/image/vsd/), yang didukung oleh versi Microsoft Visio sebelumnya. Itu juga didukung pada Layanan Visio di Microsoft SharePoint Server 2013 dan tidak memerlukan format file perantara untuk menerbitkan ke SharePoint Server. File Visio digunakan untuk membuat gambar yang berisi objek visual, diagram alur, diagram UML, aliran informasi, bagan organisasi, diagram perangkat lunak, tata letak jaringan, model database, pemetaan objek, dan informasi serupa lainnya. File yang dibuat menggunakan Visio juga dapat diekspor ke berbagai format file seperti [PNG](/id/image/png/), [BMP](/id/image/bmp/), [PDF](/id/pdf/), dan lainnya.

## Format File ##

File VSDX didasarkan pada Open Packaging Conventions dan XML dan pengembang bisa mendapatkan keuntungan dari format ini dengan mempelajari cara bekerja dengan file ini secara terprogram. Format ini mewarisi banyak struktur XML yang sama sebagai bagiannya dari format file Visio XML Drawing (.vdx). Interoperabilitas dengan file Visio sangat meningkat karena perangkat lunak pihak ketiga dapat memanipulasi file Visio pada tingkat format file.

Jenis file tertentu lainnya yang terdiri dari format file Visio 2013 meliputi:

* .vsdm (gambar berkemampuan makro Visio)
* .vssx (stensil Visio)
* .vssm (stensil berkemampuan makro Visio)
* .vstx (templat Visio)
* .vstm (template berkemampuan makro Visio)

Di balik layar, format file Visio 2013 menggunakan sarana terstruktur untuk menyimpan data aplikasi bersama dengan sumber daya terkait dalam arsip seperti [ZIP](/id/compression/zip/). File ZIP dapat diekstraksi menggunakan utilitas ekstraksi standar apa pun yang juga berisi jenis file lain. Anda tinggal mengganti ekstensi file .vsdx dengan .zip di windows explore untuk melihat isi di dalam file VSDX.

Setiap file Visio disebut sebagai paket yang menampung file atau bagian lain. Bagian paket dapat berupa file XML, gambar, atau bahkan solusi VBA. Bagian dalam paket dapat dibagi menjadi bagian "dokumen" dan "hubungan".

### Dokumen ###

Bagian dokumen berisi konten dan metadata sebenarnya dari file Visio, seperti nama file, halaman pertama, dan semua bentuk yang ada di dalamnya, bahkan koneksi data untuk bentuk. File gambar dan teks dalam paket dianggap sebagai bagian dokumen.

### Hubungan ###

Bagian relasi dari file Visio disimpan di folder "\_rels" dan menjelaskan bagaimana bagian dalam paket terkait satu sama lain. Ini juga menyediakan struktur file. Dokumen XML mandiri menggunakan hubungan elemen induk/anak untuk menentukan hubungan entitas satu sama lain. Format file Visio 2013 yang valid berisi kumpulan bagian yang benar dan paket berisi hubungan antar bagian.

Bagian hubungan adalah dokumen XML yang menjelaskan hubungan antara bagian dokumen yang berbeda di dalam paket. Mereka mendefinisikan hubungan antara dua item: sumber tertentu (ditentukan oleh nama dan lokasi file hubungan) dan bagian dokumen target yang ditentukan. Misalnya, bagian hubungan digunakan untuk menjelaskan master bentuk mana yang diasosiasikan dengan file, bagaimana halaman berhubungan dengan file dan satu sama lain, atau bagaimana gambar dan objek berhubungan dengan halaman tertentu.

## Referensi ##

* [Pengantar Format File Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

