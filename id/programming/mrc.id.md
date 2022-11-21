{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "file", "ekstensi", "format file", "implementasi mrc", "Panduan Pemrograman", "contoh mrc", "mIRC", "bahasa skrip mIRC", "file INI", " mSL scripting language", "mIRC language", "mIRC scripts", "scripting language" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - File Bahasa Skrip mIRC",
  "description":"Pelajari tentang format file MRC dan API yang dapat membuat dan membuka file MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Apa itu file MRC?

mIRC adalah bahasa scripting yang disematkan sebagai klien IRC (Internet Relay Chat) di sistem operasi Windows. Ini memberikan fasilitas perlindungan dari spamming untuk penggunaan pribadi dan saluran. Untuk memberikan pengalaman kompatibilitas pengguna yang lebih baik, bahasa skrip mIRC ini memungkinkan pembuatan jendela dialog. Berkas yang berisi skrip, sebagian besar dalam format teks biasa disimpan dengan ekstensi MRC atau sebagai berkas [INI](/id/system/ini/). Fungsi bahasa ini dikenal sebagai perintah dan pengidentifikasi (ketika mereka mengembalikan nilai).

bahasa mIRC menyediakan pemuatan beberapa file skrip sekaligus. Di sisi lain, satu file dapat menyebabkan file lainnya tidak lagi digunakan saat dimuat secara bersamaan. Perintah disimpan dan dapat ada di IRC secara otomatis. Perintah dan alias yang digunakan dalam bahasa ini tidak terdiri dari karakter yang didahulukan.

mIRC digunakan secara luas untuk membuat bot mengelola saluran secara otomatis tetapi juga dapat dimodifikasi dengan bahasa skrip mSL. Itu dapat memperkenalkan banyak fitur baru seperti makro, kemampuan memutar musik, makro dan fungsi kecil, permainan dasar, atau mengoperasikan aplikasi kecil.


## Sejarah Singkat ##

Bahasa skrip ini pertama kali dikembangkan pada tahun 1995 oleh Khaled Adam Bey. Desain bahasa scripting juga dibuat oleh Khalid. Target bahasa ini adalah pemrograman berbasis peristiwa. Awalnya ekstensi file yang digunakan untuk file bahasa pemrograman ini adalah .mrc dan .ini. Selain itu, dikembangkan di bawah lisensi perangkat lunak berpemilik.

## Spesifikasi Teknis ##

Beberapa fungsi dibuat skrip khusus melalui bahasa mIRC ini dan dikenal sebagai alias. Ketika alias ini mengembalikan nilai, mereka dikenal sebagai pengidentifikasi khusus. Semua variabel yang terdapat dalam bahasa mIRC ini diketik secara dinamis. Sigil digunakan oleh skrip mIRC. Fitur lain dari bahasa scripting ini adalah pop-up. Pengguna dapat memanggil pop-up hanya dengan memilihnya. Remote ditentukan untuk acara tertentu. Remote dipanggil ketika peristiwa relatif terjadi.

Token yang dibatasi ruang digunakan untuk memecah setiap baris kode bahasa ini. Ada beberapa ekstensi populer lainnya yang digunakan untuk file mIRC seperti MDX (mIRC Dialog Extension) dan DCX (Dialog Control Extension). Keduanya adalah ekstensi dialog dan relatif lebih populer. Konstruksi bahasa dirujuk oleh nomenklatur bahasa scripting ini. Bahasa mIRC melibatkan berbagai aspek bahasa skrip seperti variabel lokal dan global, variabel biner, tabel hash, dan penanganan file.


## Contoh Format File MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/id/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Referensi ##

* [MIRC - oleh Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



