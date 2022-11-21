{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File CGM",
  "description":"Pelajari tentang format file CGM dan API yang dapat membuat dan membuka file CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file CGM? ##

Computer Graphics Metafile (CGM) adalah format metafile standar internasional gratis, independen platform, untuk menyimpan dan bertukar grafik vektor (2D), grafik raster, dan teks. CGM menggunakan pendekatan berorientasi objek dan banyak ketentuan fungsi untuk produksi gambar. CGM menggunakan karakteristik berorientasi objek ini untuk membentuk kembali elemen grafis untuk merender gambar. Metafile berisi informasi penting yang mendefinisikan file lain. Di CGM, file sumber berbasis teks berisi semua elemen grafis yang nantinya dapat dikompilasi menjadi file biner. Pada dasarnya, CGM adalah cara untuk memfasilitasi pertukaran data grafis 2D, terlepas dari platform atau perangkat tertentu.

Format CGM menyediakan elemen yang berbeda untuk menjalankan fungsi, dan menandakan objek untuk menyesuaikan primitif geometris dan informasi grafis. Meskipun CGM telah digantikan oleh format lain untuk menampilkan seni grafis pada halaman web karena tidak didukung dengan baik oleh halaman web, masih sangat populer di kalangan industri, penerbangan, dan aplikasi teknis lainnya. Meskipun World Wide Web Consortium telah mengembangkan WebCGM, sebuah pendekatan alternatif untuk penggunaan CGM di Web. Implementasi CGM primer merupakan gambaran urutan operasi dasar dari Graphical Kernel System (GKS). Itu belum banyak diadopsi dalam desain profesional tetapi sebagian besar telah digantikan oleh format lain seperti DXF dan SVG.

## Sejarah ##

CGM ternyata menjadi standar internasional pada tahun 1987 (ISO 8632-1987) dan juga diadopsi sebagai standar nasional di Inggris oleh BSI dan Amerika Serikat oleh ANSI. Setelah sejumlah amandemen pada tahun 1991, standar CGM yang direvisi dirilis pada tahun 1992 (ISO 8632:1992). Pada tahun 2001, World Wide Web Consortium mengembangkan WebCGM dengan kemampuan yang ditingkatkan untuk digunakan dengan halaman web. Pada tahun 2007 versi kedua WebCGM dirilis dan versi ketiga dirilis pada tahun 2010 dengan kemampuan yang ditingkatkan.

## Format File CGM ##

Metafile grafis komputer pada dasarnya adalah basis data untuk informasi grafis dan menyediakan sarana untuk menangkap, menyimpan, dan mentransmisikan data grafis. Konsekuensinya, harus ada komponen sistem grafis untuk membuat database secara bersamaan bersamaan dengan eksekusi aplikasi dalam format metafile. Dalam kebanyakan kasus, komponen ini adalah generator Metafile. Di samping itu, ada kebutuhan untuk komponen lain yang dapat mengambil, menafsirkan, dan merender data grafis dalam metafile. Kebutuhan ini dipenuhi dengan adanya interpreter metafile. Gambar berikut mewakili lingkungan kerja metafile grafis.

Hubungan CGM dengan komponen lain dari sistem grafis tipikal diilustrasikan pada gambar di atas. Terlihat juga dari gambar bahwa fungsionalitas metafile tidak bergantung pada keluaran akhir perangkat.

Umumnya, ada dua kategori metafile: **pengambilan bagian** dan **pengambilan gambar**. Fungsionalitas utama dari metafile pengambilan gambar adalah menangkap beberapa definisi gambar yang tidak bergantung pada perangkat. Sementara metafile tangkapan sesi menggunakan antarmuka sistem untuk menangkap dialog keluaran dalam sistem grafis. CGM termasuk dalam kategori metafile pengambilan gambar statis. CGM menyediakan pengaturan komponen yang terorganisir dengan baik dengan struktur dua tingkat.

1. Deskriptor Metafile
1. Kumpulan gambar yang independen secara logis

Setiap gambar adalah kumpulan deskriptor gambar dan badan gambar termasuk definisi gambar. deskriptor metafile mendefinisikan informasi deskriptif yang sama-sama berlaku untuk semua gambar metafile itu. Informasi ini membantu juru bahasa untuk mengurai metafile dengan benar dan mengenali sumber daya yang diperlukan untuk rendering gambar yang benar. Meskipun deskriptor gambar juga menyertakan informasi deskriptif namun hanya dapat mengenali gambar di mana deskriptor berada. Dalam format file ini, setiap definisi gambar mandiri dan berdaulat secara logis. Mereka tidak bergantung pada semua definisi gambar lainnya dalam sebuah file. Tepat setelah interpretasi meta-deskriptor, gambar dapat diakses dan diinterpretasikan secara acak. Perubahan keadaan gambar sebelumnya tidak berpengaruh pada penerusnya. Kemandirian gambar ini adalah fitur lain yang menonjol dari CGM.CGM terdiri dari ruang koordinat yang merupakan koordinat Cartesian 2D yang disebut koordinat perangkat virtual dan dapat direpresentasikan melalui angka atau presisi yang mewakili jangkauan dan perincian. CGM menentukan pemilihan warna langsung dan pemilihan berbasis indeks. Yang pertama, penentu warna terdiri dari tiga kali lipat RGB sementara kemudian, penentu warna menunjukkan indeks ke dalam tabel warna.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
