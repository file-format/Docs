{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - File Pertukaran Data LIDAR Terkompresi",
  "description":"Pelajari tentang format file LAZ dan API yang dapat membuat dan membuka file LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Apa itu File LAZ?

Format file LAZ adalah versi terkompresi dari format file LAS (Lidar LASer), yang dirancang khusus untuk menyimpan data cloud titik lidar. File LAZ mempertahankan data dan struktur yang sama dengan file LAS tetapi menggunakan teknik kompresi lossless untuk mengurangi ukuran file sekaligus menjaga keakuratan data asli.

## Format File LAZ - Sejarah Singkat

Format file LAZ dikembangkan untuk memenuhi permintaan yang terus meningkat akan penyimpanan yang efisien dan transmisi kumpulan data lidar besar. Dengan mengompresi file LAS, file LAZ secara signifikan mengurangi ukurannya, membuatnya lebih mudah untuk dikelola dan ditransfer. Kompresi dicapai dengan menggunakan kombinasi algoritma yang berbeda, seperti pengkodean entropi dan pengkodean panjang variabel, untuk merepresentasikan atribut titik lidar dalam bentuk yang lebih ringkas.

## Format File LAZ

Meskipun dikompresi, file LAZ tetap memiliki kemampuan untuk memulihkan sepenuhnya data LAS asli tanpa kehilangan informasi apa pun. Artinya, setelah file LAZ didekompresi, file tersebut dapat diproses dan dianalisis dengan cara yang sama seperti file LAS yang tidak dikompresi. Proses kompresi dan dekompresi biasanya dilakukan menggunakan perangkat lunak atau perpustakaan khusus yang mendukung format LAZ.

Format file LAZ menjaga kompatibilitas dengan file LAS, memastikan interoperabilitas di seluruh perangkat lunak lidar dan alat pemrosesan. Ini berarti aplikasi yang dapat membaca dan memproses file LAS biasanya dapat menangani file LAZ tanpa modifikasi apa pun. Selain itu, file LAZ masih menyertakan header file, catatan panjang variabel (VLR), dan catatan data titik, dengan mempertahankan struktur yang sama seperti file LAS.

## Keuntungan Format File LAZ

**Ukuran File Berkurang:** Kompresi LAZ secara signifikan mengurangi ukuran file kumpulan data lidar, menjadikannya lebih mudah dikelola dan disimpan serta ditransfer.

**Integritas Data:** Kompresi LAZ bersifat lossless, artinya data yang didekompresi merupakan replika yang sama persis dari data LAS asli, sehingga memastikan tidak ada kehilangan informasi atau presisi.

**Interoperabilitas:** File LAZ kompatibel dengan file LAS, memungkinkan integrasi yang lancar dengan perangkat lunak dan alur kerja lidar yang ada.

**Pemrosesan yang Efisien:** Karena ukurannya yang lebih kecil, file LAZ dapat dimuat dan diproses lebih cepat, sehingga meningkatkan waktu pemrosesan dan analisis secara keseluruhan.

Format file LAZ telah diadopsi secara luas di komunitas lidar sebagai standar untuk penyimpanan dan pertukaran data lidar terkompresi. Ini menawarkan keseimbangan antara kompresi data yang efisien dan integritas data, memungkinkan penanganan kumpulan data lidar besar dengan lebih mudah sambil menjaga keakuratan dan kualitas data asli.

## Referensi

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
