{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK File Format - Apa itu file Lock?",
  "description":"Pelajari tentang format file LOCK dan .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Apa itu file KUNCI?

File **LOCK** adalah file yang diganti namanya yang digunakan oleh aplikasi dan sistem operasi untuk menandai file atau beberapa perangkat sebagai terkunci. Ini memberi tahu aplikasi lain untuk tidak menggunakan file kecuali file tersebut bebas dari aplikasi yang menggunakannya. Dalam sebagian besar kasus, file kunci ini kosong, tetapi dalam kasus lain, mungkin berisi informasi yang terkait dengan kunci seperti properti dan pengaturan.

Terkadang, file .lock digunakan oleh Microsoft .NET Framework untuk membuat salinan **lockeed** dari file database. Dalam kasus seperti itu, salinan file database akan terbuka dengan ekstensi .lock. Ini tidak memungkinkan pengguna untuk membuat perubahan pada file saat sedang digunakan oleh pengguna lain.

## KUNCI Format File - Informasi Lebih Lanjut

File LOCK dibuat oleh setiap aplikasi dan format filenya khusus untuk aplikasi tersebut. File kunci ini dapat disimpan dalam format teks maupun file biner.

Kehadiran file kunci mencegah akses sumber daya secara bersamaan ke beberapa file yang mencoba mengakses sumber daya tersebut. Salinan file asli dibuat dengan ekstensi .lock di akhiri namanya. Ini memberi tahu aplikasi lain untuk memiliki akses hanya baca ke file. Misalnya, resource.dat akan menjadi resource.data.lock.

Untuk bahasa pemrograman Ruby, Anda mungkin menemukan file **gemfile.lock**. Di sinilah Bundler mencatat versi persis yang diinstal. Jadi, ketika proyek/perpustakaan dipindahkan ke komputer lain, bundel yang berjalan akan melihat Gemfile untuk versi yang benar-benar relevan.

## Kunci File di Linux

Linux mendukung dua jenis kunci file: kunci penasehat dan kunci wajib.

* **Advisory Locks**: Jenis penguncian yang tidak diterapkan. Dalam hal ini, proses yang berpartisipasi bekerja sama satu sama lain secara eksplisit memperoleh kunci. Jika ini tidak memungkinkan, kunci penasehat diabaikan.

* **Kunci Wajib**: Dalam kasus penguncian Wajib, sistem operasi memberlakukan penguncian file dengan mencegah proses lain membaca atau menulis file. Ini tidak memerlukan kerja sama antar proses.

penguncian wajib tidak memerlukan kerja sama antara proses yang berpartisipasi. Setelah kunci wajib diaktifkan pada file, sistem operasi mencegah proses lain membaca atau menulis file.

## Referensi

* [GemFile dan Gemfile.lock di Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Mengunci di Linux](https://www.baeldung.com/linux/file-locking)

