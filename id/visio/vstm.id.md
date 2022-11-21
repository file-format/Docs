{
  "date" : "2019-10-11",
  "keywords" :[ "file vstm", "format file vstm", "apa itu file vstm", "file", "contoh vstm", "ekstensi file vstm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Format File Templat Microsoft Visio",
  "description":"Pelajari tentang format file VSTM dan API yang dapat membuat dan membuka file VSTM.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file VSTM?

File dengan ekstensi VSTM adalah file template yang dibuat dengan Microsoft Visio yang mendukung makro. Tidak seperti file VSDX, file yang dibuat dari template VSTM dapat menjalankan makro yang dikembangkan dalam kode Visual Basic for Applications (VBA). File template dapat dibuat untuk memberikan pengaturan dasar dokumen yang dapat digunakan untuk menghasilkan dokumen lebih lanjut dengan pengaturan ini. File Visio digunakan untuk membuat gambar yang berisi objek visual, diagram alur, diagram UML, aliran informasi, bagan organisasi, diagram perangkat lunak, tata letak jaringan, model database, pemetaan objek, dan informasi serupa lainnya. File yang dihasilkan menggunakan Visio juga dapat diekspor ke berbagai format file seperti PNG, BMP, PDF, dan lainnya.

## Format File ##

File VSTM didasarkan pada Open Packaging Conventions dan XML dan pengembang bisa mendapatkan keuntungan dari format ini dengan mempelajari cara bekerja dengan file ini secara terprogram. Format ini mewarisi banyak struktur XML yang sama sebagai bagiannya dari format file Visio XML Drawing (.vdx). Interoperabilitas dengan file Visio sangat meningkat karena perangkat lunak pihak ketiga dapat memanipulasi file Visio pada tingkat format file.

Setiap file Visio disebut sebagai paket yang menampung file atau bagian lain. Bagian paket dapat berupa file XML, gambar, atau bahkan solusi VBA. Bagian dalam paket dapat dibagi menjadi bagian "dokumen" dan "hubungan".

### Dokumen ###

Bagian dokumen berisi konten dan metadata sebenarnya dari file Visio, seperti nama file, halaman pertama, dan semua bentuk yang ada di dalamnya, bahkan koneksi data untuk bentuk. File gambar dan teks dalam paket dianggap sebagai bagian dokumen.

### Hubungan ###

Bagian relasi dari file Visio disimpan di folder "_rels" dan menjelaskan bagaimana bagian dalam paket terkait satu sama lain. Ini juga menyediakan struktur file. Dokumen XML mandiri menggunakan hubungan elemen induk/anak untuk menentukan hubungan entitas satu sama lain. Format file Visio 2013 yang valid berisi kumpulan bagian yang benar dan paket berisi hubungan antar bagian.

Bagian hubungan adalah dokumen XML yang menjelaskan hubungan antara bagian dokumen yang berbeda di dalam paket. Mereka mendefinisikan hubungan antara dua item: sumber tertentu (ditentukan oleh nama dan lokasi file hubungan) dan bagian dokumen target yang ditentukan. Misalnya, bagian hubungan digunakan untuk menjelaskan master bentuk mana yang diasosiasikan dengan file, bagaimana halaman berhubungan dengan file dan satu sama lain, atau bagaimana gambar dan objek berhubungan dengan halaman tertentu.

## Referensi ##

* [Pengantar Format File Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

