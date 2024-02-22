{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File WAKTU - Apa itu file .time? Waktu ketika File dibuat di Linux",
  "description" : "Pelajari tentang file TIME dan cari tahu Waktu pembuatan file di Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-id",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Apa itu file WAKTU?

Format file TIME digunakan oleh sistem web bernama LIGHT, yang membantu pengguna merekam, mengatur, dan berbagi kehidupan mereka. Pada dasarnya, ini menyimpan kumpulan postingan dan mewakili folder di halaman kehidupan pengguna di dalam sistem.

## Cara Mengetahui Kapan File Dibuat di Linux

Di Linux, Anda dapat menggunakan perintah `stat` untuk mengetahui kapan suatu file dibuat. Inilah cara Anda melakukannya:

Buka terminal dan ketik perintah berikut:

```
stat <file_path>
```

Ganti `<file_path> ` dengan jalur ke file yang Anda minati. Misalnya:

```
stat /path/to/your/file.txt
```

Perintah ini akan menampilkan berbagai informasi tentang file tersebut, termasuk waktu pembuatannya. Cari baris yang dimulai dengan Birth atau File:. Waktu Kelahiran menunjukkan kapan file dibuat di sistem file.

Berikut adalah contoh tampilan keluarannya:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Dalam contoh ini, waktu Kelahiran menunjukkan kapan file tersebut dibuat.

