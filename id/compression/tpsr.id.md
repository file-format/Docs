{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File TPSR - File Laporan Sesi Pilot TeamViewer",
  "description":"Pelajari tentang format file TPSR dan API yang dapat membuat dan membuka file TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Apa itu file TPSR?

TPSR adalah file protokol koneksi yang digunakan oleh TeamViewer Assist AR (sebelumnya dikenal sebagai TeamViewer Pilot). Informasi yang disimpan dalam file TPSR disimpan dalam format file [ZIP](/id/compression/zip/) terkompresi. TPSR berisi riwayat detail koneksi TeamViewer antara pakar dan teknisi untuk menyelesaikan masalah dan tujuan peninjauan. Informasi yang terkandung di dalam file TPSR mencakup jenis perangkat, nama, ID AR Bantuan, ID Pakar, tanggal dan waktu, serta durasi koneksi. Data ini disimpan dalam file [JSON](/id/web/json/) di dalam arsip TPSR terkompresi.

## Format File TPSR

File TPSR disimpan ke disk dalam format file arsip ZIP yang isinya disimpan di dalam file JSON. Ini dihasilkan secara otomatis setelah penyelesaian koneksi Assist AR asalkan opsi pelaporan Connetion diaktifkan di TeamViewer.

TeamViewer Assist AR memungkinkan pakar terhubung ke teknisi untuk mendapatkan umpan LANGSUNG dari ujung jarak jauh melalui kamera seluler. Mereka dapat membantu teknisi untuk menyelesaikan masalah melalui telepon.

## Buka File TPSR

Anda dapat membuka file TPSR menggunakan perangkat lunak TeamViewer versi desktop. Jika diinstal pada komputer Anda, mengklik dua kali file TPSR akan membukanya di perangkat lunak TeamViewer. File TPSR juga dapat diekspor ke file [PDF](/id/pdf/) atau dapat dicetak untuk mendapatkan salinan cetak dari file protokol.

## Referensi ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

