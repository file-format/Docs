{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File ZIM - File Arsip OpenZIM",
  "description":"Pelajari tentang format file ZIM dan API yang dapat membuat dan membuka file ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Apa itu file ZIM? ##

File dengan ekstensi .zim adalah arsip yang dibuat untuk menyimpan konten Wiki secara offline. Ini dianggap sebagai format file terbuka yang paling cocok untuk menyimpan Wikipedia di USB. Ini menyimpan konten situs dalam format yang ringkas. Namanya berasal dari "Zeno IMproved" yang merupakan format file Zeno sebelumnya. ZIM dikelola oleh proyek [openZIM ](https://openzim.org/) yang disponsori oleh Wikimedia CH, dan didukung oleh Wikimedia Foundation. File ZIM dapat dibuka dengan aplikasi seperti Kiwix dan ZIMReader. Proyek OpenZIM telah menyelenggarakan implementasi format file ZIM di [Github](https://github.com/openzim) atas kontribusi dari komunitas OpenSource.

## Spesifikasi Format File ZIM

Format file ZIM dikembangkan di atas [format file Zeno](https://openzim.org/wiki/Zeno_file_format) dan tidak kompatibel dengan versi sebelumnya. Spesifikasi format format file ZIM [tersedia online](https://openzim.org/wiki/ZIM_file_format) oleh openZIM untuk referensi pengembang. OpenZIM telah menyediakan implementasi sumber terbuka C++, [LibZim](https://openzim.org/wiki/Zimlib), untuk membaca dan menulis file ZIM.

Format file ZIM menggunakan kompresi LZMA2 untuk membuat konten menjadi ringkas.

{{< figure src="../ZIM_File_Format.jpeg" alt="Format File ZIM" >}}


### Tajuk ZIM

File ZIM dimulai dengan header yang diimbangi 0. Semua konstituen didasarkan pada little-endian dan semua bilangan bulat adalah bilangan bulat yang tidak ditandatangani yaitu uint_16, uint_32, uint_64.

|Nama Bidang |Jenis| mengimbangi| Panjang| Deskripsi|
---|---|---|---|---|
|angkaajaib| bilangan bulat| 0| 4| Angka ajaib untuk mengenali format file, harus 72173914 (0x44D495A)|
|majorVersion| bilangan bulat| 4| 2| Versi utama dari format file ZIM (5 atau 6)|
|minorVersion| bilangan bulat| 6| 2| Versi minor dari format file ZIM|
|uuid| bilangan bulat| 8| 16| id unik dari file zim ini|
|artikel Hitung| bilangan bulat| 24| 4| jumlah artikel|
|clusterCount| bilangan bulat| 28| 4| jumlah total cluster|
|urlPtrPos| bilangan bulat| 32| 8| posisi daftar penunjuk direktori yang diurutkan berdasarkan URL|
|titlePtrPos| bilangan bulat| 40| 8| posisi daftar penunjuk direktori yang diurutkan berdasarkan Judul|
|clusterPtrPos| bilangan bulat| 48| 8| posisi daftar pointer cluster|
|mimeListPos| bilangan bulat| 56| 8| posisi daftar tipe MIME (juga ukuran tajuk)|
|halaman utama| bilangan bulat| 64| 4| halaman utama atau 0xffffffff jika tidak ada halaman utama|
|layoutPage| bilangan bulat| 68| 4| halaman tata letak atau 0xffffffffff jika tidak ada halaman tata letak|
|checksumPos| bilangan bulat| 72| 8| arahkan ke md5checksum dari file ini tanpa checksum itu sendiri. Poin ini selalu 16 byte sebelum akhir file.|

## Referensi ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

