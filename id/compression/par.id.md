{
"tanggal":"18-07-2023",
   "keywords":[
"PAR",
"Berkas PAR",
"cara membuka file par",
"mengajukan",
"ekstensi file PAR",
"perpanjangan",
"mengajukan"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draf":"false",
"toc": true,
"title":"Format File PAR - File Indeks Parchive",
   "description":"Pelajari tentang format PAR dan API yang dapat membuat dan membuka file PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent":"kompresi"
}
},
"mod terakhir":"18-07-2023"
}

## Apa itu file PAR?

Dalam arsip Parchive (PAR), file .par mengacu pada file indeks yang berisi sekelompok volume paritas atau blok paritas. File indeks ini digunakan untuk tujuan deteksi kesalahan dan pemulihan ketika satu atau lebih file dalam arsip hilang atau rusak.

Arsip Parchive biasanya terdiri dari file data asli dan volume paritas yang sesuai. Volume paritas dibuat menggunakan algoritma koreksi kesalahan Reed-Solomon. Volume paritas ini berisi informasi berlebihan yang dapat digunakan untuk memulihkan file data asli.

File .par, juga dikenal sebagai kumpulan volume paritas, berisi informasi tentang struktur dan lokasi volume paritas dalam arsip. Ini berfungsi sebagai indeks atau peta untuk proses pemulihan. Dengan menggunakan file .par, perangkat lunak PAR khusus dapat menentukan volume paritas mana yang diperlukan dan bagaimana volume tersebut harus digunakan untuk merekonstruksi file yang hilang atau rusak.

Ketika satu atau lebih file dalam arsip Parchive tidak dapat diakses atau rusak, file .par dapat digunakan bersama dengan volume paritas yang tersedia untuk memulihkan data yang hilang. Perangkat lunak PAR membaca file .par, mengidentifikasi file yang hilang atau rusak, dan menggunakan volume paritas untuk merekonstruksinya.

## Bagaimana cara membuka file PAR?

Untuk membuka dan menggunakan file .par, Anda memerlukan perangkat lunak PAR khusus. Berikut adalah beberapa opsi perangkat lunak populer yang dapat menangani file .par:

- **QuickPar:** QuickPar adalah perangkat lunak PAR yang banyak digunakan untuk Windows. Ini memungkinkan Anda membuat, memverifikasi, dan memperbaiki file PAR. Anda dapat membuka file .par di QuickPar untuk memverifikasi integritasnya atau menggunakannya untuk memperbaiki file yang rusak atau hilang dalam arsip Parchive.

- **MultiPar:** MultiPar adalah perangkat lunak PAR populer lainnya yang tersedia untuk Windows. Ini mendukung format file PAR dan PAR2 dan menyediakan fitur-fitur canggih untuk membuat, memverifikasi, dan memperbaiki arsip. MultiPar dapat membuka file .par dan melakukan operasi deteksi kesalahan dan pemulihan berdasarkan volume paritas yang disediakan.

- **MacPAR deLuxe:** MacPAR deLuxe adalah perangkat lunak PAR yang dirancang khusus untuk macOS. Ini mendukung format file PAR dan PAR2 dan menyediakan fungsionalitas serupa seperti QuickPar dan MultiPar. MacPAR deLuxe dapat membuka file .par dan membantu memverifikasi arsip dan memulihkan file yang rusak atau hilang.

## Format File PAR - Informasi Lebih Lanjut

Format file PAR, biasa disebut Parchive, adalah format file khusus yang digunakan untuk membuat data paritas dan melakukan deteksi kesalahan serta pemulihan dalam arsip file. Format file PAR biasanya terdiri dari tiga jenis: PAR, PAR2, dan PAR3.

- **PAR:** Format file PAR asli, juga dikenal sebagai PAR1, dikembangkan oleh proyek Parchive. Ini mencakup data paritas yang dihasilkan dari file data asli. File PAR menyediakan deteksi dan pemulihan kesalahan tingkat dasar tetapi memiliki keterbatasan dalam hal kemampuan koreksi kesalahan.

- **PAR2:** PAR2 adalah versi format file PAR yang ditingkatkan. Ia menawarkan kemampuan koreksi kesalahan yang lebih canggih dan fitur pemulihan yang ditingkatkan. File PAR2 biasanya digunakan untuk membuat data paritas yang dapat memulihkan file yang hilang atau rusak dalam arsip. File PAR2 memberikan perlindungan yang lebih baik terhadap kerusakan data dan banyak digunakan untuk tujuan pengarsipan file.

- **PAR3:** PAR3 adalah versi terbaru dari format file PAR dan memberikan peningkatan lebih lanjut dalam koreksi dan pemulihan kesalahan. Ia menawarkan tingkat redundansi dan kemampuan koreksi kesalahan yang lebih tinggi dibandingkan dengan PAR2. File PAR3 dirancang untuk memberikan opsi perlindungan dan pemulihan yang lebih kuat untuk data yang disimpan dalam arsip.

Format file PAR2 dan PAR3 didukung secara luas oleh perangkat lunak PAR dan menawarkan kemampuan untuk memverifikasi integritas file dalam arsip dan memulihkan data yang hilang atau rusak. File PAR dan PAR2 masih umum digunakan, sementara file PAR3 secara bertahap mulai diadopsi karena kemampuan koreksi kesalahannya yang ditingkatkan.

## Referensi
* [Parsip](https://en.wikipedia.org/wiki/Parchive)

