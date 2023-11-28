{
  "date" : "2023-01-31",
  "keywords" :["menjalankan file", "apa itu file yang dijalankan", "file", "cara membuka file yang dijalankan", "menjalankan ekstensi file","ekstensi"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file RUN dan API yang dapat membuat dan membuka file RUN.",
  "title" :"JALANKAN Format File - File Eksekusi Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Apa itu file RUN?

Format file .run biasanya digunakan untuk mendistribusikan software atau installer aplikasi di lingkungan Linux. Untuk menginstal perangkat lunak, Anda perlu membuat file tersebut dapat dieksekusi, yang dapat dilakukan dengan menggunakan perintah berikut:

```bash
chmod +x file_name.run 
```

Kemudian, Anda dapat menjalankan file tersebut menggunakan perintah berikut:

```bash
./file_name.run 
```

Proses instalasi mungkin berbeda-beda tergantung pada file dan program spesifik yang Anda coba instal.

Format file .run adalah jenis skrip shell yang digunakan untuk mendistribusikan penginstal perangkat lunak atau aplikasi di lingkungan Linux. Ini adalah paket mandiri yang mencakup semua yang diperlukan untuk menginstal perangkat lunak, termasuk file biner, perpustakaan, dan file konfigurasi.

Penting untuk dicatat bahwa file .run juga dapat berisi kode berbahaya, jadi sebaiknya verifikasi sumber file dan pindai virus sebelum menjalankannya.

Selain itu, beberapa file .run mungkin memerlukan hak akses root untuk menjalankan dan menginstal, jadi Anda mungkin perlu menggunakan perintah "sudo" untuk menjalankan file dengan izin yang lebih tinggi:

```bash
sudo ./filename.run
```

## Bagaimana cara membuka file RUN?

Untuk membuka file .run, Anda harus membuatnya dapat dieksekusi, yang dapat dilakukan dengan perintah "chmod":

```bash
chmod +x filename.run 
```

Setelah file dibuat dapat dieksekusi, Anda dapat menjalankannya dengan mengetik:

```bash
./filename.run
```

Menjalankan file .run tidak sama dengan membukanya di editor teks. Menjalankan file .run akan menjalankan instruksinya, yang bisa berupa apa saja mulai dari menginstal program hingga menjalankan skrip. Untuk melihat konten file .run, Anda perlu membukanya di editor teks, seperti nano atau vim:

```
nano filename.run
```
atau
```
vim filename.run
```

## Referensi
* [Cara Mengeksekusi File .bin dan .run di Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


