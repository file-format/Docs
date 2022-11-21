{
  "date" : "2021-08-11",
  "keywords" :[ "file vdi", "format file vdi", "apa itu file vdi", "file", "contoh vdi", "ekstensi file vdi", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file VDI dan API yang dapat membuat dan membuka file VDI.",
  "title" :"VDI - File Gambar Disk VirtualBox Virtual",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Apa itu file VDI?
File dengan ekstensi .vdi adalah image disk virtual; khusus untuk program virtualisasi desktop open source Oracle yang disebut VirtualBox. File VDI digunakan untuk memulai mesin virtual VirtualBox. VM memungkinkan pengguna untuk menjalankan sistem operasi atau program tambahan di satu komputer. Oleh karena itu, keuntungan dari file VDI adalah pengguna dapat menyimpan file gambar disk ini di hard disk mereka dan dapat menjalankannya menggunakan emulator kapan pun mereka membutuhkannya.

## format file VDI
Virtual Disk Image (VDI) adalah format file disk utama untuk Oracle VM sumber terbuka yang dikembangkan secara aktif yang dikenal sebagai VirtualBox, yang merupakan produk virtualisasi kelas perusahaan. Format file VDI dirancang untuk membuat image disk portabel yang dapat dijalankan dengan mudah menggunakan program virtualisasi lainnya. Ini mendukung penyimpanan yang dialokasikan secara dinamis dan berukuran tetap. Ini memungkinkan Anda untuk memperluas file gambar setelah dibuat, meskipun sudah berisi data.

### Virtualisasi disk
Sistem mengemulasi hard disk dalam format citra disk VDI. VM VirtualBox dapat menggunakan disk sebelumnya yang dibuat di Microsoft Virtual PC atau VMware, serta format aslinya sendiri. VirtualBox juga mampu terhubung ke target iSCSI dan mempartisi mentah di host, baik menggunakan hard disk virtual. VirtualBox mengemulasi IDE (pengontrol PIIX4 dan ICH6), SATA (pengontrol ICH8M), pengontrol SAS tempat hard drive dapat dipasang dan SCSI.

Dukungan tersedia untuk Open Virtualization Format (OVF) sejak versi 2.2.0 dari VirtualBox. Baik perangkat fisik yang terhubung ke host dan image ISO dapat dipasang sebagai drive CD atau DVD.
Secara default, VirtualBox mendukung grafik melalui kartu grafis virtual khusus yang kompatibel dengan VESA.

### Dukungan virtualisasi untuk Ethernet
VirtualBox memvirtualisasikan Kartu Antarmuka Jaringan berikut untuk adaptor jaringan Ethernet:
-AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Desktop Intel Pro/1000 MT (82540EM)
-Server Intel Pro/1000 MT (82545EM)
-Server Intel Pro/1000T (82543GC)
- Adaptor jaringan paravirtualisasi (virtio-net)

Kartu jaringan yang ditiru memungkinkan OS tamu untuk berjalan tanpa perlu mencari dan menginstal driver untuk perangkat keras jaringan karena tersedia sebagai bagian dari OS tamu. Adaptor jaringan paravirtual khusus meningkatkan kinerja jaringan dengan mengurangi kebutuhan untuk mencocokkan antarmuka perangkat keras tertentu. Oleh karena itu, diperlukan dukungan pengemudi khusus di tamu.


## Referensi

* [VirtualBox - oleh Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


