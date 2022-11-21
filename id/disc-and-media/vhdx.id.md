{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file VHDX dan API yang dapat membuat dan membuka file VHDX.",
  "title" :"Format File VHDX - Apa itu file VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Apa itu file VHDX?

File VHDX adalah file image disk dalam format file Virtual Hard Disk v2. Ini berisi seluruh sistem operasi yang dapat dimuat dan digunakan sebagai mesin normal apa pun untuk menguji perangkat lunak atau menjalankan perangkat lunak yang memerlukan sistem operasi tertentu. VHDX, meskipun merupakan image disk penuh, disimpan dalam satu file. Perangkat lunak mesin virtual seperti Parallels Desktop, Windows Virtual Machine, dan Virtual Box dapat memuat dan membuka image disk.

File VHDX dapat dikonversi ke [VHD](/id/disc-and-media/vhd/) dengan Hyper-V Manager, atau ke [VDI](/id/disc-and-media/vdi/) dengan VirtualBox.

## Format File VHDX - Informasi Lebih Lanjut

Detail format file VHDX sepenuhnya didokumentasikan dan tersedia online sebagai [Spesifikasi Format File VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) pada Dokumentasi Microsoft. Ini adalah ekstensi ke format VHD dan menyertakan kemampuan yang ditingkatkan. Format file VHDX menyediakan fitur tambahan yang tersedia pada hard disk virtual dan lapisan file hard disk virtual. Ini lebih dioptimalkan dan memberikan hasil yang lebih baik untuk konfigurasi dan kemampuan perangkat keras penyimpanan. File VHDX dapat dibuka

### Dukungan untuk Hard Disk Virtual di VHDX

Ini mendukung tiga jenis hard disk virtual.

1. **Hard Disk Virtual Tetap** - Hard disk virtual dengan alokasi ukuran data tetap. Ukuran hard disk virtual tidak berubah dengan penambahan atau penghapusan data.

1. **Hard Disk Virtual Dinamis** - Hard disk virtual dengan ukuran disk dinamis. Ukurannya kapan saja sebesar data aktual yang ditulis padanya dan metadata. Ukuran filenya meningkat secara dinamis saat data ditambahkan atau dihapus darinya.

1. **Membedakan Hard Disk Virtual** - Mewakili arus hard disk virtual sebagai sekumpulan blok yang dimodifikasi dibandingkan dengan file hard disk virtual induk.

## Referensi

* [Spesifikasi Format File VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - oleh Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

