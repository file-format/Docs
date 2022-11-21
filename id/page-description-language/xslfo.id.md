{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Objek Pemformatan XSL", "File", "Ekstensi", "Format File", "Bahasa Lembar Gaya yang Dapat Diperluas"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Pelajari tentang format file XSLFO dan API yang dapat membuat dan membuka file XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file XSL-FO? ##

XSL-FO (XSL Formatting Objects) adalah bahasa stylesheet yang ampuh untuk memformat dokumen XML. Semantik dari bentuk kertas dan cetakan yang dibatasi diekspresikan oleh XSL-FO ketika dimensinya tetap. Berbeda dengan HTML, semantik yang merepresentasikan bentuk tak terbatas dari jendela browser dengan dimensi variabel. Dokumen XML yang diformat oleh XSL-FO sebagian besar digunakan untuk menghasilkan file PDF. XSL (Extensible Stylesheet Language) adalah seperangkat teknologi W3C lengkap fitur yang dimaksudkan untuk merancang pemformatan dan pertukaran dokumen XML dan bagian XSL-FO dari bahasa ini. XSLT dan XPath juga merupakan bagian lain dari XSL.

Diusulkan bahwa dokumen XML harus diubah terlebih dahulu menjadi XSL-FO, PDF adalah contoh dari kriteria ini. Dalam PDF, hasil dirender menggunakan XSLT terlebih dahulu, lalu pemformat XSL-FO. Dengan cara ini, dokumen XML dapat diformat secara acak. Meskipun XSL-FO mengambil keuntungan dari penggunaan properti Cascading Style Sheet (CSS) dan memperluasnya jika diperlukan untuk format sebenarnya, XSL-FO menampung penyediaan templat halaman yang disebut master halaman dalam terminologi XSL-FO. XSL-FO juga menyediakan pemformatan untuk dokumen yang cukup canggih dan mendukung pembuatan indeks.

## Sejarah dan Konsep Dasar ##

Pada Januari 2012, Working Draft XSL-FO terakhir kali diperbarui, dan pada November 2013, Working Group-nya telah ditutup. Lembar gaya XSL menentukan presentasi kelas dokumen XML dengan menjelaskan bagaimana turunan kelas diubah menjadi dokumen XML yang menggunakan kosakata pemformatan. XSL-FO adalah bahasa presentasi terintegrasi dan tidak memiliki markup semantik yang digunakan dalam HTML. Selain itu, bahasa ini menyimpan semua data dokumen di dalam dirinya sendiri, bertentangan dengan CSS yang mengubah pengaturan default dokumen HTML atau XML eksternal.

Kriteria umum menggunakan XSL-FO adalah pengguna menulis dokumen dalam bahasa XML daripada menulis dalam FO. Setelah itu, transformasi XSLT terjadi. Transformasi XSLT ini bertanggung jawab untuk konversi XML menjadi XSL-FO. Segera setelah dokumen XSL-FO dibuat, kemudian diserahkan ke aplikasi yang disebut pemroses FO. Pemroses FO bertanggung jawab untuk mengubah dokumen ini menjadi dokumen yang dapat dibaca dan dicetak. File PDF atau PS adalah contoh keluaran XSL-FO yang paling umum. Namun bukan berarti prosesor FO hanya bisa menghasilkan dua jenis format tersebut sebagai output. Beberapa prosesor FO dapat menghasilkan file RTF atau bahkan sebuah jendela dapat muncul di GUI pengguna, jendela ini menampilkan urutan halaman dan isinya.

Dokumen XSL-FO berbeda dari PDF atau PS dalam arti, pada akhirnya tidak menentukan tata letak teks pada halaman yang berbeda. Mungkin, mengatur gaya halaman dan menentukan tempat untuk menampilkan konten. Selain itu, pemroses FO mengatur teks dalam batas-batas yang ditentukan oleh dokumen FO. Spesifikasi ini bahkan mengizinkan pemroses FO yang berbeda untuk berperilaku sesuai dengan halaman yang dihasilkan. Contoh dari perilaku tersebut adalah hyphenation, beberapa pemroses FO dapat menghipnotis kata-kata untuk menghemat ruang saat garis terputus, sementara beberapa pemroses tidak memilih opsi ini. Itu tergantung pada prosesor untuk memilih algoritma tanda hubung yang berbeda yang sesuai dengan kebutuhan mereka. Algoritme hyphenation ini mungkin sangat sederhana atau mungkin lebih kompleks. Dalam beberapa situasi, spesifikasi XSL-FO secara eksplisit memberi sanksi pada prosesor FO, beberapa tingkat pilihan dalam konteks tata letak.

Variasi di antara pemroses FO ini menghasilkan hasil yang beragam, yang sering diabaikan oleh pemroses. Karena fokus umum XSL-FO adalah menghasilkan dokumen halaman/cetak. Dokumen XSL-FO sendiri biasanya bertindak sebagai perantara, fungsi utamanya adalah menghasilkan file PDF atau dokumen yang dapat dicetak sebagai keluaran untuk didistribusikan. Dalam HTML/CSS atau XSL-FO, mendistribusikan PDF sebagai hasil akhir daripada memasukkan bahasa pemformatan menunjukkan bahwa penerima tetap tidak terpengaruh oleh keserbagunaan yang dihasilkan karena perbedaan di antara penafsir bahasa pemformatan. Di sisi lain, jelas tidak ada cara yang mudah, bahwa sebuah dokumen dapat memenuhi kebutuhan penerima yang berbeda, misalnya ukuran halaman variabel atau ukuran font yang diinginkan, atau menyesuaikan halaman atau cetakan.

## Format File XSLFO ##

Dokumen SL-FO pada dasarnya adalah dokumen XML, tetapi tidak mengikuti skema apa pun. Sebagai gantinya, dokumen SL-FO mengikuti sintaks yang ditentukan dalam spesifikasi bahasanya sendiri. Ada dua bagian yang diperlukan dalam setiap dokumen XSL-FO:

1. Bagian yang menentukan daftar tata letak halaman berlabel.
1. Bagian dengan semua detail data dokumen, dengan markup, yang menentukan tampilan konten pada halaman berbeda melalui berbagai tata letak halaman.

Properti halaman disebutkan dalam tata letak halaman, yang dapat menentukan organisasi teks, untuk mematuhi konvensi untuk bahasa tertentu. Selain itu, ukuran halaman, marginnya, dan urutan halaman (yang memberikan sanksi properti yang berbeda untuk halaman ganjil dan genap) juga ditentukan oleh tata letak halaman.

Porsi data dokumen dibagi menjadi rangkaian alur, di mana setiap aliran terhubung ke tata letak halaman. Alur menyertakan daftar blok di dalamnya. Daftar blok ini mungkin berisi fitur markup sebaris atau daftar data teks, atau mungkin keduanya sekaligus. Margin dokumen juga dapat menampilkan nomor halaman atau judul bab. Fungsionalitas blok dan elemen inline tetap sama seperti di CSS, namun beberapa aturan padding dan margin berbeda antara FO dan CSS.

Arah orientasi halaman sepenuhnya ditentukan untuk perpanjangan blok dan inline, sehingga membuat dokumen FO tampil di bawah bahasa yang berbeda dari bahasa Inggris. Bahasa spesifikasi FO menggunakan kata mulai dan akhir daripada kiri dan kanan untuk deskripsi arah. Markup konten dasar dan aturan kaskade XSL-FO diambil dari CSS. Bahasa XSL-FO sesuai dengan spesifikasi berikut.

## Beberapa kolom ##

Halaman dapat memiliki beberapa kolom dan blok dan dapat diperluas dari satu kolom ke kolom lainnya secara default. Beberapa halaman diperbolehkan memiliki lebar dan jumlah kolom yang berbeda. Semua karakteristik FO mengikuti batas halaman multi-kolom.

### Daftar ###

Daftar XSL-FO dibuat oleh dua set blok yang disusun berdampingan. Secara konseptual, dalam daftar, blok di sebelah kiri menunjukkan angka, poin, atau string teks, sedangkan blok di sebelah kanan dapat berfungsi seperti yang diharapkan. Penomoran daftar XSL-FO biasanya dilakukan oleh XSLT.

### Tabel ###

Tabel FO mirip dengan tabel HTML/CSS. Pengguna dapat memilih baris data, informasi gaya, warna latar belakang untuk setiap sel individual. Dengan menggunakan informasi gaya yang berbeda, pengguna memiliki hak istimewa untuk memilih baris pertama sebagai baris tajuk tabel. Pemroses FO dapat diinformasikan secara eksplisit tentang spesifikasi ruang setiap kolom, atau untuk menyesuaikan teks secara otomatis dalam tabel.

### Pengindeksan ###

XSL-FO 1.1 memiliki fitur yang membantu menghasilkan indeks melalui referensi elemen yang ditandai dengan benar.

### Manfaat ###

* Sesuai untuk penerbitan berbasis konten
* Kemudahan penggunaan
* Biaya rendah

## Referensi ##

* [Apa itu XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Objek Pemformatan XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

