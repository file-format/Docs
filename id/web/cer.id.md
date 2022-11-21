{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "ekstensi", "file", "format", "web", "sertifikat", "bahasa" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Format File Sertifikat",
  "description":"Pelajari tentang format file CER dan API yang dapat membuat dan membuka file CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Apa itu file CER? ##

File dengan ekstensi .cer bertanggung jawab untuk menyimpan beberapa informasi tentang sertifikat pemilik dan kunci publik tertentu. Format file ini tidak dapat menyimpan kunci pribadi dan hanya memiliki kapasitas untuk menyimpan satu sertifikat yaitu x509. Otoritas sertifikat yang diamankan secara khusus adalah milik HTTPS, protokol tepercaya dan aman untuk penelusuran
CER adalah sertifikat dari server Anda. Biasanya diterima oleh otoritas sertifikat untuk domain. CER sebagian besar dianggap sama dengan [CRT](/id/web/crt/), meskipun keduanya merupakan format sertifikat SSL yang sama tetapi merupakan ekstensi nama file yang berbeda.
Ini dapat digunakan pada sistem operasi hanya dengan membuka browser dan memeriksa keamanan browser atau situs web yang digunakan.

## Sejarah Singkat ##

Pada tahun 1995, Thawte menjadi otoritas sertifikasi pertama untuk menyelesaikan masalah sertifikat SSL (secure socket link) publik di luar AS. Setelah itu, ada sederet otoritas yang berdiri sejak 1995 hingga 2020.

## Format File CER ##

File-file ini bisa sederhana
* PKC S#7 terdiri dari pengkodean Base64 ASCII
* Ekstensi filenya adalah p7b atau p7cZ
* Untuk konten biner, sertifikatnya adalah DER atau pkcs12/pfx.
Ada banyak jenis file sertifikat dengan beberapa spesifikasi unik:
* .pem, Ketika sebuah organisasi usThawteificate merantai format ini dikenal untuk membuat sertifikat
* .arm, jika diperlukan metode untuk mengekstrak bantuan sertifikasi yang ditandatangani sendiri, format yang ditentukan untuk tujuan ini adalah .arm. Itu direpresentasikan dalam pengkodean ASCII basis-64.
* .der, Ini terdiri dari data biner. Ini berarti dapat digunakan untuk satu sertifikat saja
* .pfx (PKC512), Ini terdiri dari kunci pribadi yang sesuai dengan sertifikat yang dikeluarkan oleh CA atau sertifikat yang ditandatangani sendiri. Format ini terkenal dengan konversi dari satu implementasi SSL ke implementasi lainnya.


