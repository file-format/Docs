{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - File Skrip Bash Shell",
  "description":"Pelajari tentang format file SH dan API yang dapat membuat dan membuka file SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Apa itu file SH?

File dengan ekstensi .sh adalah file perintah bahasa scripting yang berisi program komputer yang akan dijalankan oleh shell Unix. Itu dapat berisi serangkaian perintah yang dijalankan secara berurutan untuk melakukan operasi seperti pemrosesan file, eksekusi program, dan tugas serupa lainnya. Ini dijalankan dari antarmuka baris perintah oleh pengguna atau dalam batch untuk melakukan banyak operasi pada saat yang bersamaan. File skrip dapat dibuka di editor teks seperti Notepad, Notepad ++, Vim, Apple Terminal dan aplikasi serupa lainnya di OS Windows, MacOS dan Linux.

## Format File SH

File SH ditulis dalam teks biasa mengikuti sintaks yang ditentukan. File skrip ini mendukung:

* `Komentar` - Komentar dimulai dengan # dan diabaikan oleh shell.
* `Shortcuts` - Ini dapat digunakan untuk mengganti nama perintah untuk eksekusi singkat dan mudah.
* `Batch Jobs` - Beberapa perintah dapat dijalankan secara otomatis yang jika tidak perlu dimasukkan secara manual. Ini menghilangkan kebutuhan untuk menunggu pengguna memicu setiap tahap urutan.
* `Generalisasi` - Menggunakan loop sederhana, lebih banyak generalisasi dicapai untuk operasi seperti konversi gambar dari satu format ke format lainnya.

## Contoh file SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Bagaimana cara menjalankan file SH?
File SH biasanya dijalankan di Linux, bahkan di Windows Anda perlu terhubung dengan terminal Linux menggunakan perangkat lunak seperti Putty untuk menjalankan file sh. Berikut adalah langkah-langkah untuk menjalankan file SH di terminal Linux.

1. Buka terminal Linux dan buka direktori tempat file SH berada.
2. Dengan menggunakan perintah `chmod`, setel izin eksekusi pada skrip Anda (jika belum disetel).
3. Jalankan skrip menggunakan salah satu dari berikut ini
1. `./namaberkas.sh`
2. `sh namafile.sh`
3. `nama-skrip-bash-di sini.sh`

## Referensi

* [Bashscripting untuk Pemula](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

