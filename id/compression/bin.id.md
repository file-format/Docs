{
"tanggal":"20-07-2023",
   "keywords":[
"TEMPAT SAMPAH",
"Berkas BIN",
"mengajukan",
"ekstensi file BIN",
"perpanjangan",
"mengajukan"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draf":"false",
"toc":true,
"title":"Format File BIN - File Berkode MacBinary",
   "description":"Pelajari tentang format BIN dan API yang dapat membuat dan membuka file BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent" : "compression"
}
},
"mod terakhir":"20-07-2023"
}

## Apa itu file BIN?

File BIN, dalam konteks komputer Macintosh, dapat merujuk ke file yang disimpan dalam format MacBinary. MacBinary adalah format file yang dirancang khusus untuk mentransfer file Macintosh melalui internet, email, FTP, atau media portabel. Tujuan MacBinary adalah untuk mempertahankan struktur file lengkap dan atribut file Macintosh, termasuk data fork dan resource fork, dalam satu file.

Format MacBinary mencapai hal ini dengan merangkum garpu sumber daya dan garpu data Sistem File Hierarki Macintosh (HFS) ke dalam file terkompresi. Ini juga mencakup header pencari yang berisi metadata penting tentang file tersebut. Dengan menggabungkan semua komponen ini ke dalam satu file, MacBinary memastikan bahwa file tersebut mempertahankan integritasnya dan dapat dengan mudah ditransfer dan dibagikan ke berbagai platform.

Dengan kemajuan dalam sistem file Apple dan protokol transfer file, penggunaan file BIN dan format MacBinary menjadi semakin jarang. Pengenalan format file seperti ZIP dan transisi ke sistem file yang lebih modern, seperti HFS+ dan APFS, telah mengurangi kebutuhan akan file yang dikodekan MacBinary. Sistem file yang lebih baru ini menyediakan cara yang lebih efisien dalam menangani atribut file, percabangan sumber daya, dan percabangan data, menjadikan format MacBinary kurang diperlukan dalam lanskap komputasi saat ini.

## Format File BIN - Informasi Lebih Lanjut

Pada masa awal komputer Macintosh, file disimpan dalam dua "garpu" terpisah karena keterbatasan data. "Garpu sumber daya" berisi data terstruktur, sedangkan "garpu data" berisi data tidak terstruktur. Meskipun Mac OS Klasik memperlakukan fork ini sebagai satu file, mentransfer file ke sistem non-Mac mengakibatkan hilangnya data karena sistem tersebut tidak mengenali fork tersebut sebagai satu kesatuan. Untuk mengatasi hal ini, format MacBinary dibuat oleh individu seperti Dennis Brothers, Harry Chesley, dan Yves Lempereur. MacBinary mengompresi dan menggabungkan fork menjadi satu file, yang dikenal sebagai file BIN, untuk ditransfer ke sistem non-Mac. Setelah kembali ke Mac OS, percabangan akan dipisahkan lagi. Dengan peralihan dari HFS berbasis fork pada tahun 2000an, penggunaan format MacBinary menurun secara signifikan. Saat ini, jarang menemukan file BIN yang dikodekan MacBinary kecuali Anda menemukan file lama di sistem non-Mac atau mengunduhnya dari internet.

Format MacBinary telah melalui beberapa versi dari waktu ke waktu untuk mengakomodasi perubahan dalam sistem Macintosh dan penanganan file. Berikut adalah beberapa versi berbeda dari format MacBinary:

- **MacBinary I:** Versi awal MacBinary, diperkenalkan pada akhir tahun 1980an. Ini menggabungkan garpu sumber daya dan garpu data ke dalam satu file biner, memungkinkan transfer file Macintosh lintas platform.

- **MacBinary II:** Versi ini, dirilis pada awal tahun 1990-an, menyempurnakan format MacBinary asli dengan menambahkan informasi tambahan, seperti jenis file dan kode pembuat, ke header file biner. Kode-kode ini membantu menjaga integritas dan identifikasi file Macintosh selama transfer.

- **MacBinary III:** Format MacBinary III, yang diperkenalkan pada pertengahan tahun 1990-an, semakin menyempurnakan versi sebelumnya dengan menyertakan metadata tambahan, seperti nama file dan tanggal pembuatan serta modifikasi file, di header file biner. Hal ini memungkinkan pelestarian atribut file Macintosh yang lebih komprehensif selama transfer.

- **MacBinary IV:** MacBinary IV dikembangkan untuk mengatasi masalah kompatibilitas dengan sistem operasi Mac OS X yang sedang berkembang di awal tahun 2000-an. Ini memasukkan perubahan untuk beradaptasi dengan struktur dan atribut sistem file baru yang diperkenalkan di Mac OS X.

## Bagaimana cara membuka file BIN?

File BIN Berkode MacBinary dapat dibuka menggunakan berbagai utilitas kompresi. Untuk pengguna macOS, **Apple Archive Utility** adalah opsi yang cocok. Pengguna Windows dapat menggunakan perangkat lunak seperti **Smith Micro StuffIt Deluxe** untuk mengekstrak konten file BIN Berkode MacBinary. Opsi lain untuk pengguna macOS adalah **The Unarchiver**, yang merupakan alat serbaguna yang mampu menangani berbagai format file, termasuk MacBinary.

Penting untuk dicatat bahwa ekstensi file .bin digunakan oleh berbagai format file, bukan hanya MacBinary. Oleh karena itu, jika Anda menemukan file BIN yang tidak dapat dibuka dengan utilitas yang disebutkan di atas, file tersebut mungkin disimpan dalam format yang berbeda. Dalam kasus seperti itu, Anda mungkin perlu mengidentifikasi format file tertentu dan menggunakan perangkat lunak atau utilitas yang sesuai yang dirancang untuk format tersebut untuk mengakses konten file.

## File BIN lainnya

Berikut jenis file lain yang menggunakan ekstensi file **.bin**.

- [BIN - File Gambar Disk Biner](/id/disc-and-media/bin/)
- [BIN - File Unix yang Dapat Dieksekusi](/id/executable/bin/)
- [BIN - File Kebijakan TI BlackBerry](/id/settings/bin/)
- [BIN - ROM Game Sega Genesis](/id/game/bin/)
- [BIN - Gambar BIOS PlayStation PSX](/id/game/bin-pcsx/)

## Referensi

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

