{
  "date" : "2021-06-29",
  "keywords" :[ "file com", "apa itu file com", "file", "contoh com", "ekstensi file com", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file COM dan API yang dapat membuat dan membuka file COM.",
  "title" :"COM - Format File Perintah DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu file COM?
File COM hanya digunakan untuk menjalankan serangkaian perintah atau instruksi. File COM terdiri dari program yang dapat dieksekusi yang dapat dijalankan dari Windows atau MS-DOS. Demikian juga file EXE, file COM juga disimpan dalam format biner tetapi berbeda dengan file EXE karena tidak memiliki header atau metadata dan juga memiliki ukuran maksimum sekitar 64KB. Ketika file COM berjalan pertama kali pada sistem 32-bit, ia meminta untuk menginstal komponen NT Virtual DOS Machine (NTVDM). File COM dapat dijalankan pada Microsoft Windows versi 64-bit dengan mesin virtual yang mendukung lingkungan MS-DOS.

## format file.COM
Format file COM adalah format yang dapat dieksekusi biner yang digunakan di Microsoft Windows atau MS-DOS. Strukturnya hanya terdiri dari sekumpulan instruksi; tidak memiliki tajuk dan tidak berisi metadata standar. Ini menyimpan semua data dan kodenya dalam satu segmen saja dan binernya memiliki ukuran maksimum 64KB. Format file ini tidak berpindah sendiri saat mencoba menjalankan ulang. Jadi sistem operasi memuatnya di alamat yang telah ditentukan sebelumnya. Selain itu, dimungkinkan untuk membuat file COM untuk dijalankan di kedua sistem operasi dalam bentuk **fat binary**. Tidak ada kompatibilitas aktual di tingkat instruksi. Instruksi pada titik masuk dipilih untuk memiliki fungsionalitas yang sama tetapi berbeda di kedua sistem operasi, dan membuat program berjalan, lompat ke bagian sistem operasi yang digunakan. Ini pada dasarnya adalah dua program berbeda dengan prosedur yang sama dalam satu file, didahului dengan pemilihan kode yang akan digunakan.
### Contoh file COM
Saat mengeksekusi file COM, instruksi dibaca dari byte pertama dan diikuti secara berurutan hingga instruksi terakhir ditemukan. Berikut adalah contoh kode ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Referensi

* [COM file - oleh Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

