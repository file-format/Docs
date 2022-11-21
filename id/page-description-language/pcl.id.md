{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Pelajari tentang format file PCL dan API yang dapat membuat dan membuka file PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PCL? ##

PCL adalah singkatan dari Printer Command Language yang merupakan Bahasa Deskripsi Halaman yang diperkenalkan oleh Hewlett Packard (HP). HP menciptakan PCL untuk memberikan cara yang efisien dalam mengontrol fitur printer di banyak perangkat pencetakan yang berbeda. Format ini awalnya dikembangkan untuk printer dot matrix dan Inkjet HP, tetapi telah menjadi bagian dari berbagai printer termal, matriks, dan halaman seiring berjalannya waktu. Format mengalami beberapa revisi yang berbeda, sehingga menghasilkan versi yang berbeda di mana setiap versi ditingkatkan untuk memenuhi tuntutan waktu sehubungan dengan fitur kontrol printer. Saat ini, PCL adalah bahasa printer yang paling banyak tersebar di pasar printer terakhir.

## Versi PCL ##

Versi PCL berbeda dalam fungsi (mis. dukungan jenis font: font bitmap, font yang dapat diskalakan (font Intellifont, font TrueType), metode kompresi grafis raster, dukungan grafis HP-GL/2).

**PCL 1:** sekitar tahun 1980 - Fungsi Cetak dan Ruang adalah kumpulan fungsi dasar yang disediakan untuk keluaran stasiun kerja pengguna tunggal yang sederhana dan nyaman.

**PCL 2:** sekitar tahun 1980 - fungsi EDP (Electronic Data Processing)/Transaction adalah superset dari PCL 1. Fungsi ditambahkan untuk tujuan umum, pencetakan sistem multi-pengguna.

**PCL 3**: 1984 - Fungsi Pemrosesan Kata Office adalah superset dari PCL 2. Fungsi ditambahkan untuk produksi dokumen kantor berkualitas tinggi dan peningkatan dpi hingga 300 dpi. Itu memungkinkan untuk penggunaan font dan grafik bitmap dalam jumlah terbatas, dan mendukung HP-GL. PCL 3 banyak ditiru oleh produsen printer lain dan disebut oleh perusahaan ini sebagai "Emulasi LaserJet Plus".
(Printer: keluarga HP DeskJet, printer seri HP LaserJet, printer seri HP LaserJet Plus)

**PCL3+:** Digunakan oleh rangkaian printer DeskJet dan DesignJet.

**PCL3c:** Digunakan oleh rangkaian printer DeskJet dan DesignJet.

**PCL3e**: Digunakan oleh rangkaian printer DeskJet dan DesignJet. Sekarang juga digunakan di PhotoSmart.

**PCL3GUI**: Menggunakan RTL dan digunakan oleh rangkaian printer DeskJet dan DesignJet.

**PCLSLEEK**: Menggunakan RTL dan digunakan oleh rangkaian printer DeskJet dan DesignJet.

**PCL 4**: 1985 - Fungsi pemformatan halaman adalah superset dari PCL 3. Makro yang didukung, font dan grafis bitmap yang lebih besar. (Printer: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Fungsionalitas Office Publishing adalah superset dari PCL 4. Kemampuan penerbitan baru meliputi penskalaan font dan grafik HP-GL/2 (vektor). (Printer: HP LaserJet III)

**PCL 5e:** 1994 - Ini adalah revisi besar, yang menyertakan fitur baru seperti Sistem Kompresi Adaptif, pengkodean karakter 2byte, dukungan untuk font vektor, dan perintah konfigurasi dua arah. Termasuk Operasi Logis (sesuai dengan ROP GDI) untuk meningkatkan dukungan Windows sebelum memotong jalur. (Printer: HP LaserJet 4)

**PCL 5j:** Fitur baru seperti dukungan karakter 2 byte untuk font skalabel penduduk Jepang, tulisan vertikal, ukuran kertas Jepang, dan string jenis huruf. (Printer: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Dukungan warna dan Operasi Logis ditambahkan ke PCL5. PCL5c mendahului PCL5e. Beberapa model juga mendukung jalur kliping. (Printer: HP Color LaserJet, HP PaintJet 300 XL (printer pertama dengan PCL5c), HP DeskJet 1200C/1600C (nomor model ini telah digunakan kembali dan model yang lebih baru bukan PCL 5c)

**PCL 5ce:** Mendukung jenis huruf Agfa Microtype yang dapat diskalakan. (Printer: Printer HP 2500c Pro)

**PCL 6 / XL:** 1996 - PCL 6 atau PCL XL adalah format baru yang diperkenalkan pada tahun 1995, yang tidak kompatibel dengan versi PCL sebelumnya. (Printer: HP LaserJet 5, 5M dan 5N)

## Ikhtisar PCL 6 ##

HP memperkenalkan PCL 6 pada tahun 1996 yang merupakan evolusi berikutnya dari bahasa PCL dan teknologi terkait. Ini memiliki komponen berikut:

**PCL 6 Enhanced:** menyediakan versi yang dioptimalkan untuk mencetak dari antarmuka pengguna grafis (GUI) seperti MS Windows dan OS/2

**PCL 6 Standard:** memberikan kompatibilitas mundur lengkap dengan printer HP LaserJet sebelumnya

**Sintesis Font PCL:** menyediakan font yang dapat diskalakan, manajemen font, dan penyimpanan formulir dan font.

Versi diperpanjang PCL XL lebih dekat dengan GDI yang digunakan banyak aplikasi. Itu memastikan bahwa lebih sedikit terjemahan terjadi yang menghasilkan peningkatan kemampuan WYSIWYG dan kinerja yang lebih baik dengan aplikasi yang mendukung pelolosan yang diterapkan oleh driver yang Disempurnakan. Output dari driver Enhanced (PCL XL) mungkin tidak sama dengan output dari driver Standard. Jika output tidak seperti yang diharapkan, pilih driver Standard (PCL5e).

Perintah PCL 6 yang Disempurnakan dirancang agar sesuai secara optimal dengan persyaratan pencetakan grafis untuk aplikasi berbasis GUI. Dalam kebanyakan kasus, untuk setiap perintah pencetakan grafik yang ingin dilakukan oleh GUI, ada perintah PCL 6 Enhanced yang cocok. Ini mengurangi jumlah perintah yang diperlukan untuk mendeskripsikan halaman grafik. Setiap perintah di PCL 6 Enhanced dirancang untuk memerlukan transfer data minimal dari PC host ke printer. Hal ini mengurangi jumlah data yang diperlukan untuk mendeskripsikan halaman.

Sistem Pencetakan Windows untuk sebagian besar printer HP LaserJet menyediakan dua driver terpisah: Standard dan Enhanced. Driver Standard menyediakan kompatibilitas mundur dengan menggunakan perintah PCL 6 Standard (PCL5e) untuk mencetak teks sederhana atau teks campuran dan halaman grafis. Driver Enhanced menggunakan perintah PCL 6 Enhanced yang telah dioptimalkan untuk mencetak halaman grafis yang rumit.

## Revisi Kelas PCL 6 ##

#### Kelas 1.1 ####

**Alat gambar:** Mendukung garis gambar, busur/elips/akord, persegi panjang (bulat), poligon, jalur Bezier, jalur terpotong, gambar raster, garis pindai, operasi raster.
**Penanganan warna:** Mendukung palet 1/4/8-bit, ruang warna RGB/abu-abu. Mendukung pola halftone khusus (maks 256 pola).
**Kompresi:** Mendukung RLE.
**Satuan ukuran:** Inci, milimeter, sepersepuluh milimeter.
**Penanganan kertas:** Mendukung kumpulan jenis kertas khusus atau standar, termasuk Letter, Legal, A4, dll. Dapat memilih kertas dari pengumpanan manual, baki, kaset. Kertas dapat digandakan secara horizontal atau vertikal. Kertas dapat diorientasikan dalam potret, lanskap, atau rotasi 180 derajat dari dua yang sebelumnya.
**Font:** Mendukung font bitmap atau TrueType, poin kode 8 atau 16-bit. Pemilihan character set menggunakan kode set simbol yang berbeda dari PCL 5. Ketika font bitmap digunakan, banyak perintah scaling yang tidak tersedia. Ketika font TrueType digunakan, deskriptor panjang variabel, blok kelanjutan tidak didukung. Font kerangka dapat diputar, diskalakan, atau dicukur.

#### Kelas 2.0 ####

**Kompresi:** Menambahkan kompresi JPEG eksklusif yang disebut JetReady.
**Penanganan kertas:** Media dapat dialihkan ke nampan keluaran yang berbeda (hingga 256). Menambahkan ukuran media prasetel A6 dan B6 Jepang. Menambahkan preset kaset ketiga, 248 sumber media baki eksternal.
**Font:** Teks dapat ditulis secara vertikal.

#### Kelas 2.1 ####

**Penanganan warna:** Menambahkan fitur pencocokan Warna.
**Kompresi:** Menambahkan Baris Delta.
**Penanganan kertas:** Orientasi, ukuran media bersifat opsional saat mendeklarasikan halaman baru. Menambahkan jenis kertas B5, JIS 8K, JIS 16K, JIS Exec.

#### Kelas 3.0 ####

**Penanganan warna:** Memungkinkan penggunaan pengaturan halftone yang berbeda untuk grafik vektor atau raster, teks. Mendukung half-toning adaptif.
**Protokol:** Mendukung PCL passthrough, memungkinkan fitur PCL 5 digunakan oleh stream PCL 6. Namun, beberapa status PCL 6 tidak dipertahankan saat menggunakan fitur ini.
**Font:** Mendukung font PCL.
**Viewer/Converter:** PCLReader (freeware) dapat melihat, mengonversi, atau mencetak PCL 6 level apa pun (termasuk JetReady) ke printer apa pun.

## Referensi ##

* [PCL - Oleh Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

