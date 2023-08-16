{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Format File", "CAD", "Buka", "Buat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DWG dan API yang dapat membuat dan membuka file DWG.",
  "title" :"Format File DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DWG?

File dengan ekstensi DWG mewakili file biner eksklusif yang digunakan untuk memuat data desain 2D dan 3D. Seperti DXF, yang merupakan file ASCII, DWG mewakili format file biner untuk gambar CAD (Computer Aided Design). Ini berisi gambar vektor dan metadata untuk representasi konten file CAD. Ada pemirsa gratis yang tersedia untuk melihat file DWG di Sistem Operasi Windows seperti DWG TrueView gratis dari Autodesk. Ada juga aplikasi pihak ketiga lainnya yang mendukung penjangkauan file DWG. File DWG berisi informasi yang dibuat pengguna dan termasuk:

* Desain
* Data geometris
* Peta dan foto

Format ini banyak digunakan oleh arsitek, insinyur, dan desainer untuk berbagai keperluan desain.

## Sejarah Singkat ##

Format file DWG telah berkembang seiring waktu sejak diperkenalkan secara formal pada tahun 1982. Gambaran singkat tentang peristiwa masa lalu dari perspektif sejarah adalah sebagai berikut.

**1982:** Autodesk melisensi format file DWG , yang dikembangkan oleh Mike Riddle pada tahun 1970, sebagai dasar AutoCAD.

**1998:** Dengan dirilisnya AutoCAD R14.01, Autodesk menambahkan verifikasi file melalui fungsi yang disebut DWGCHECK yang menyematkan checksum terenkripsi dan kode produk, yang disebut WaterMark oleh Autodesk, ke dalam file DWG yang dibuat oleh program.

**2006:** Autodesk memodifikasi AutoCAD 2007, untuk menyertakan "Teknologi DWG Tepercaya" untuk menyematkan string teks "Autodesk DWG. File ini adalah DWG Tepercaya yang terakhir disimpan oleh aplikasi Autodesk atau aplikasi berlisensi Autodesk" ke dalam file DWG. Tujuan dari ini adalah untuk membantu pengguna perangkat lunak Autodesk memastikan bahwa file-file ini dibuat oleh aplikasi Autodesk atau RealDWG, yang pasti akan membantu mengurangi risiko ketidakcocokan.

## Struktur File ##

DWG telah menjadi salah satu format file yang banyak digunakan oleh berbagai aplikasi dan memiliki struktur file yang kuat. Karena DWG adalah format file biner, DWG tidak dapat dibaca manusia seperti format file ASCII [DXF](/id/cad/dxf/) biasa. File DWG biasanya menyertakan informasi tentang koordinat gambar dan metadata apa pun yang terkait dengannya. [Spesifikasi](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) lengkap format file DWG tersedia untuk diunduh oleh OpenDesign. Struktur file format file DWG dirangkum sebagai berikut.

**Header**: File header terdiri dari variabel DWG Header dan informasi tentang Cyclic Redundancy Check (CRC) yang digunakan untuk deteksi kesalahan. Setiap subbagian adalah vektor khusus di mana panjang bit yang berbeda digunakan untuk mewakili label yang berbeda. Misalnya, 6 bit pertama dari variabel DWG Header adalah string versi.

**Definisi Kelas:** File DWG mungkin berisi banyak kelas tergantung pada tujuan file .dwg tertentu. Informasi seperti ukuran metadata kelas dari area data kelas, nomor kelas dan checksum di samping yang lain.

**Template**: Ini opsional dan untuk versi R15 dan R15, bagian ini berada di bawah bagian Object Free Space.

**Padding**: Metadata diberi sufiks dan postfix dengan sejumlah byte tertentu yang membuat versi perangkat lunak AutoCAD yang lebih lama kompatibel dengan format file DWG yang baru.

**Data Gambar**: Metadata untuk bagian ini bergantung pada jenis .dwg tertentu. Untuk pengguna R14 dan R15, bagian ini bersifat opsional.

**Data Objek**: Data objek terdiri dari daftar lengkap entitas tabel, entri kamus, dll. yang sesuai dengan daftar objek yang ada.

**Peta Objek**: Lokasi setiap objek dalam file ditentukan di bagian file ini. Sebagian besar metadata di bagian ini adalah pegangan file yang berperan dalam identifikasi dan rendering ulang objek.

**Ruang Bebas Objek**: Bagian ini bersifat opsional untuk semua pengguna

**Header Kedua**: Duplikat bagian header file menjelang akhir file DWG

## Referensi ##

* [Spesifikasi Format File DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Spesifikasi File DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - Oleh Wikipedia](https://en.wikipedia.org/wiki/.dwg)

