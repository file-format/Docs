{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "file", "ekstensi", "format file", "File Makro Microsoft Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file XLM Macros dan API yang dapat membuat dan membuka file XLM.",
  "title" :"Apa itu file XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file XLM?

XLM, untuk Excel Macro, adalah jenis file Spreadsheet yang digunakan untuk menyimpan Macro. Dari sudut pandang aplikasi, Makro adalah sekumpulan instruksi yang digunakan untuk mengotomatisasi proses. Makro digunakan untuk merekam langkah-langkah yang dilakukan berulang kali untuk format file [XLS](/id/spreadsheet/xls/) dan memfasilitasi melakukan tindakan dengan menjalankan makro lagi. Makro diprogram dengan Visual Basic for Applications (VBA) Microsoft dari dalam Buku Kerja Excel menggunakan Editor Visual Basic dan dapat dijalankan/di-debug langsung dari sana.

## Sejarah Singkat ##

Microsoft Excel mendukung pemrograman makro sejak peluncuran publik pertamanya. Fitur makro tetap sama hingga versi berikutnya untuk Excel dengan ekstensi sesuai fitur baru. XLM adalah bahasa makro default untuk Excel hingga Excel 4.0. Excel 5.0 merekam makro di VBA secara default tetapi dengan versi 5.0 perekaman XLM masih diizinkan sebagai opsi. Setelah versi 5.0 opsi itu dihentikan. Semua versi Excel, termasuk Excel 2010 mampu menjalankan makro XLM, meskipun Microsoft tidak menganjurkan penggunaannya.

## Merekam Makro di XLM ##

Excel menyediakan langkah-langkah yang mudah digunakan untuk merekam makro. Ini mengharuskan Anda menginstal alat Pengembang untuk bekerja dengan Macro. Setelah perekaman makro dalam proses, merekam setiap tindakan pengguna untuk dimainkan nanti. Perekaman makro sebenarnya melibatkan semua langkah yang dilakukan pengguna setelah perekaman dimulai. Jadi, jika Anda membuat konten sel tebal, miring, dan menyetel pembenaran teksnya setelah perekaman makro dimulai, semua perintah ini akan direkam. Setiap makro yang direkam dapat diberi pintasan juga untuk pemutaran cepat nanti. Perekaman makro menghasilkan kode VBA dalam bentuk makro yang dapat diedit menggunakan Visual Basic Editor (VBE).

## Model Objek Excel ##

Makro menggunakan rutinitas VBA di belakangnya dan mengikuti [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) untuk tujuan ini. Model ini mengidentifikasi objek spreadsheet untuk berinteraksi dengan spreadsheet melalui toolbar perintah yang ditentukan pengguna, bilah perintah, atau kotak pesan. Misalnya, akses ke properti buku kerja diberikan dengan objek Buku Kerja. Demikian pula, ada objek Lembar Kerja dalam model untuk bekerja dengan lembar kerja buku kerja secara terprogram.

## Makro dan Keamanan ##

VBA memungkinkan akses ke semua area aplikasi serta sistem file dan juga bisa berbahaya. Hal ini menimbulkan kekhawatiran saat berbagi buku kerja dengan seseorang yang dapat menjalankan file tersebut pada akhirnya. Itu Microsoft Excel memperingatkan tentang membuka file seperti itu. Makro dapat disertifikasi dengan tanda tangan digital agar pengguna lain dapat memverifikasi bahwa ini dapat dipercaya. Dengan demikian, makro dapat diaktifkan setelah verifikasi sumbernya.

## Referensi ##

* [[MS-XLS] - Struktur Format File Biner Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Pemrograman Makro](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

