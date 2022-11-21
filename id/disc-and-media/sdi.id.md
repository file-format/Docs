{
  "date" : "2021-08-13",
  "keywords" :[ "file sdi", "format file sdi", "apa itu file sdi", "file", "contoh sdi", "ekstensi file sdi", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file SDI dan API yang dapat membuat dan membuka file SDI.",
  "title" :"SDI - File Gambar Penerapan Sistem Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Apa itu file SDI?
File dengan ekstensi .sdi berisi load blob, boot blob, dan part blob; biasanya digunakan oleh Windows Embedded Studio untuk membuat disk RAM atau boot disk untuk memuat dan menginstal Windows. SDI disingkat untuk System Deployment Image. Windows Embedded Studio adalah program yang digunakan untuk membuat gambar disk untuk Windows. Sebenarnya program ini berisi program SDI File Manager dan alat baris perintah yang disebut **sdigr.exe**, keduanya dapat digunakan untuk menyebarkan, membuat, dan mengedit gambar SDI.

## format file SDI
Format file SDI banyak digunakan untuk mengaktifkan penggunaan disk virtual untuk mem-boot sistem. Beberapa versi Microsoft Windows mengaktifkan **RAM booting**, yang penting untuk memuat file SDI ke dalam memori dan kemudian melakukan booting dari situ. Format file SDI juga mengaktifkan dirinya sendiri untuk booting jaringan dengan menggunakan PXE (Preboot Execution Environment). Itu juga digunakan untuk pencitraan hard disk.
### bagian file SDI
File SDI itu sendiri dapat dibagi menjadi beberapa bagian berikut:
- **Boot BLOB**: Ini berisi program boot sebenarnya, STARTROM.COM. Ini analog dengan sektor boot hard disk.
- **Load BLOB**: Ini biasanya berisi NTLDR dan diluncurkan oleh boot BLOB.
- **Part BLOB**: Ini berisi runtime boot aktual; juga menyertakan file boot.ini dan ntdetect.com yang harus ditempatkan di dalam direktori root runtime.
- **Disk BLOB**: Ini adalah image HDD datar yang dimulai dengan MBR. Ini digunakan untuk pencitraan hard drive alih-alih booting. Juga hanya Disk BLOB yang dapat dipasang dengan utilitas Microsoft.


## Referensi

* [Gambar Penerapan Sistem - oleh Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


