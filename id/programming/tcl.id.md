{
  "date" : "2021-09-02", 
  "keywords" :[ "TCL", "file", "ekstensi", "format file", "tiсkle", "Panduan Pemrograman", "contoh tcl", "Bahasa TCL", "inisialisme", "Tооl Соmmаnd Lаnguаge" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCL - File Bahasa Alat Bantu",
  "description":"Pelajari tentang format file TCL dan API yang dapat membuat dan membuka file TCL.",
  "linktitle" : "TCL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-02"
}

## Apa itu file TCL?

TCL (diucapkan "menggelitik" atau sebagai inisialisasi) adalah bahasa pemrograman tingkat tinggi, umum, ditafsirkan, dan dinamis. Itu dirancang dengan tujuan menjadi sangat sederhana namun kuat. TCL melemparkan segala sesuatu ke dalam cetakan perintah, bahkan pemrograman konstruksi seperti penugasan variabel dan definisi prosedur. Bahasa TCL mendukung beberapa pola peta, termasuk gaya peta yang berorientasi objek, penting, dan fungsional.

## Format File TCL ##

TCL biasanya hanya digunakan tertanam ke dalam aplikasi, untuk pengembangan cepat, aplikasi skrip, GUI, dan pengujian. Penerjemah TCL tersedia untuk banyak sistem operasi, memungkinkan kode TCL berjalan di berbagai sistem. Karena TCL adalah bahasa yang sangat nyaman, TCL digunakan pada platform sistem tertanam, baik dalam bentuk penuh maupun dalam beberapa versi kecil lainnya.

Kombinasi populer dari TCL dengan ekstensi Tk disebut sebagai TCL/TK, dan memungkinkan membangun antarmuka pengguna grafis (GUI) secara native di TCL. TCL/TK disertakan dalam instalasi Python standar dalam bentuk Tkinter. TCL berinteraksi secara native dengan bahasa С. Hal ini karena itu pada awalnya ditulis untuk menjadi kerangka kerja untuk menyediakan front-end sintaksis ke perintah yang ditulis dalam С, dan semua perintah dalam bahasa (termasuk hal-hal yang mungkin menjadi kata kunci, seperti jika atau sementara) diterapkan di sini.

Bahasa TCL selalu memungkinkan untuk paket ekstensi, yang menyediakan fungsi tambahan, seperti GUI, aplikasi otomatisasi berbasis terminal, akses database, dan sebagainya. TCL adalah bahasa pemrograman yang sangat sederhana yang dapat ditafsirkan sumber-sumber yang ditafsirkan secara sederhana yang menyediakan fasilitas umum seperti variabel, prosedur, dan struktur kontrol serta banyak fitur berguna yang tidak ditemukan di banyak tempat.


## Sejarah Singkat ##

Bahasa pemrograman TCL dibuat pada musim semi tahun 1988. Awalnya "dilahirkan dari frustrasi", menurut penulisnya, dengan programmer merancang bahasa mereka sendiri yang dimaksudkan untuk disematkan ke dalam lisensinya sendiri. Оusterhоut dianugerahi pada tahun 1997 untuk TCL/TK. Nama aslinya berasal dari Tооl Соmmаnd Lаnguаge, tetapi biasanya dieja "TCL" daripada "TСL". Lem yang lebih sederhana membuat pekerjaan lebih mudah.


## Spesifikasi Teknis ##

Semua rangkuman adalah perintah, termasuk struktur bahasa. Mereka ditulis dalam notasi awalan. Umumnya hanya menerima sejumlah variabel argumen. Semuanya dapat secara dinamis didefinisikan ulang dan ditunggangi. Sebenarnya, tidak ada kata kunci, bahkan struktur kontrol dapat ditambahkan atau diubah, meskipun ini tidak disarankan. Semua tipe data dapat dimanipulasi sebagai string, termasuk kode sumber.

Secara internal, variabel memiliki tipe seperti bilangan bulat dan ganda, tetapi konversi murni otomatis. Variabel tidak dideklarasikan, tetapi ditugaskan ke. Penggunaan variabel yang tidak ditentukan menghasilkan kesalahan. Sepenuhnya dinamis, sistem objek berbasis kelas, TCL, termasuk fitur lanjutan seperti kelas meta, filter, dan mixin. Antarmuka berbasis peristiwa ke soket dan file. Acara berbasis waktu dan yang ditentukan pengguna juga dimungkinkan. Visibilitas variabel terbatas pada lingkup leksikal (statis) secara default, tetapi uplevel dan upvаr memungkinkan semua bagian untuk berinteraksi dengan lingkup fungsi terlampir.

Semua perintah yang ditentukan oleh TCL sendiri menghasilkan pesan kesalahan pada penggunaan yang salah. Ekstensibilitas, melalui С, С++, Jаvа, Рythоn, dan TCL. Bahasa yang ditafsirkan menggunakan kode byte. Unicode Penuh (3.1 pada awalnya, diperbarui secara teratur) pertama kali dirilis pada tahun 1999.

Safe-Tcl adalah bagian dari TCL yang memiliki fitur terbatas sehingga skrip TCL tidak dapat membahayakan mesin hosting atau aplikasi mereka. Safe-Tcl dapat disertakan dalam email ketika аррliсаtiоn/safe-tcl dan multipartаrt/enаbled-mаil didukung. Fungsi Safe-Tcl sejak saat itu dimasukkan sebagai bagian dari rilis TCL/TK standar.


## Contoh Format File TCL ##

```
puts "Hello, World!"

oo::class create fruit {
    method eat {} {
        puts "yummy!"
}
}
oo::class create banana {
    superclass fruit
    constructor {} {
        my variable peeled
        set peeled 0
}
    method peel {} {
        my variable peeled
        set peeled 1
        puts "skin now off"
}
    method edible? {} {
        my variable peeled
        return $peeled
}
    method eat {} {
        if {![my edible?]} {
            my peel
    }
        next
}
}
set b [banana new]
$b eat               → prints "skin now off" and "yummy!"
fruit destroy
$b eat               → error "unknown command"
```

## Referensi ##

* [TCL - oleh Wikipedia](https://en.wikipedia.org/wiki/Tcl)



