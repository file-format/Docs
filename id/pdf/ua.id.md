{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PDF/UA",
  "description":"Pelajari tentang format file PDF/UA dan API yang dapat membuat dan membuka file PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Apa itu file PDF/UA? #

PDF/UA diterbitkan sebagai [Standar ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) pada bulan Agustus 2012 dan sejauh ini merupakan definisi lengkap pertama dari sekumpulan persyaratan untuk dokumen PDF yang dapat diakses secara universal. Istilah "dapat diakses secara universal" mengacu pada pemahaman bahwa informasi yang terkandung dalam dokumen [PDF](/id/pdf/) harus dapat diakses secara setara dan mandiri oleh semua orang pada umumnya dan khususnya penyandang disabilitas. Pengenalan standar PDF/UA dapat dianggap sebagai langkah besar untuk membuat alat dan aplikasi guna membuat dan membaca konten PDF.

## Persyaratan Format File ##

PDF/UA memiliki beberapa persyaratan pasti pada dasarnya yang bertindak sebagai inti dari standar ini. Pada dasarnya, ini didasarkan pada penandaan PDF yang berarti bahwa semua dokumen PDF/UA harus diberi penandaan dengan benar. Itu juga membutuhkan tag agar sesuai secara semantik dan dalam urutan logis. Ini memastikan bahwa dokumen akhir yang dibuat dengan spesifikasi PDF/UA lebih andal dan mudah diakses. Ini dapat membuat penulis PDF mempertanyakan apakah mereka perlu mengetahui segalanya tentang semua persyaratan tersebut? Untungnya, tidak seperti ini karena alat kepatuhan PDF/UA bertanggung jawab untuk menambah dan mempertahankan aksesibilitas PDF.

Persyaratan format file untuk PDF/UA adalah sebagai berikut.

* Konten dikategorikan dalam salah satu dari dua cara: konten bermakna, dan artefak seperti elemen halaman dekoratif. Semua konten yang bermakna harus diberi tag dan diintegrasikan ke dalam pohon struktur dari semua tag dalam dokumen. Artefak, di sisi lain, hanya perlu ditandai seperti itu.
* Konten yang bermakna harus ditandai dengan tag dan, bersama dengan tag lain dalam dokumen, buat pohon struktur yang lengkap.
* Konten yang bermakna harus ditandai dengan tag semantik yang sesuai.
* Pohon struktur yang dibuat oleh tag dokumen harus mencerminkan urutan pembacaan logis dokumen.
* Hanya tag standar yang ditentukan dalam PDF 1.7 yang dapat digunakan; jika ada tag lain yang digunakan, entri penetapan peran harus merekam tag standar mana yang diwakili masing-masing.
* Informasi tidak boleh disampaikan hanya dengan menggunakan sarana visual (misalnya kontras, warna atau posisi pada halaman).
* Konten yang berkedip, berkedip, atau berkedip tidak diizinkan, baik sebagai efek yang dikontrol oleh JavaScript atau sebagai bagian dari video apa pun yang disematkan dalam PDF.
* Judul dokumen harus diberikan, dan dokumen harus diatur sehingga judul (bukan nama file) muncul di judul jendela.
* Bahasa semua konten harus diperhatikan, dan perubahan bahasa harus ditandai secara eksplisit.

## Kesesuaian PDF/UA ##

Standar PDF/UA menetapkan spesifikasi untuk konten, pembaca, dan teknologi bantuan. Ketiga aspek ini terkait satu sama lain berdasarkan isi dokumen. Persyaratan kesesuaian untuk masing-masing ini adalah seperti yang disebutkan di bawah ini.

## File yang Sesuai ##

File yang sesuai dengan standar PDF/UA harus berisi fitur yang valid sesuai [spesifikasi PDF 1.7](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). Namun, fitur yang secara khusus dilarang oleh PDF/UA harus dikecualikan.

## Pembaca yang Sesuai ##

Pembaca yang patuh harus mematuhi aturan yang dieja oleh spesifikasi PDF 1.7. Secara khusus, itu harus mendukung:

* semua tag, atribut, dan nilai kunci yang ditentukan untuk aksesibilitas. Itu juga harus memiliki kemampuan untuk memproses dan mewakili tanda tangan digital, anotasi, dan Konten Opsional.
* memproses dan mewakili tanda tangan digital, anotasi, dan Konten Opsional
* menavigasi dokumen dengan berbagai cara

## Teknologi Bantuan yang Sesuai ##

Teknologi bantuan yang sesuai terikat untuk mendukung fitur PDF/UA. Ini termasuk, misalnya, fitur konten dan pembaca, dan harus memungkinkan navigasi menurut label halaman, struktur dokumen, atau kerangka. Itu juga harus membiarkan pengguna mengesampingkan zoom navigasi default.

## Referensi ##

* [PDF/UA - Oleh Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA singkatnya](https://pdfa.org/pdfua-in-a-nutshell/)

