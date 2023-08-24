{
  "date" : "2021-03-30",
  "keywords" :["PMLZ", "File Bahasa Markup Palm yang Di-zip", "ekstensi", "File", "format", "eBuku", "Bahasa Markup Palm" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PMLZ, Palm Markup Language, dan API yang dapat membuat dan membuka file PMLZ.",
  "title" :"PMLZ - File Bahasa Markup Palm yang Di-Zip",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Apa itu file PMLZ?

Palm Inc memperkenalkan jenis file eBuku; dikenal sebagai format file PMLZ yang merupakan versi terkompresi dari format file [PML](/id/ebook/pml/) itulah sebabnya file dengan ekstensi .pmlz dikenal sebagai **File Bahasa Markup Palm Berzip**. File PMLZ hanyalah wadah zip dari file yang mengkompilasi file [PDB](/id/programming/pdb/) untuk membuat dokumen untuk **eReader** (Dikenal sebagai perangkat pembaca ebook seperti komputer tablet). File PML memberikan tata letak ke file PDB (berisi berbagai file data) untuk ditampilkan di Perangkat Palm. Padahal, file PDB adalah file database, yang digunakan oleh berbagai aplikasi, termasuk Quicken, Pegasus, Microsoft Visual Studio, dan Palm Pilot. Singkatnya, PMLZ adalah wadah terkompresi dari file PML dan PDB.


## Pengetahuan tentang Palm Markup Language
Tabel berikut menentukan perintah PML:

|Perintah|Deskripsi|
---|---|
| \p | Halaman baru |
| \x | Bab baru; juga menyebabkan jeda halaman baru. Lampirkan judul bab (dan kode gaya apa pun) dengan \x dan \x |
| \Xn | Bab baru, menjorok n level (n antara 0 dan 4 inklusif) dalam dialog Bab; tidak menyebabkan jeda halaman. Lampirkan judul bab (dan semua kode gaya) dengan \Xn dan \Xn |
| \Cn="Judul bab" | Sisipkan "Judul bab" ke dalam daftar bab, dengan level n (seperti \Xn). Teks tidak ditampilkan di halaman dan tidak memaksa jeda halaman. Ini terkadang berguna untuk menyisipkan tanda bab di awal pengantar bab, misalnya. |
| \c | Tengahkan blok teks ini; tutup dengan \c di awal baris |
| \ r | Kanan membenarkan blok teks; tutup dengan \r di awal baris |
| \i | Cetak miring blok; tutup dengan \i |
| \u | Blok garis bawah; tutup dengan \u |
| \o | Menyerang blok; tutup dengan \o |
| \v | Teks tak terlihat; tutup dengan \v (dapat digunakan untuk komentar) |
| \t | Blok inden. Mulai di awal baris, tutup dengan \t di akhir baris |
| \T="50%" | Indentasi persentase lebar layar yang ditentukan, 50% dalam kasus ini. Jika posisi gambar saat ini sudah melewati lokasi layar yang ditentukan, tag ini akan diabaikan. |
| \w="50%" | Sematkan aturan horizontal dari persentase lebar layar tertentu, dalam hal ini 50%. Tag ini menyebabkan jeda baris sebelum dan sesudahnya. Aturannya terpusat. Tanda persen adalah wajib. |
| \ n | Beralih ke font "normal", yang ditentukan oleh pengguna |
| \s | Beralih ke stdFont; tutup dengan \s untuk kembali ke font normal |
| \b | Beralih ke boldFont; tutup dengan \b untuk kembali ke font normal (usang; gunakan \B sebagai gantinya) |
| \l | Beralih ke font besar; tutup dengan \l untuk kembali ke font normal |
| \B | Tandai teks sebagai huruf tebal. Berbeda dengan \b tag, \B tidak mengubah font, sehingga Anda dapat memiliki teks tebal yang besar. Anda tidak dapat mencampur \b dan \B dalam file PML yang sama. |
| \Sp | Menandai teks sebagai superskrip. Tidak boleh dicampur dengan gaya lain seperti bold, italic, dll. Lampirkan teks superskrip dengan \Sp. |
| \Sb | Tandai teks sebagai subskrip. Tidak boleh dicampur dengan gaya lain seperti bold, italic, dll. Lampirkan teks subskrip dengan \Sb. |
| \k | Buat teks terlampir menjadi huruf kecil; tutup dengan \k. Setiap karakter yang terlampir dalam tag \k (termasuk yang beraksen) dibuat menjadi huruf besar dan dirender dengan ukuran titik yang lebih kecil daripada karakter huruf besar biasa. |
| \\ | Mewakili garis miring terbalik tunggal |
| \aXXX | Sisipkan karakter non-ASCII yang kode Windows-1252-nya adalah XXX desimal. Lihat tabel karakter PML untuk detailnya. |
| \UXXXX | Sisipkan karakter non-ASCII dengan kode Unicode XXXX heksadesimal. Lihat tabel karakter PML yang diperluas untuk detailnya. |
| \m="namagambar.png" | Masukkan gambar bernama. Lihat bagian Gambar di bawah ini. |
| \q="#linkanchor"Beberapa teks\q | Referensi jangkar tautan yang ada di tempat lain dalam dokumen. String setelah spesifikasi anchor dan sebelum trailing \q digarisbawahi atau ditampilkan sebagai tautan saat melihat dokumen. |
| \Q="linkanchor" | Tentukan jangkar tautan dalam dokumen. |
| \- | Sisipkan tanda hubung lunak. Tanda hubung lunak hanya muncul jika diperlukan untuk memecah kata melewati satu baris. |
| \Fn="catatan kaki1"1\Fn | Tautkan "1" ke catatan kaki yang namanya catatan kaki1, diberi tag di bagian akhir dokumen PML. Lihat bagian Catatan Kaki dan Bilah Samping di bawah ini. |
| \Sd="sidebar1"Sidebar\Sd | Tautkan teks "Sidebar" ke sidebar yang bernama sidebar1, yang ditandai di bagian akhir dokumen PML. Lihat bagian Catatan Kaki dan Bilah Samping di bawah ini. |
| \saya | Tandai sebagai item indeks referensi. Lampirkan item indeks (dan semua kode gaya) dengan \I dan \I.|


## Referensi

* [Palm Markup Language - Oleh MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Oleh MobileRead](https://en.wikipedia.org/wiki/E-reader)

