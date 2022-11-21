{
  "date" : "2021-06-30",
  "keywords" :[ "file msi", "format file MSI", "apa itu file msi", "file", "contoh msi", "ekstensi file msi", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file MSI dan API yang dapat membuat dan membuka file MSI.",
  "title" :"MSI - File Paket Pemasang Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Apa itu file MSI?
File MSI yang digunakan untuk menginstal dan meluncurkan program Windows; paket lengkap untuk Microsoft Windows yang berisi informasi penginstalan untuk program perangkat lunak biasa, termasuk file penting yang akan diinstal dan informasi tentang lokasi penginstalan. File MSI mungkin juga berisi paket untuk pembaruan perangkat lunak. File MSI mirip dengan [EXE](/id/executable/exe/), tetapi EXE terkadang tidak menyertakan informasi penginstal dan program perangkat lunak dapat berjalan langsung saat mengeksekusi file EXE.

## format file MSI
Penginstal Windows sebenarnya adalah API (Application Programming Interface) dan komponen perangkat lunak Microsoft Windows yang digunakan untuk penginstalan, penghapusan, dan pemeliharaan program perangkat lunak. Informasi penginstalan, dan file opsional, dikemas sebagai paket penginstalan dan basis data relasional longgar yang disusun sebagai Penyimpanan Terstruktur COM; dikenal sebagai **file MSI**, memiliki ekstensi file .msi. Paket dengan ekstensi file **.mst** berisi **Transformation Scripts** dari Windows Installer, file dengan ekstensi **.msm** berisi **Merge Modules** dan ekstensi file **.pcp** digunakan untuk **Properti Pembuatan Patch**. Windows Installer menjadi lebih maju setelah mengalami perubahan signifikan dari versi sebelumnya, Setup API. Kerangka kerja GUI dan pembuatan otomatis urutan un-installation adalah fitur baru dari Windows Installer. Sekarang telah dipertimbangkan sebagai alternatif untuk kerangka pemasang yang dapat dieksekusi yang berdiri sendiri.

### Struktur logis paket MSI
Paket menunjukkan penginstalan satu atau beberapa produk lengkap dan biasanya ditandai dengan **GUID**. Sebuah produk terdiri dari satu atau beberapa komponen dan dikelompokkan ke dalam berbagai fitur. Penginstal Windows tidak menangani ketergantungan antara berbagai produk secara bersamaan. Struktur logis dari paket terdiri dari elemen-elemen berikut:

- **Produk**: Program tunggal, terinstal, yang berfungsi, atau kumpulan beberapa program yang digabungkan menjadi satu produk. Produk diidentifikasi oleh GUID unik.
- **Fitur**: Dapat berisi sejumlah komponen dan sub-fitur lainnya. Paket yang lebih kecil dapat terdiri dari satu fitur.
- **Komponen**: Komponen diperlakukan oleh Penginstal Windows sebagai satu unit; dapat berisi file program, folder, kunci registri, komponen COM, dan pintasan.
- **Jalur Kunci**: Jalur kunci adalah file tertentu, sumber data ODBC, atau kunci registri yang ditentukan pembuat paket sebagai penting untuk komponen tertentu.

## Referensi

* [Penginstal Windows - oleh Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


