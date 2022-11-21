{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PS",
  "description":"Pelajari tentang format file PS dan API yang dapat membuat dan membuka file PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file .PS? ##

PostScript (PS) adalah bahasa deskripsi halaman tujuan umum yang digunakan dalam bisnis desktop dan penerbitan elektronik. Fokus utama PostScript (PS) adalah memfasilitasi desain grafis dua dimensi. Sebagian besar bahasa memerlukan tahap kompilasi yang berbeda sebelum eksekusi kode sementara format Post Script (PS) mendukung interpretasi runtime langsung ke depan. Versi awalnya mendefinisikan bentuk grafis, tampilan teks yang berbeda, dan citra yang dimodelkan pada halaman cetak atau halaman yang ditampilkan, mengikuti aturan model pencitraan Adobe. Sebuah program PS mampu menghubungkan deskripsi dokumen antara komposisi dan sistem pencetakan yang menjaga independensi perangkat dan tingkat tinggi. Selain itu program ini juga mampu mengatur tampilan teks dan grafik pada sebuah tampilan.

Deskripsi halaman PostScript tersedia untuk dirender, ditampilkan pada printer dan perangkat keluaran lainnya dengan bantuan juru bahasa PostScript perangkat. Saat perintah untuk mencetak karakter, bentuk grafis dan gambar dijalankan oleh juru bahasa, untuk perangkat khusus itu, deskripsi PostScript tingkat tinggi diubah menjadi format data raster tingkat rendah. Umumnya, berbagai aplikasi seperti ilustrator, sistem komposisi dokumen, dan desain dengan bantuan komputer (CAD) diotomatiskan untuk menghasilkan deskripsi halaman PostScript. Umumnya programmer harus menulis program PostScript pada saat pembuatan aplikasi baru. Namun, seorang pemrogram dapat memanfaatkan kemampuan bahasa PostScript yang tidak dapat diakses di aplikasi mana pun dengan menulis program PS untuk situasi khusus tersebut.

## Sejarah Singkat ##

Konsep bahasa PostScript pertama kali diperkenalkan oleh John Warnock. Pada tahun 1966 dia mengerjakan proyek Pelabuhan New York. Dia mencoba mengembangkan juru bahasa untuk grafik tiga dimensi besar untuk basis data proyek itu. Untuk memproses grafik ini, John Warnock menyusun bahasa Sistem Desain. Sementara itu Xerox PARC mencari cara standar untuk menentukan gambar halaman untuk printer laser pertama mereka. Meskipun Bob Sproull dan William Newman pada tahun 1975-76 mengembangkan format Press (format data) untuk menggerakkan printer laser, namun bahasa diperlukan untuk fleksibilitas yang lebih besar. Pada tahun 1978 Warnock bergabung dengan Martin Newell di Xerox PARC dan menulis ulang bahasa interpretatif, JaM yang kemudian berkembang dan diperluas menjadi bahasa Interpress. Warnock mendirikan Adobe Systems pada Desember 1982 bersama Chuck Geschke, Doug Brotz, Ed Taft, dan Bill Paxton. Mereka mulai mengerjakan bahasa yang lebih sederhana yang disebut PostScript mirip dengan Interpress, yang dirilis secara komersial pada tahun 1984. Steve Jobs dari Apple mengunjungi mereka dan menyarankan mereka untuk mengadaptasi PostScript untuk menggerakkan printer laser.

Pada bulan Maret 1985, printer pertama dengan juru bahasa PostScript tertanam adalah LaserWriter Apple, yang merevolusi desktop publishing (DTP). Kesehatan teknis dan ketersediaan yang luas menjadikan PostScript, bahasa pilihan untuk desktop dan penerbitan elektronik. Selama tahun 1990, seorang juru bahasa untuk bahasa PostScript merupakan bagian penting dari printer laser.

## Fitur utama ##

Kemampuan bahasa PostScript untuk menangani grafik interaktif dan deskripsi halaman memiliki fitur berikut:

**Bentuk:** Bersifat sewenang-wenang, dapat terdiri dari garis lurus, kurva, bujur sangkar, dan kurva kubik yang dapat melintasi sendiri dan tidak terhubung (dalam bagian dan lubang).

**Operator pengecatan:** mengizinkan garis besar bentuk dengan ketebalan, warna, isian apa pun, atau mengizinkan bentuk digambar sebagai kliping untuk memungkinkan pemotongan grafik lainnya.

**Warna:** memiliki keragaman seperti grayscale, RGB, CMYK, dan CIE. Jenis warna khusus dimodelkan sebagai fitur yang berbeda: warna spot, pemetaan warna, bahkan pola bayangan dan pengulangan.

**Teks:** terintegrasi penuh dengan grafis. Selain itu, model pencitraan adobe memungkinkan karakter teks ditampilkan sebagai bentuk grafik yang dapat dioperasikan oleh operator grafik biasa.

**Gambar sampel**: diambil dari sumber asli (foto yang dipindai) atau dapat diproduksi secara sintetis. Bahasa PostScript menawarkan beragam cara untuk membuat ulang gambar pada resolusi apa pun dan menurut model warna yang berbeda pada perangkat keluaran.

Bahasa pemrograman tujuan umum dapat memanfaatkan kemampuan grafis bahasa PostScript dengan menyematkan Ps dalam kerangka kerjanya. Tipe data primitif, seperti angka, karakter, array, dan string; kontrol primitif, seperti, loop, prosedur dan kondisional; dan beberapa fitur yang tidak konvensional, seperti kamus ditentukan dalam bahasa. Fitur-fitur ini memfasilitasi pemrogram untuk menulis perintah untuk menjalankan operasi tingkat yang lebih tinggi. Operasi tingkat tinggi ini memenuhi kebutuhan aplikasi yang kompleks. Praktik seperti itu lebih kompak dan efisien daripada menggunakan serangkaian operasi dasar yang tetap.

Program yang ditulis dalam PostScript dapat diproduksi, dikomunikasikan, dan diinterpretasikan dalam bentuk teks sumber ASCII. Seluruh bahasa dapat didefinisikan dalam bentuk karakter yang dapat dicetak dan spasi putih. Representasi ini mendukung programmer untuk membuat, memanipulasi, dan memahami bahasa dengan mudah. Selain itu, penyimpanan dan transmisi file di antara beragam komputer dan sistem operasi tetap nyaman melalui kemandirian mesin.

Bentuk bahasa yang disandikan biner dimungkinkan, ketika program dijamin untuk jalur komunikasi yang sepenuhnya transparan ke juru bahasa PostScript. Kekompakan yang ketat terhadap representasi ASCII dari program PS disarankan dari Adobe untuk pertukaran dokumen atau penyimpanan arsip.

## Versi ##

PS(.ps) adalah ekstensi file untuk dokumen PostScript. Arsip Nasional Inggris mengkategorikan lima versi kronologis file PostScript, yang ditentukan dalam versi DSC: versi 1.0, 2.0, 2.1, 3.0, 3.1. Setiap versi mendefinisikan komentar penataan penting. Encapsulated PostScript File (EPS) adalah subtipe khusus dari file PostScript yang menggunakan bahasa untuk menentukan grafik persegi panjang. Manual Referensi Bahasa PostScript menggambarkan EPS sebagai, "File PostScript (EPS) yang dienkapsulasi adalah program PostScript yang menjelaskan paling banyak satu halaman dalam bentuk yang dapat diimpor oleh aplikasi lain untuk disematkan di dalam dokumen yang berisi." File dokumen PostScript dapat merangkum file EPS di dalamnya. Penggunaan tambahan PostScript disebut sebagai Display PostScript (DPS). DPS menghasilkan grafis di layar melalui mesin grafis yang menggunakan model dan bahasa pencitraan PostScript.

## Referensi ##

* [Rangkaian Format PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

