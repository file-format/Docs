{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "file", "format", "jenis file", "ekstensi", "apa itu file 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file 3DS dan API yang dapat membuka dan membuat file 3DS.",
  "title" :"Format File 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file 3DS?

File dengan ekstensi .3ds mewakili format file mesh 3D Sudio (DOS) yang digunakan oleh Autodesk 3D Studio. Autodesk 3D Studio telah berada di pasar format file 3D sejak 1990-an dan kini telah berevolusi menjadi 3D Studio MAX untuk bekerja dengan pemodelan, animasi, dan rendering 3D. File 3DS berisi data untuk representasi 3D dari adegan dan gambar dan merupakan salah satu format file populer untuk impor dan ekspor data 3D. Ini mempertimbangkan informasi seperti lokasi kamera, data Mesh, informasi pencahayaan, konfigurasi viewport, data grup pemulusan, referensi bitmap, dan atribut untuk membuat simpul dan poligon untuk merender pemandangan.

## Format File 3DS - Informasi Lebih Lanjut
Pada dasarnya, 3DS adalah format file biner dan mengikuti struktur yang telah ditentukan sebelumnya untuk menyimpan dan mengambil data. Format file biner memungkinkan format file 3DS lebih cepat lebih kecil dibandingkan dengan format file berbasis teks. Data di dalam file 3DS disimpan dalam bentuk potongan.

### Potongan 3DS

Setiap potongan dalam file 3DS adalah blok data yang berisi ID, panjang blok untuk lokasi blok berikutnya, dan data itu sendiri. ID potongan memungkinkan pembaca format file 3DS melewati blok yang tidak mereka kenali. Ini juga membantu dalam ekstensibilitas format. Setiap bongkahan menyimpan informasi yang berkaitan dengan bentuk, pencahayaan, dan informasi tampilan yang bersama-sama merender pemandangan. Potongan disusun dalam struktur hierarkis dalam file 3DS dan menyerupai pohon Objek Dokumen XML dalam representasi.

**Chunk ID:** Dua byte pertama dari chunk mewakili pengenal chunk yang memungkinkan pembaca file memutuskan apakah akan mempertimbangkannya selama membaca atau melewatkannya.

**Panjang potongan:** Chunk ID diikuti oleh bilangan bulat 4-byte (dalam little-endian) yang menunjukkan panjang potongan. Panjang ini juga mencakup panjang data, panjang sub-bloknya, dan header 6-byte.

**Muatan:** Panjang potongan diikuti oleh byte data aktual untuk potongan tersebut, diikuti oleh sub-potongannya dalam struktur hierarki yang sama yang dapat diperluas ke kedalaman beberapa level.

### Struktur Potongan

Struktur hierarkis dari potongan sederhana adalah seperti yang ditunjukkan di bawah ini:

**Sepotong**

|awal|akhir|ukuran|nama
--- | --- | --- | ---
|0|1|2|ID potongan
|2|5|4|Potongan Selanjutnya

Potongan memiliki hierarki yang dikenakan pada mereka yang diidentifikasi oleh ID-nya. File 3ds memiliki ID potongan Utama 4D4Dh. Ini selalu merupakan bagian pertama dari file. Dengan di bagian utama adalah potongan utama.

**Potongan Utama**

|id|Deskripsi
--- | ---
|3D3D|Mulai dari data jaring objek.
|B000|Mulai dari data keyframer.

Pointer Potongan Berikutnya setelah blok ID menunjuk ke potongan Utama berikutnya.
Langsung setelah potongan Utama ada potongan lain. Ini bisa berupa jenis bongkahan lain yang diperbolehkan dalam lingkup bongkahan utamanya.
Untuk deskripsi Mesh (3D3D) jumlahnya bisa berapa saja.

**Subpotongan 3D3D - Blok Jala**


|id|Deskripsi
--- | ---
|1100|tidak diketahui
|1200|Warna Latar Belakang.
|1201|tidak diketahui
|1300|tidak diketahui
|1400|tidak diketahui
|1420|tidak diketahui
|1450|tidak diketahui
|1500|tidak diketahui
|2100|Blok Warna Sekitar
|2200|kabut?
|2201|kabut?
|2210|kabut?
|2300|tidak diketahui
|3000|tidak diketahui
|4000|Blok Objek
|7001|tidak diketahui
|AFFF|tidak diketahui

**Subpotongan dari 4000 - Blok Deskripsi Objek**
Item pertama Subchunk 4000 adalah string ASCIIZ dari nama objek.
Ingat sebuah objek bisa berupa jaring, cahaya atau kamera.

|id|Deskripsi
--- | ---
|4010|tidak diketahui
|4012|bayangan?
|4100|Objek Poligon Segitiga
|4600|Cahaya
|4700|Kamera

## Referensi

* [Format File Geometri - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - Oleh Wikipedia](https://en.wikipedia.org/wiki/.3ds)
