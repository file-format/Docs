{
  "date" : "2019-10-11",
  "keywords" :[ "file jp2", "format file jp2", "apa itu file jp2", "file", "contoh jp2", "ekstensi file jp2", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Format Berkas Gambar",
  "description":"Pelajari tentang format file JP2 dan API yang dapat membuat dan membuka file JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Apa itu file JP2? ##

JPEG 2000 (**JP2**) adalah sistem pengkodean gambar dan standar kompresi gambar yang canggih. Itu menggunakan teknologi wavelet untuk mengkodekan konten lossless dalam kualitas apa pun sekaligus. Selain itu, tanpa penalti besar dalam efisiensi pengkodean, JPEG 2000 memiliki kemampuan untuk mengakses dan mendekodekan konten yang sama secara efektif ke dalam berbagai resolusi dan kualitas lainnya. Aliran kode dalam JPEG 2000 secara signifikan dapat diskalakan memiliki wilayah minat yang menyediakan fasilitas untuk akses acak spasial.

JPEG 2000 menonjol sebagai salah satu standar yang paling dapat diskalakan. Bagian yang berbeda dari suatu gambar dapat disimpan menggunakan beragam kualitas. Peningkatan kinerja yang patut diperhatikan dapat dicapai dengan mengurutkan aliran kode dalam berbagai cara. Namun demikian, JP2 memerlukan pembuat enkode/dekoder yang kompleks dan menantang secara komputasi, sebagai hasil dari fleksibilitas ini. Dibandingkan dengan JPEG, JPEG 2000 hanya menghasilkan artefak dering yang membuat cincin di dekat tepi gambar dan dapat buram, sedangkan JPEG menggunakan blok artefak visual 8×8 yang dapat berupa artefak dering dan pemblokiran. Memiliki hingga 16384 komponen yang beragam dengan dimensi dalam terapixels, dan presisi yang dapat setinggi 38 bit/sampel.

## Sejarah ##

Pada tahun 2000, komite Joint Photographic Experts Group merancang JP2 dengan tujuan untuk meningkatkan standar JPEG berbasis transformasi kosinus diskrit mereka sendiri dengan metode berbasis gelombang kecil ini. Komite JPEG bertujuan untuk menyediakan metode dasar mereka tanpa biaya lisensi. Dalam lisensi JP2 yang mendapatkan persaingan di antara 20 perusahaan, mereka menang tipis. JPEG 2000 telah dinyatakan sebagai standar ISO, meskipun sebagian besar browser web belum siap untuk membantu JPEG 2000 sejak 2017.

## Bagian dari sistem pengkodean gambar JPEG 2000 ##

Berikut ini adalah bagian utama yang merupakan rangkaian lengkap standar untuk JPEG 2000.


|Bagian|Judul|Uraian|Nomor
---|---|---|---|
|Bagian 1|Sistem pengkodean inti| Mendefinisikan sintaks aliran kode. Berbagai tahapan terlibat dalam mendekode gambar JPEG 2000. Menjelaskan format file dasar JP2, metadata, dan hak IP yang harus disediakan.|ISO/IEC 15444-1
|Bagian 2|Ekstensi|Mendefinisikan ekstensi untuk aliran kode format file dan memungkinkan demonstrasi sampel HDR, spesifikasi ruang warna, pemangkasan, transformasi geometris; beragam animasi, metadata, dan banyak aliran kode.|ISO/IEC 15444-2
|Bagian 3|Motion JPEG 2000 (MJ2 atau MJP2)|Memperkenalkan format file untuk rangkaian gerakan, menyandikan gambar dalam aliran kode independen.|ISO/IEC 15444-3
|Bagian 4|Kesesuaian|Menyatakan teknik pengujian untuk encoding dan decoding dan memeriksa file untuk stream kode telanjang dan file JP2.|ISO/IEC 15444-4
|Bagian 5|Perangkat lunak referensi|Terdiri dari dua paket kode sumber (Java, C) yang mengimplementasikan sistem pengkodean Inti dan tersedia di bawah lisensi sumber terbuka.|ISO/IEC 15444-5
|Bagian 6|Format file gambar majemuk|Mendefinisikan format file JPM dan memungkinkan pencitraan dokumen multi-halaman untuk aplikasi seperti faks. Mendukung penggunaan JBIG2 dan JPEG.|ISO/IEC 15444-6
|Bagian 8|JPEG 2000 Secured (JPSEC)|Memastikan keamanan transaksi, konten, dan teknologi, dan memungkinkan streaming bit JPEG 2000 yang aman.|ISO/IEC 15444-8
|Bagian 9|JPIP|Mendefinisikan alat dalam lingkungan jaringan untuk mengakses metadata dan gambar, dan menyatakan protokol Interaktif dan efisien|ISO/IEC 15444-9
|Bagian 10|JP3D|Ekstensi volumetrik dari Bagian 1 dan memperkenalkan dimensi Z. Memperluas konsep petak, blok kode, kawasan sekitar, dan fitur aksesibilitas wilayah minat 3D.|ISO/IEC 15444-10
|Bagian 11|JPWL|Berurusan dengan transmisi yang terorganisir dengan baik melalui jaringan nirkabel yang rawan kesalahan. Ekstensi ini kompatibel dengan decoder|ISO/IEC 15444-11
|Bagian 13|Encoder level awal|Mendefinisikan implementasi encoder level awal dari sistem pengkodean Inti.|ISO/IEC 15444-13
|Bagian 14|JPXML|Representasi dalam XML dan menjelaskan segmen penanda dan metode untuk mengakses data internal citra.|ISO/IEC 15444-14
|Bagian 15|HTJ2K (Dalam pengembangan)|Menentukan algoritme pengkodean blok alternatif. Algoritma menawarkan throughput sepuluh kali lipat dan coding/decoding lossless.|

## Format File JP2 ##

JPEG 2000 mendefinisikan format file serta aliran kode dengan cara yang sama seperti JPEG-1. Meskipun sampel gambar secara eksklusif dijelaskan oleh JPEG 2000, namun JPEG-1 menyertakan informasi tambahan lainnya tentang ruang warna dan resolusi penting untuk menyandikan gambar. Jika gambar disimpan sebagai file JPEG 2000, **.jp2** digunakan sebagai ekstensi. Format file ini semakin ditingkatkan dengan ekstensi JPEG 2000 part-2, yang mendefinisikan mekanisme animasi dan konfigurasi berbagai aliran kode menjadi satu gambar tunggal. Ekstensi **.jpx** digunakan saat gambar disimpan menggunakan format file yang diperluas ini. Karena data aliran kode tidak dianggap disimpan dalam file terutama, maka tidak ada ekstensi standar yang ditentukan untuk tujuan ini. Meskipun untuk tujuan pengujian, sering mendapatkan ekstensi **.jpc** atau **.j2k**. Berbeda dengan JPEG-1, JPEG 2000 memilih cara berbeda untuk menyandikan metadata dalam format XML. Standar 12234-1.4 (oleh komite ISO TC42) digunakan sebagai referensi antara tag Exif dan komponen XML. JPEG 2000 dapat berisi standar ISO, XMP di dalamnya.

### Potongan ###
File JPEG 2000 terdiri dari potongan berurutan. Setiap potongan memiliki header 8 byte: ukuran potongan 4-byte (big-endian, byte tinggi pertama) dan tipe potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "jP " atau "jP2".

Chunk kedua harus bertipe "ftyp" dan memiliki sub-tipe pada offset 8. JPEG 2000 ditentukan oleh sub-tipe yang harus berupa salah satu nilai: "jp2 "(tipe file \*.JP2), "jp20" (file ketik \*.JPA), "jpm " (jenis berkas \*.JPM), "jpx " (jenis berkas \*.JPX).

Pengulangan potongan, hingga jenis yang tidak diketahui terdeteksi, kami membuat file gambar/video JPEG 2000.

### Transformasi warna ###

Awalnya, transformasi gambar dari ruang warna RGB ke ruang warna lain diperlukan. Untuk tujuan ini, ada dua cara: Irreversible Color Transform (ICT) dan Reversible Color Transform (RCT). Mantan menggunakan YC,,B,,C,,R,, ruang warna dan harus diimplementasikan dalam fix/floating –point sementara kemudian ruang warna YUV dimodifikasi dan bersifat reversibel.// //Tidak terbatas pada model RGB, JPEG Bahasa 2000 menggunakan transformasi banyak komponen.

### Ubin ###

Saat transformasi warna selesai, gambar diubah menjadi wilayah persegi panjang yang disebut ubin yang dapat diubah dan dikodekan secara terpisah. Ukuran semua petak akan sama atau keseluruhan gambar dapat dianggap sebagai satu petak tunggal. Decoder memanfaatkan ubin dan mengkonsumsi lebih sedikit memori atau dapat mengkodekan sebagian ubin. Padahal teknik ini memiliki kelemahan yaitu penurunan kualitas gambar.

### Transformasi wavelet ###

Gambar setelah ubin ditransformasikan menjadi wavelet yang dapat berupa ireversibel atau reversibel dan diimplementasikan dengan menggunakan skema konvolusi atau pengangkatan.

### Rasio kompresi ###

Bergantung pada karakteristik fisik dari sebuah gambar, keuntungan kompresi sebesar 20% diperoleh Prediksi redundansi spasial dari JPEG 2000 memainkan peran penting dalam proses kompresi dan gambar beresolusi tinggi cenderung mendapatkan keuntungan terbesar.

## Aplikasi dilayani oleh standar ##

* Merekam, mengedit, dan menyimpan video HD berbasis bingkai
* Citra medis & biometrik
* Citra satelit, penginderaan jauh dan deteksi gerak
* Komunikasi klien/server, distribusi dan penyimpanan jaringan.
* Sinema digital, kontribusi umpan HDTV Langsung, hal-hal Audio-visual Digital

## Referensi ##

* [Ringkasan JPEG 2000](https://jpeg.org/jpeg2000/)
* [Sistem pengkodean gambar JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

