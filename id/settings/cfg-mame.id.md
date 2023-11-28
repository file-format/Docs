{
"tanggal": "27-09-2023",
  "keywords": [
"cfg",
"file cfg",
"file konfigurasi cfg mame",
"apa itu file cfg",
"cara membuka file cfg",
"mengajukan",
"ekstensi file cfg",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File CFG - File Konfigurasi MAME",
  "description":"Pelajari tentang format File Konfigurasi MAME CFG dan API yang dapat membuat dan membuka file CFG.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"parent": "pengaturan"
}
},
"mod terakhir": "27-09-2023"
}

## Apa itu file CFG?

File CFG adalah file konfigurasi keyboard XML yang digunakan oleh emulator video game arcade MAME. Ini adalah komponen penting untuk menyesuaikan kontrol keyboard dan hotkey agar sesuai dengan preferensi pemain. File-file ini menyimpan pemetaan dan pengaturan yang menentukan bagaimana keyboard berinteraksi dengan emulator saat bermain game. Dengan mengedit file ini, pengguna dapat menyesuaikan pengalaman bermain game mereka dengan menetapkan tombol keyboard tertentu untuk tindakan dalam game, seperti memasukkan koin, memulai, memindahkan, dan berbagai fungsi lainnya.

## File Konfigurasi MAME

MAME, yang merupakan singkatan dari **Multiple Arcade Machine Emulator**, adalah aplikasi perangkat lunak yang memungkinkan Anda meniru dan memainkan game arcade di komputer Anda. MAME menggunakan file konfigurasi untuk menyesuaikan perilaku dan pengaturannya. File konfigurasi ini biasanya terletak di folder `cfg` dalam direktori MAME Anda.

Berikut adalah file konfigurasi utama yang mungkin Anda temui saat menyiapkan dan mengonfigurasi MAME:

1. **mame.ini:** Ini adalah file konfigurasi utama untuk MAME. Ini berisi pengaturan global yang berlaku untuk semua game. Anda dapat menemukan file ini di direktori root instalasi MAME Anda.

1. **default.cfg:** File ini menyimpan pengaturan default untuk semua game yang tidak memiliki file konfigurasinya sendiri. Ini digunakan sebagai cadangan untuk pengaturan khusus game.

1. **game-special.cfg:** File ini digunakan untuk menyimpan pengaturan untuk masing-masing game. Mereka biasanya diberi nama berdasarkan file ROM untuk game yang terkait dengannya. Misalnya jika Anda memiliki game bernama "pacman.zip", file konfigurasinya adalah "pacman.cfg."

Berikut adalah beberapa pengaturan umum yang mungkin Anda temukan di file konfigurasi MAME.

1. **rompath:** Menentukan direktori tempat ROM game arcade Anda berada.

1. **cfg_directory:** Menentukan direktori tempat file konfigurasi khusus game disimpan.

1. **nvram_directory:** Menentukan direktori tempat file RAM non-volatile (NVRAM) disimpan. NVRAM menyimpan skor tinggi dan data khusus game lainnya.

1. **artwork_directory:** Menentukan direktori tempat file karya seni (seperti bezel, marquees, dan flyer) disimpan.

1. **samplepath:** Menentukan direktori tempat file suara sampel berada.

1. **cheatpath:** Menentukan direktori tempat file cheat berada.

Anda juga dapat mengonfigurasi berbagai pengaturan lain seperti opsi video dan audio, kontrol, dan perangkat input. Untuk mengubah pengaturan ini, Anda dapat membuka file konfigurasi di editor teks dan membuat perubahan yang diperlukan.

## MAME

MAME, yang merupakan singkatan dari **"Multiple Arcade Machine Emulator,"** adalah aplikasi perangkat lunak yang dirancang untuk meniru dan mereplikasi perangkat keras mesin arcade kuno dan konsol game arcade. Hal ini memungkinkan pengguna untuk memainkan perpustakaan besar permainan arcade klasik di komputer modern dan perangkat lain yang kompatibel. MAME adalah proyek sumber terbuka dan telah menjadi emulator pilihan untuk melestarikan dan menikmati kekayaan sejarah game arcade.

1. **Emulasi:** Tujuan utama MAME adalah meniru perangkat keras mesin arcade secara akurat, termasuk unit pemrosesan pusat (CPU), chip suara, chip grafis, dan perangkat input. Tingkat akurasi ini memastikan bahwa game berperilaku sedekat mungkin dengan pengalaman arcade aslinya.

1. **Kompatibilitas:** MAME mendukung berbagai ROM game arcade, menjadikannya salah satu emulator arcade terlengkap yang tersedia. Itu dapat menjalankan game dari berbagai platform arcade termasuk game klasik dari tahun 70an, 80an, 90an, dan bahkan beberapa judul arcade yang lebih baru.

1. **Pelestarian:** Salah satu misi utama MAME adalah melestarikan sejarah game arcade. Dengan meniru perangkat keras arcade secara akurat, MAME membantu mencegah hilangnya game klasik dan memastikan bahwa generasi mendatang dapat memainkannya sesuai tujuan awalnya.

1. **Front-End:** Banyak pengguna menggunakan aplikasi front-end yang menyediakan antarmuka grafis untuk mengelola dan meluncurkan game melalui MAME. Front-end ini memudahkan navigasi perpustakaan permainan MAME yang luas.

## Bagaimana cara membuka file CFG?

Program yang membuka atau mereferensikan file CFG

- MAME (Gratis) (Windows)
- EkstraMAME (Uji Coba)
- MacMAME (MAC)

## File CFG lainnya

Berikut jenis file lain yang menggunakan ekstensi file **.cfg**.

**Pengaturan**
- [CFG - File Konfigurasi Celestia](/id/settings/cfg-celestia/)
- [CFG - File Koneksi Server Citrix](/id/settings/cfg-citrix/)
- [CFG - File Konfigurasi MAME](/id/settings/cfg-mame/)
- [CFG - File Konfigurasi LightWave](/id/settings/cfg-lightwave/)

**Permainan**
- [CFG - File Bahasa Markup Wesnoth](/id/game/cfg-wesnoth/)
- [CFG - File Konfigurasi MUGEN](/id/game/cfg-mugen/)
- [CFG - File Konfigurasi Mesin Sumber](/id/game/cfg-sourceengine/)

**Sistem & Lainnya**
- [CFG - Berkas CFG](/id/system/cfg/)
- [CFG - File Konfigurasi Model Cal3D](/id/misc/cfg-cal3d/)

## Referensi
* [MAME](https://en.wikipedia.org/wiki/MAME)

