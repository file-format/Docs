{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "apa itu file cd", "cara membuka file cd", "ekstensi", "file", "file cd", "format file cd", "ekstensi file cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - File Diagram Kelas Visual Studio",
  "description":"Pelajari tentang format file CD dan API yang dapat membuat dan membuka file CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Apa itu file CD?

File dengan ekstensi .cd adalah file diagram kelas Visual Studio yang menyediakan informasi tentang struktur dan hubungan antara semua kelas dalam solusi saat ini. Solusi Visual Studio (diwakili oleh [.sln](/id/programming/sln/)) dapat berisi satu atau lebih proyek, masing-masing memiliki beberapa kelas yang berbeda. File diagram kelas dapat dihasilkan dengan mengklik kanan proyek dan memilih opsi diagram kelas.

## Format File Diagram Kelas (.cd) - Informasi Lebih Lanjut

File diagram kelas disimpan dalam format file XML standar yang mewakili kelas dalam proyek sebagai simpul XML. Jika Visual Studio tidak tersedia, file diagram kelas ini dapat dibuka di program aplikasi apa pun yang mendukung pembukaan file XML.

### Cara Menambahkan Diagram Kelas ke Proyek Visual Studio

Di Visual Studio, buka Solusi/Proyek yang ingin Anda tambahkan diagram kelasnya. Kemudian, klik kanan simpul proyek lalu pilih Tambah > Item Baru. Atau, tekan Ctrl+Shift+A.

* Dialog Tambahkan Item Baru akan terbuka.

* Luaskan Item Umum > Umum, lalu pilih Diagram Kelas dari daftar template. Untuk proyek Visual C++, lihat di kategori Utilitas untuk menemukan template Diagram Kelas.

### Ekspor Diagram Kelas (CD) ke Gambar

Visual Studio memungkinkan untuk mengonversi/mengekspor diagram kelas ke gambar seperti [PNG](/id/image/png/), [JPEG](/id/image/jpeg/), dan [BMP](/id/image/bmp/). File diagram kelas yang diekspor ini dapat digunakan untuk tujuan penyimpanan dokumentasi dan paket data teknis (TDP). Untuk mengubah diagram kelas menjadi gambar, langkah-langkah berikut dapat digunakan dari dalam Microsoft Visual Studio.

1. Buka file diagram kelas (.cd) Anda.
1. Dari menu Diagram Kelas atau menu pintasan permukaan diagram, pilih Ekspor Diagram sebagai Gambar.
1. Pilih diagram.
1. Pilih format yang Anda inginkan.
1. Pilih Ekspor untuk menyelesaikan ekspor.

## Referensi

* [Kelas Desain di Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

