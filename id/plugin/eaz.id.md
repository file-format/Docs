{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File EAZ - Apa itu file EAZ dan bagaimana cara membukanya?",
  "description":"Pelajari tentang format file EAZ dan API yang dapat membuat dan membuka file EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-idz"
}
},
  "lastmod" : "2023-12-23"
}

## Apa itu file EAZ?

File EAZ adalah file Add-in yang digunakan oleh ArcGIS Explorer, aplikasi gratis yang dikembangkan oleh ESRI untuk eksplorasi, visualisasi, dan berbagi peta. Ini berisi arsip file terkompresi yang mencakup [XML file](/web/xml/), kode yang dikompilasi, dan file pendukung yang diperlukan untuk add-in. File-file ini digunakan untuk memperluas fungsionalitas dasar perangkat lunak dengan memasukkan tombol baru, jendela yang dapat di-dock, dan ekstensi lainnya.

## Format File EAZ - Informasi Lebih Lanjut

File EAZ dibuat melalui pemanfaatan ArcGIS Explorer SDK, kit pengembangan yang dirancang untuk membuat fungsionalitas khusus dalam ArcGIS Explorer. File-file ini menggunakan kompresi [ZIP](/compression/zip/) untuk mengemas kontennya secara efisien. Pada inti arsip, file **Addins.xml** berada di direktori akar, berfungsi sebagai komponen penting yang menguraikan dan merinci berbagai penyesuaian yang tertanam dalam file EAZ.

File Addins.xml pada dasarnya bertindak sebagai peta jalan, menawarkan wawasan tentang peningkatan, modifikasi, dan ekstensi spesifik yang diperkenalkan oleh file EAZ ke ArcGIS Explorer. Melalui struktur komprehensif ini, pengembang dapat merangkum dan mengintegrasikan fitur-fitur baru, tombol, dan jendela yang dapat di-dock secara mulus, sehingga meningkatkan keseluruhan fungsionalitas dan pengalaman pengguna aplikasi ArcGIS Explorer.

## Referensi

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
