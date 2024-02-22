{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - File Legenda ArcView",
  "description":"Pelajari tentang format file AVL dan API yang dapat membuat dan membuka file AVL.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-id",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Apa itu file AVL?

File AVL adalah file legenda yang berisi kunci peta yang dihasilkan dengan perangkat lunak ESRI ArcView GIS (Sistem Informasi Geografis). Ini berisi informasi simbologi referensi yang digunakan dalam peta terkait untuk akses. File AVL dapat berisi lebih banyak informasi seperti Simbologi, Pengaturan tampilan, seperti transparansi, Properti tampilan yang bergantung pada skala, informasi tabel yang digabungkan/tabel terkait, Kueri definisi, properti pelabelan untuk lapisan fitur, dan Properti tampilan anotasi untuk lapisan anotasi tergantung pada jenisnya jenis lapisan.

File AVL dapat direferensikan dari file proyek ArcView [.APR](/gis/apr/).

## Format File AVL - Informasi Lebih Lanjut

File AVL disimpan dalam format file teks biasa. Artinya Anda dapat membuka file AVL di editor teks apa pun seperti Notepad, Notepad++, dan Apple TextEdit. Setelah dibuka, Anda tidak hanya dapat melihat konten file tetapi juga memodifikasinya.

### Perbedaan antara File .LYR dan .AVL

 * **Perbedaan Format File** - .lyr adalah file biner sedangkan .avl adalah file teks
 * **Perbedaan Konten** - File .lyr berisi lebih banyak informasi daripada file .avl. File AVL hanya menyimpan informasi simbologi, sedangkan file LYR menyimpan semua informasi yang tersedia di kotak dialog properti lapisan di ArcMap.

## Referensi

* [Perbedaan antara File .lyr dan .avl](https://support.esri.com/en/technical-article/000005936)


