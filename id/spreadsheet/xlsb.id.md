{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "file", "ekstensi", "format file", "File Spreadsheet Biner Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file XLSB dan API yang dapat membuat dan membukanya.",
  "title" :"Apa itu berkas XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file XLSB?

Format file XLSB menentukan Format File Biner Excel, yang merupakan kumpulan rekaman dan struktur yang menentukan konten buku kerja Excel. Konten dapat mencakup tabel angka, teks, atau angka dan teks yang tidak terstruktur atau semi terstruktur, rumus, koneksi data eksternal, bagan, dan gambar. Tidak seperti [XLSX](/id/spreadsheet/xlsx/) (yang didasarkan pada format file Open XML), XLSB mewakili file buku kerja Excel biner. File XLSB dapat dibaca dan ditulis lebih cepat yang membuatnya berguna untuk bekerja dengan file besar. XLSB jarang digunakan untuk menyimpan buku kerja karena XLSX (dan sebelumnya [XLS](/id/spreadsheet/xls/)) adalah format file pilihan pengguna yang paling umum untuk menyimpan buku kerja. Dapat dibuka oleh Microsoft Office 2007 ke atas.

## Spesifikasi Format File XLSB ##

Spesifikasi format file untuk format file XLSB dipublikasikan kembali pada tahun 2008 sebagai versi 1.0. Sejak saat itu, spesifikasi telah direvisi beberapa kali dan versi spesifikasi terbaru (v 10.0) diterbitkan pada April 2018. Spesifikasi tersebut tersedia untuk umum oleh Microsoft sebagai [[MS-XLSB] - Spesifikasi Format File Biner Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) dan harus dikonsultasikan oleh siapa pun untuk membaca atau menulis file dalam format file XLSB.

## Struktur File XLSB ##

File XLSB adalah paket yang terdiri dari kumpulan bagian. Bagian ini berisi informasi tentang isi buku kerja, termasuk data buku kerja dan struktur paketnya. Beberapa bagian berisi informasi yang disimpan menggunakan catatan biner, beberapa sebagai XML, sementara yang lain berisi informasi yang disimpan sebagai aliran byte biner. Setiap rekaman biner berisi nol atau beberapa bidang terstruktur yang berisi data buku kerja.

#### Kemasan ####

Paket XLSB adalah arsip [ZIP](/id/compression/zip/) yang harus berisi tepat satu bagian buku kerja. Bagian ini harus menjadi target dari sebuah relasi di bagian relasi paket ini. Bagian buku kerja adalah bagian awal dalam dokumen XLSB.

#### Bagian ####

Bagian adalah aliran byte yang memiliki tipe konten terkait yang menentukan sifat dan jenis konten yang disimpan di bagian tersebut. Beberapa bagian menyimpan informasi dalam format biner sementara yang lain menyimpan informasi sebagai XML. Bagian [pencacahan suku cadang](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) dari dokumen spesifikasi mencantumkan suku cadang yang valid, tipe konten, dan hubungan wajib/opsional di antara semua bagian dalam satu paket.

#### Hubungan ####

Sumber dan sumber daya target dihubungkan oleh suatu hubungan. Sebuah hubungan bisa berupa:

**Hubungan paket:** di mana target adalah bagian dan sumber adalah paket secara keseluruhan

**Hubungan bagian-ke-bagian:** di mana target adalah bagian dan sumber adalah bagian dalam paket

**Hubungan eksplisit:** di mana sumber daya direferensikan dari konten bagian sumber dengan mereferensikan nilai atribut ID dari elemen hubungan

**hubungan implisit** adalah hubungan yang tidak eksplisit

**Hubungan internal:** di mana target adalah bagian dari paket

**Hubungan eksternal:** dengan target adalah sumber daya eksternal yang tidak ada dalam paket

#### Catatan ####

Catatan adalah blok penyusun dasar yang digunakan untuk menyimpan informasi tentang fitur dalam buku kerja. Setiap catatan biner adalah urutan byte dengan panjang variabel. Catatan biner terdiri dari tiga komponen:

* jenis rekaman
* ukuran rekaman, dan
* data rekaman yang khusus untuk jenis rekaman tersebut.

**Record Type:** Jenis record menampilkan jenis record yang ditentukan oleh record. Ini juga menentukan struktur data rekaman khusus untuk rekaman ini. Jenis rekaman yang valid tercantum di bagian [Enumerasi Rekaman](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) pada dokumen spesifikasi. Jenis rekaman harus satu atau dua byte dan harus lebih besar dari atau sama dengan 128 dan kurang dari 16384.

**Record Size:** Ukuran record menentukan jumlah byte yang menentukan ukuran total data record. Nilai ini HARUS satu sampai empat byte. Nilai ini HARUS satu byte jika bit tinggi dalam byte rendah sama dengan 0; jika tidak, nilai ini HARUS lebih besar dari satu byte. Jika hitungan byte lebih besar dari satu byte, bit tinggi di setiap byte berturut-turut menentukan apakah byte tambahan digunakan. Jika bit tinggi byte kedua sama dengan 1, maka nilai ini HARUS menggunakan byte ketiga tambahan. Jika bit tinggi dari byte ketiga sama dengan 1, maka nilai ini HARUS menggunakan byte keempat tambahan. Bit tinggi dari byte keempat HARUS diabaikan. Nilainya terdiri dari tujuh bit rendah dari setiap byte yang digabungkan. Bit rendah, paling tidak signifikan terkandung dalam byte pertama, dan setiap byte berikutnya berisi bit urutan lebih tinggi dari byte sebelumnya.

**Data Rekam:** Komponen data rekod berisi bidang yang sesuai dengan jenis rekod tertentu dan terdiri dari sisa rekod. Urutan dan struktur bidang untuk jenis catatan tertentu yang tercantum dalam Pencacahan Catatan ditentukan di bagian terkait untuk jenis catatan tersebut di Catatan. Ukuran total komponen data record HARUS sama dengan ukuran record. Bidang dalam komponen data rekaman dapat berisi nilai sederhana, larik nilai, struktur beberapa bidang, larik bidang, dan larik struktur.

#### Contoh Catatan XLSB ####

Jenis record dan ukuran record berikut menentukan record **BrtCommentText** dengan ukuran 200 byte:

11111101 00000100 11001000 00000001 [Rekam Bidang]

Byte pertama adalah 11111101, menentukan nilai rendah 125 dan tipe record membutuhkan byte kedua. Byte kedua adalah 00000100, menetapkan nilai tinggi 4 * 128, yang sama dengan 512. Nilai jenis rekaman adalah 125 + 512, atau 637, yang sesuai dengan jenis rekaman **BrtCommentText**. Byte berikutnya adalah 11001000, menentukan nilai rendah 72 dan ukuran record membutuhkan byte kedua. Byte kedua adalah 00000001, menentukan nilai yang lebih tinggi dari 1 * 128 dan ukuran record tidak memerlukan byte tambahan. Ukuran record adalah 72 + 128, atau 200, yang menentukan ukuran total, dalam byte, dari komponen data record. Bidang dalam komponen data rekaman ditentukan oleh **BrtCommentText**.

## Referensi ##

* [[MS-XLSB] - Format File Biner Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

