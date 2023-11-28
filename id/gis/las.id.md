{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Format File Lidar LASer",
  "description":"Pelajari tentang format file LAS dan API yang dapat membuat dan membuka file LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Apa itu File LAS?

Format file LAS (Lidar LASer) adalah format file biner yang dirancang khusus untuk menyimpan data lidar point cloud. Ini dikembangkan dan dikelola oleh American Society for Photogrammetry and Remote Sensing (ASPRS) sebagai format standar untuk pertukaran data dan interoperabilitas lidar.

File LAS menyimpan informasi terperinci tentang masing-masing titik lidar, termasuk koordinat 3D (x, y, dan z), nilai intensitas, kode klasifikasi, dan atribut tambahan. Format ini mendukung data pengembalian diskrit dan data lidar bentuk gelombang penuh, memungkinkan penyimpanan beberapa pengembalian per pulsa laser.

## Format Berkas LAS

Struktur file LAS terdiri dari tiga bagian utama: header file, catatan panjang variabel (VLR), dan catatan data titik.

1. File Header: File header berisi informasi penting tentang file LAS, seperti versi format data, format data titik, jumlah titik, koordinat kotak pembatas, sistem referensi koordinat (CRS), dan metadata lainnya. Ini memberikan ringkasan data lidar yang terkandung dalam file.

2. Catatan Panjang Variabel (VLR): VLR bersifat opsional dan dapat menyimpan metadata tambahan dan informasi khusus tentang data lidar. VLR memungkinkan fleksibilitas dalam memperluas format untuk mengakomodasi kebutuhan pengguna tertentu. Contoh VLR mencakup informasi tentang sistem sensor, parameter pemrosesan data, atau skema klasifikasi.

3. Catatan Data Titik: Catatan data titik menyimpan pengukuran lidar sebenarnya. Setiap rekaman data titik mewakili satu titik lidar dan berisi atribut seperti koordinat x, y, dan z, nilai intensitas, kode klasifikasi (misalnya, tanah, vegetasi, bangunan), dan atribut lain yang ditentukan pengguna. Catatan titik juga dapat menyimpan stempel waktu, jumlah pengembalian, dan sudut pemindaian.

File LAS mendukung format data yang berbeda (0 hingga 10) untuk mengakomodasi berbagai jenis data lidar dan tingkat informasi yang dibutuhkan. Misalnya, format 0 mewakili format titik sederhana dengan informasi dasar, sedangkan format 1 hingga 3 menyediakan data yang lebih komprehensif termasuk informasi bentuk gelombang untuk setiap pengembalian.

File LAS didukung secara luas oleh perangkat lunak dan alat pemrosesan lidar, menjadikannya format standar untuk pertukaran dan analisis data lidar. Selain itu, file LAS dapat dikompresi menggunakan teknik kompresi lossless untuk mengurangi ukuran file sekaligus menjaga keakuratan data asli. Versi terkompresi dari file LAS sering disebut sebagai LAZ, yang menawarkan kemampuan penyimpanan dan transfer data yang efisien.

## Referensi

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
