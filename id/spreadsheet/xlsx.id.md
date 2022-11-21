{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "file", "ekstensi", "format file", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang apa itu file XLSX dan API yang dapat membuat dan membuka file XLSX.",
  "title" :"Format File XLSX - Apa itu file XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file XLSX?

**XLSX** adalah format terkenal untuk dokumen Microsoft Excel yang diperkenalkan oleh Microsoft dengan rilis Microsoft Office 2007. Berdasarkan struktur yang diatur menurut Konvensi Pengemasan Terbuka sebagaimana diuraikan dalam [Bagian 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) dari standar OOXML ECMA-376, format barunya adalah paket zip yang berisi sejumlah file XML. Struktur dan file yang mendasarinya dapat diperiksa hanya dengan membuka ritsleting file .xlsx.

## Sejarah Singkat Format File XLSX

Format file XLSX diperkenalkan pada tahun 2007 dan menggunakan standar Open XML yang diadaptasi oleh Microsoft pada tahun 2000. Sebelum XLSX, format file yang umum digunakan adalah [XLS](/id/spreadsheet/xls/) yang merupakan format file biner murni. Jenis file baru telah menambahkan keunggulan ukuran file kecil, lebih sedikit perubahan korupsi dan representasi gambar yang diformat dengan baik. Pada awal tahun 2000, Microsoft memutuskan untuk melakukan perubahan untuk mengakomodasi standar **Office Open XML**. Pada tahun 2007, format file baru ini menjadi bagian dari Office 2007 dan dijalankan di versi baru Microsoft Office juga.

## Spesifikasi Format File XLSX

[Spesifikasi format file XLSX resmi](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) tersedia online dari Microsoft. Untuk melihat apa yang ada di dalam file XLSX, cukup ganti namanya menjadi file [ZIP](/id/compression/zip/) dengan mengubah ekstensinya lalu ekstrak untuk melihat file konstituen buku kerja Excel ini. Buku kerja kosong, saat diekstrak ke filenya, memiliki file dan folder konstituen berikut.

### [Content_Types].xml ###

Ini adalah satu-satunya file yang ditemukan di tingkat dasar saat zip diekstrak. Ini mencantumkan tipe konten untuk bagian dalam paket. Semua referensi ke file XML yang disertakan dalam paket direferensikan dalam file XML ini.

### \_rels (Folder) ###

Ini adalah folder Hubungan yang berisi satu file XML yang menyimpan hubungan tingkat paket. Tautan ke bagian penting dari file Xlsx terdapat dalam file ini sebagai URI. URI ini mengidentifikasi jenis hubungan dari setiap bagian kunci ke paket. Ini termasuk hubungan dengan dokumen kantor utama yang terletak sebagai xl/workbook.xml dan bagian lain dalam docProps sebagai properti inti dan tambahan.

### docProps ###

Folder ini berisi properti dokumen secara keseluruhan. Ini termasuk satu set properti inti, satu set properti yang diperluas atau khusus aplikasi dan pratinjau thumbnail dokumen. Buku kerja kosong memiliki dua file di folder ini yaitu app.xml dan core.xml. core.xml berisi informasi seperti penulis, tanggal dibuat dan disimpan, dan dimodifikasi. App.xml berisi informasi tentang konten file.

### xl (Folder) ###

Ini adalah folder utama yang berisi semua detail tentang isi buku kerja. Secara default, ini memiliki folder berikut:

* \_rels
* tema
* lembar kerja

dan file xml berikut:

* style.xml
* buku kerja.xml

## Contoh Format XLSX ##


Untuk setiap lembar kerja Excel yang terdapat dalam buku kerja, ada satu file XML. Anda dapat menemukan file XML ini di folder xl/worksheets. Semua informasi yang terdapat dalam lembar kerja diatur dalam bagian yang berbeda dalam file XML. Mari kita periksa contoh lembar kerja dari buku kerja yang ditunjukkan pada gambar berikut.

{{< figure src="../XLSX file format.png" alt="Format File XLSX" >}}

Seperti yang bisa dilihat, lembar kerja ini berisi konten di sel A1 hingga B2 dan sebuah gambar. Selain itu, sel G13 saat ini adalah sel aktif di lembar kerja. Sekarang, mari kita periksa file xl/worksheets/sheet1.xml untuk melihat bagaimana informasi ini direpresentasikan dalam file XML. Isi file XML ini adalah seperti yang ditunjukkan di bawah ini.

{{< figure src="../XLSX File Format Details.png" alt="Format File XPS" >}}

1. Tab memiliki warna tema yang diterapkan padanya. Disebutkan dalam file XML dengan tag<tabColor> mengikuti id tema.
1. Nilai tabSelected diatur ke 1 yang menunjukkan bahwa ini adalah sheet yang dipilih
1. Seperti yang terlihat pada gambar pertama di atas, sel G13 di lembar kerja adalah sel aktif yang juga disebutkan dalam file XML.
1. Tab sheetData mewakili data yang terdapat dalam lembar kerja. Namun, Anda dapat melihat bahwa konten asli lembar kerja tidak ada di bagian ini. Ini karena teks secara tidak langsung dirujuk dari lembar XML "sharedStrings". Tautan ini memastikan bahwa setiap teks disimpan hanya sekali dan dapat direferensikan lagi untuk menghemat ruang.
1. Gambar seperti yang terlihat direferensikan oleh id referensi "rId2"

## Menyumbang

Harus berbagi sesuatu tentang format file XLSX atau Spreadsheet? Anda dapat memposting temuan Anda di bagian [Berita Format File Spreadsheet](https://news.fileformat.com/t/Spreadsheet).

## Referensi

* [[MS-XLSX] - Format File XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Buka Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

