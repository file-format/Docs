{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File TEX",
  "description":"Pelajari tentang format file TEX dan API yang dapat membuat dan membuka file TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu File TEX? ##

**TeX** adalah bahasa yang terdiri dari pemrograman serta fitur mark-up, yang digunakan untuk mengeset dokumen. Donald Knuth dari Stanford University, adalah pencipta sistem penyusunan huruf yang cerdas ini. Di seluruh dunia, TeX adalah pilihan utama penulis dan penerbit untuk menghasilkan dokumen teknis berkualitas tinggi. TeX melakukan pekerjaan luar biasa dalam memformat ekspresi matematika yang kompleks. Dalam hubungannya dengan phototypesetter berkualitas tinggi, TeX bersaing dengan hasil yang dihasilkan oleh sistem typesetting tradisional terbaik. Oleh karena itu dianggap sebagai sistem tipografi digital paling berkelas.

File input TeX didasarkan pada kode ASCII, sehingga memungkinkan berbagi naskah di antara penulis, manajer penerbitan, dan kritikus. Berbagai macam lingkungan komputasi, hampir setiap platform modern dan banyak platform lama mendukung TeX. Selain itu, TeX adalah perangkat lunak gratis, tersedia untuk berbagai konsumen. Banyak instalasi UNIX menggunakan troff UNIX dan TeX sebagai sistem pemformatannya untuk tujuan yang berbeda. Tugas penyusunan huruf lainnya dilakukan secara luar biasa dalam bentuk LaTeX, ConTeXt, dan paket makro lainnya.

## Sejarah Singkat ##

TeX dirancang dan ditulis oleh Donald Knuth pada tahun 1978. Guy Steele dari Massachusetts Institute of Technology merevisi input/output TeX untuk membuatnya berjalan di bawah sistem operasi yang tidak kompatibel seperti Timesharing System (ITS). Versi pertama TeX dikembangkan di bawah sistem operasi Stanford's WAITS in the programming language (SAIL) dan diuji untuk dijalankan pada PDP-10. Knuth memperkenalkan ide pemrograman melek huruf untuk versi lanjutan. Pemrograman Literate adalah cara untuk menghasilkan kode sumber yang dapat dikompilasi dan kumpulan huruf (dalam TeX) untuk dokumentasi yang terhubung silang menggunakan file asli. Bahasa yang digunakan untuk mengembangkan TeX versi lanjutan ini disebut WEB, campuran program Pascal DEC PDP-10 untuk memastikan portabilitas.

TeX versi baru yang direvisi diterbitkan pada tahun 1982 dan disebut TeX82. Perubahan besar adalah penggantian algoritma hyphenation asli dengan algoritma yang baru ditulis oleh Frank Liang. Untuk memastikan portabilitas di berbagai platform, Alih-alih menggunakan titik-mengambang, TeX82 menggunakan aritmatika titik-tetap bersama dengan bahasa pemrograman yang nyata dan lengkap turing. Pada tahun 1989, versi baru TeX dan Metafont dirilis. Jadi TeX versi 3.0 memfasilitasi input 8-bit, memungkinkan 256 karakter berbeda dalam teks. Setelah versi 3, pembaruan dilambangkan dengan menambahkan digit tambahan di akhir desimal, misalnya versi TeX saat ini diindikasikan sebagai 3.14159265. Versi ini terakhir diperbarui 12-1-2014.

## Masukan TeX ##

File input ke TEX dapat disiapkan dengan editor teks menggunakan teks biasa. Tidak seperti pengolah Word pada umumnya, file input ini melarang karakter kontrol yang tidak terlihat. Satu file dapat disematkan ke dalam file lain, berisi definisi makro dan definisi tambahan yang meningkatkan kemampuan TeX. Jika penginstalan TeX dilengkapi dengan file makro apa pun, informasi lokal tentang TeX menunjukkan tentang penggunaan file makro. Bentuk standar TeX, mengintegrasikan kombinasi makro dan definisi lain yang dikenal sebagai TEX biasa.

Berdasarkan pengetahuan yang tepat tentang ukuran semua karakter dan simbol, itu menghitung organisasi optimal huruf per baris dan baris per halaman. Pada saat pemrosesan dokumen, file .dvi dihasilkan, di mana "dvi" adalah singkatan dari "device independent". Program driver perangkat diperlukan untuk mencetak atau melihat pratinjau dokumen dengan ekstensi dvi. Saat ini, pembuatan dvi dilewati oleh pdf-TeX yang umum digunakan. Tidak ada pengetahuan font sebelumnya yang tersedia dalam instalasi TeX, jadi file font eksternal, yang merupakan bagian dari lingkungan TeX lokal digunakan untuk mendapatkan informasi untuk dokumen.

## Sistem Penataan ##

Sekitar 300 primitif (perintah) dapat dipahami oleh sistem dasar TeX. Primitif adalah perintah tingkat rendah, oleh karena itu pengguna umum jarang menggunakannya secara langsung dan sebagian besar fungsinya dilakukan oleh file format. File format ini adalah gambar memori TeX yang dimuat sebelumnya yang diikuti dengan pemuatan koleksi makro besar. Format default asli bahasa yaitu TeX biasa menambahkan sekitar 600 perintah.

Garis miring terbalik yang dikelompokkan dengan kurung kurawal menandakan dimulainya perintah TeX. Karena TeX adalah bahasa berbasis makro dan token, hampir semua karakteristik sintaksis TeX dapat diubah saat dijalankan, termasuk yang ditentukan pengguna kecuali token yang tidak dapat dikembangkan yang kemudian dieksekusi. Ekspansi itu sendiri praktis bebas masalah. Beberapa perintah perlu muncul setelah argumen yang membantu menjelaskan fungsi perintah. Misalnya, perintah \vskip mengarahkan TEX untuk melewatkan halaman ke bawah/ke atas diikuti dengan argumen yang menentukan berapa banyak ruang yang harus dilewati.

## Versi ##

LaTeX adalah format yang paling sering digunakan yang awalnya dikembangkan oleh Leslie Lamport. LaTeX mengintegrasikan berbagai gaya dokumen untuk file, surat, buku, dan slide serta menawarkan referensi dan penomoran otomatis untuk berbagai bagian dan ekspresi matematika. AMS-TeX adalah format populer lainnya, yang dikembangkan oleh American Mathematical Society.

AMS-TeX menawarkan lebih banyak perintah yang mudah digunakan, yang dapat didefinisikan ulang oleh jurnal agar sesuai dengan gaya lokal mereka. LaTeX dapat memanfaatkan AMS-TeX dengan menggunakan "paket" AMS yang kemudian disebut sebagai AMS-LaTeX. ConTeXt adalah format lain yang ditulis oleh Hans Hagen yang digunakan terutama untuk penerbitan desktop.

Perangkat lunak TeX menawarkan beberapa fitur yang tidak tersedia, atau kualitasnya lebih rendah, di sistem penyusunan huruf lain pada saat pembuatannya. Beberapa fitur inovatif dari bahasa ini didasarkan pada algoritme menarik yang berasal dari tesis siswa Knuth. Sementara program penyusunan huruf lainnya sekarang memasukkan fitur TeX yang berguna ke dalam program mereka.

## Referensi ##

* [Sistem Pengaturan Huruf TeX](https://en.wikipedia.org/wiki/TeX)

