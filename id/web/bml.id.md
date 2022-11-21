{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File BML - File Bahasa Markup Bean",
  "description":"Pelajari tentang format file BML dan API yang dapat membuat dan membuka file BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Apa itu file BML?

File dengan ekstensi .bml adalah file Bean Markup Language yang menyimpan kelas Java untuk mendukung aplikasi Java. Ini memungkinkan akses ke objek dan metode Java, dan tidak perlu membuat fungsionalitas baru menggunakan kelas Java. Ini menentukan bagaimana komponen terhubung satu sama lain untuk melakukan tugas yang bermanfaat. BML dikembangkan oleh IBM alphaWorks untuk menggambarkan hubungan struktur dan komponen. File BML dapat dibuka dan dilihat menggunakan editor teks apa pun seperti Browser Web, Microsoft Notepad, dan Notepad ++.

## Format File BML

Situs web IBM alphaworks telah menyediakan dua implementasi BML. Implementasi Pertama adalah juru bahasa yang 'memainkan' skrip BML untuk menghasilkan hierarki kacang yang diinginkan. Implementasi kedua adalah kompiler yang mengkompilasi skrip BML apa pun menjadi kode Java yang bebas refleksi. Hal ini menguntungkan dalam arti memungkinkan menangkap struktur antar-komponen aplikasi menggunakan bahasa yang dirancang untuk tujuan khusus ini dengan kemampuan tambahan untuk mengompilasinya menjadi kode Java 'biasa'.

## Tag BML

Berikut penjelasan beberapa tag yang digunakan dalam bahasa BML:

### Itu<bean> menandai:

Itu<bean> elemen digunakan untuk membuat kacang baru atau untuk mencari kacang dengan nama. Itu<bean> tag dengan format:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
The "id" dalam tag dikaitkan dengan registri objek untuk JavaBean.

### Itu<string> menandai

Ada dua cara tag string dapat digunakan:

1. Untuk membuat string yang tidak kosong:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Untuk membuat string kosong:

```
<string/>
```
## Referensi

* [Pesan Berorientasi Objek dengan XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Bahasa Markup Fisik](http://web.mit.edu/mecheng/pml/standards.htm)
* [Bahasa Markup Bean](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

