{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File AWK - File Skrip AWK",
  "description":"Pelajari tentang format file AWK dan API yang dapat membuat dan membuka file AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Apa itu file AWK?

File AWK adalah file skrip yang dibuat untuk aplikasi pemrosesan teks **AWK** yang dibundel dengan sistem operasi Unix dan Linux. Ini berisi instruksi logis untuk melakukan tindakan pada teks atau konten file seperti mencocokkan, mengganti, dan mencetak teks. Ini membantu menghasilkan laporan dan teks yang diformat dari file input. Utilitas awk biasanya terletak di /usr/bin/awk pada sebagian besar distribusi linux/unix.

## Bagaimana Cara Membuat Skrip AWK?

File AWK dapat dibuat atau dibuka di editor teks apa pun di Linux/Unix OS. File skrip AWK baru dapat dibuat sebagai berikut.

```
$ vi script.awk
```

Ini akan membuka file AWK di editor teks. Masukkan beberapa pernyataan di editor teks sebagai berikut.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Baris pertama isi teks ini dijelaskan sebagai berikut.

* \#! – disebut sebagai `Shebang`, yang menentukan juru bahasa untuk instruksi dalam skrip
* /usr/bin/awk – adalah penerjemah
* -f – opsi juru bahasa, digunakan untuk membaca file program

## Bagaimana Cara Menjalankan Skrip AWK?

Simpan file dan buat skrip dapat dieksekusi dengan mengeluarkan perintah di bawah ini:
```
$ chmod +x script.awk
```

Script kemudian dapat dijalankan sebagai berikut.

```
$ ./script.awk
```

yang menghasilkan output berikut.

```
Writing my first Awk executable script!
```

## Referensi ##

* [Menulis Skrip Menggunakan Bahasa Pemrograman Awk](https://www.tecmint.com/write-Shell-scripts-in-awk-programming/)

