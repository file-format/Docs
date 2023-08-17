{
  "date" : "2019-10-11",
  "keywords" :[ "file exif", "format file exif", "apa itu file exif", "file", "contoh exif", "ekstensi file exif", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Pelajari tentang format file EXIF dan API yang dapat membuat dan membuka file EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file EXIF?
EXIF adalah singkatan dari "Exchangeable Image File Format", definisi yang pertama kali diberikan oleh [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) pada tahun 1985. Standar ini dikelola oleh Japan Electronics dan Asosiasi Industri Teknologi Informasi (JEITA) mulai hari ini. EXIF adalah standar untuk spesifikasi format gambar dan suara yang terutama digunakan oleh kamera digital dan pemindai.

Standar EXIF mencakup informasi penandaan dan metadata dengan file gambar. Metadata dapat berisi informasi seperti model kamera, kecepatan rana, Tanggal dan waktu, apertur, pabrikan, waktu pencahayaan, resolusi X, resolusi Y, dll. Biasanya data EXIF disembunyikan secara default. Untuk melihat data EXIF, kita harus memilih properti tampilan dalam aplikasi tampilan gambar. Metadata Exif juga dapat menyertakan thumbnail bersama dengan data gambar teknis dan utama dalam satu file gambar.

## Sejarah dan Versi ##

* Pada Oktober 1995, JEIDA mendirikan Versi 1. Dalam versi ini JEIDA mendefinisikan struktur, yang terdiri dari format data gambar dan informasi atribut, dan tag dasar.
* Nov 1997, versi 1.1 diperkenalkan dengan sebagian besar tag dari versi 1 tetapi juga menambahkan ketentuan untuk informasi atribut opsional dan operasi format.
* Juni 1998, Versi 2 dengan ruang warna sRGB, thumbnail terkompresi, dan file audio.
* Desember 1998, Versi 2.1 dengan penyimpanan yang ditingkatkan dan informasi atribut.
* Februari 2002, Versi 2.2, perbaikan versi 2.1 dengan penambahan finishing cetak.
* September 2003, Versi 2.21 dengan ruang warna opsional yang dikenal sebagai adobe RGB.

## Format File EXIF

EXIF menggunakan format file berikut dengan penambahan metadata tertentu.

1. [JPEG](/id/image/jpeg/) - transformasi kosinus diskrit (DCT) untuk file gambar terkompresi.
1. [TIFF](/id/image/tiff/) Rev. 6.0 (RGB atau YCbCr) untuk file gambar yang tidak dikompresi.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) untuk file audio (Linear [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) atau ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM untuk data audio yang tidak terkompresi, dan [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) untuk data audio terkompresi).

### Penanda yang digunakan oleh EXIF ###

Marker 0xFFE0~~0xFFEF adalah "Application Marker", yang digunakan oleh aplikasi pengguna. Misalnya, kamera digital lama menggunakan JFIF (JPEG File Interchange Format) untuk menyimpan gambar. JFIF menggunakan APP0 (0xFFE0) Marker untuk memasukkan data konfigurasi digi cam dan gambar thumbnail. Selain itu, EXIF juga menggunakan Penanda Aplikasi untuk memasukkan data, tetapi EXIF menggunakan Penanda APP1 (0xFFE1) untuk menghindari konflik dengan format JFIF. Setiap format file EXIF dimulai dari format ini.


|SOI Marker|APP1 Marker|APP1 Data|Other Marker
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Dimulai dari SOI (0xFFD8) Marker, jadi ini adalah file JPEG. Kemudian Penanda APP1 segera mengikuti. Semua data EXIF disimpan di area data APP1 ini. Bagian "SSSS" pada tabel atas berarti ukuran area data APP1 (area data EXIF). Harap perhatikan bahwa ukuran "SSSS" juga mencakup ukuran deskriptor itu sendiri. Setelah "SSSS", data APP1 dimulai. Bagian pertama adalah data khusus untuk identifikasi apakah EXIF atau tidak, digunakan karakter ASCII "EXIF" dan 2 byte 0x00. Setelah area Penanda APP1, Penanda JPEG lainnya mengikuti.

### Struktur Data Exif ###

Struktur kasar data EXIF (APP1) ditampilkan seperti di bawah ini. Seperti yang telah dibahas di atas, data EXIF mulai dari karakter ASCII "EXIF" dan 2 byte 0x00, kemudian mengikuti data EXIF. EXIF menggunakan format TIFF untuk menyimpan data.


|FFE1|Penanda APP1
---|---|
|SSSS|Data APP1|Ukuran Data APP1
|45786966 0000|Tajuk Exif
|49492A00 08000000|TIFF Tajuk
|XXXX. . . .|IFD0 (gambar utama)|Direktori
|LLLLLLLL|Tautan ke IFD1
|XXXX. . . .|Area data IFD0
|XXXX. . . .|Exif SubIFD|Direktori
|00000000|Akhir Tautan
|XXXX. . . .|Area data Exif SubIFD
|XXXX. . . .|IFD1(gambar mini)|Direktori
|00000000|Akhir Tautan
|XXXX. . . .|Area data IFD1
|FFD8XXXX. . . XXXXFFD9|Gambar mini

#### Tajuk TIFF ####

header file [TIFF](/id/image/tiff/) 8-byte berisi informasi berikut:

`Bytes 0-1:` Urutan byte yang digunakan dalam file. Nilai hukumnya adalah:“II”(4949.H)“MM” (4D4D.H).

Dalam format "II", urutan byte selalu dari byte paling signifikan ke byte paling signifikan, untuk bilangan bulat 16-bit dan 32-bit. Ini disebut urutan byte little-endian. Dalam format "MM", urutan byte selalu dari yang paling signifikan hingga yang paling tidak signifikan, untuk bilangan bulat 16-bit dan 32-bit. Ini disebut urutan byte big-endian.

`Bytes 2-3:` Nomor acak tetapi dipilih dengan hati-hati (42) yang selanjutnya mengidentifikasi file sebagai file TIFF. Urutan byte bergantung pada nilai Byte 0-1.

`Bytes 4-7:` Offset (dalam byte) dari IFD pertama. Direktori boleh berada di sembarang lokasi dalam file setelah header tetapi harus dimulai pada batas kata. Secara khusus, Direktori File Gambar dapat mengikuti data gambar yang dijelaskannya. Pembaca harus mengikuti penunjuk ke mana pun petunjuk itu mengarah. Istilah byte offset selalu digunakan dalam dokumen ini untuk merujuk ke lokasi sehubungan dengan awal file TIFF. Byte pertama dari file memiliki offset 0.

#### Direktori File Gambar ####

Sebuah IFD berisi informasi tentang gambar serta penunjuk ke data gambar sebenarnya. Ini terdiri dari hitungan 2-byte dari jumlah entri direktori (yaitu jumlah bidang), diikuti dengan urutan entri bidang 12-byte , diikuti dengan offset 4 byte dari IFD berikutnya (atau 0 jika tidak ada). Harus ada setidaknya 1 IFD dalam file TIFF dan setiap IFD harus memiliki setidaknya satu entri.

##### Entri IFD #####

Setiap Entri IFD 12-byte dalam format berikut.


|Byte|Deskripsi
---|---|
|0-1|Tag yang mengidentifikasi bidang
|2-3|Jenis kolom
|4-7|Jumlah dari jenis yang ditunjukkan
|8-11|The Value Offset, file offset (dalam byte) dari Nilai untuk field.Nilai diharapkan dimulai pada batas kata; dengan demikian, Value Offset yang sesuai akan menjadi angka genap. File ini mengimbangi titik di mana saja dalam file, bahkan setelah data gambar

Bidang TIFF adalah entitas logis yang terdiri dari tag TIFF dan nilainya. Konsep logis ini diimplementasikan sebagai Entri IFD, ditambah nilai sebenarnya jika tidak sesuai dengan bagian nilai/offset, 4 byte terakhir dari Entri IFD. Istilah bidang TIFF dan entri IFD dapat dipertukarkan di sebagian besar konteks.

#### Gambar Thumbnail ####

Format exif berisi thumbnail gambar (kecuali Ricoh RDC-300Z). Biasanya terletak di sebelah IFD1. Ada 3 format untuk thumbnail; Format JPEG (JPEG menggunakan YCbCr), format TIFF RGB, format TIFF YCbCr.

##### Gambar Kecil Format JPEG #####

Jika nilai Compression(0x0103) Tag di IFD1 adalah '6', format gambar thumbnail adalah JPEG. Sebagian besar gambar Exif menggunakan format JPEG untuk thumbnail. Dalam hal ini, Anda bisa mendapatkan offset thumbnail dengan Tag JpegIFOffset(0x0201) di IFD1, ukuran thumbnail dengan Tag JpegIFByteCount(0x0202). Format data adalah format JPEG biasa, dimulai dari 0xFFD8 dan diakhiri dengan 0xFFD9. Tampaknya format JPEG dan ukuran 160x120piksel adalah format thumbnail yang direkomendasikan untuk Exif2.1 atau lebih baru.

##### Gambar Kecil Format TIFF #####

Jika nilai Compression(0x0103) Tag pada IFD1 adalah '1', format gambar thumbnail adalah tanpa kompresi (disebut gambar TIFF). Titik awal data thumbnail adalah Tag StripOffset(0x0111), ukuran thumbnail adalah jumlah dari Tag StripByteCounts(0x0117).

## Referensi ##

* [EXIF - Oleh Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [Format File EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

