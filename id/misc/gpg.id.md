{
  "date" : "2022-02-17",
  "keywords" :["file gpg", "format file gpg", "apa itu file gpg", "file", "contoh gpg", "ekstensi file gpg", "ekstensi", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File GPG - File Kunci Publik Penjaga Privasi GNU",
  "description":"Pelajari tentang file GPG dan API yang dapat membuat dan membuka file GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Apa itu file GPG?

File GPG adalah file kunci enkripsi/dekripsi yang digunakan oleh program enkripsi GNU Privacy Guard (GnuPG). Program GnuPC itu sendiri didasarkan pada standar OpenPGP sebagaimana didefinisikan RFC4880 dan juga dikenal sebagai PGP. Kunci keberhasilan penggunaan GPG dalam sistem operasi modern adalah sistem manajemen kuncinya yang serbaguna. Utilitas baris perintah GPG membuatnya mudah diintegrasikan dengan aplikasi lain.

## Format File GPG

File GPG disimpan sebagai file biner terenkripsi dan tentu saja tidak dapat dibaca manusia. Untuk mendekripsi file GPG terenkripsi, Anda perlu menggunakan kunci aman yang sama. Dan itulah mengapa format file internal dari file-file ini tidak diketahui.

## Enkripsi dan Dekripsi File dengan GPG di Linux

Utilitas baris perintah GPG dapat digunakan untuk mengenkripsi dan mendekripsi file di Linux.

### Mengenkripsi File

File dapat dienkripsi menggunakan perintah gpg dengan opsi -c (buat) seperti yang ditunjukkan di bawah ini.

```
gpg -c file1.txt
```
Menjalankan perintah ini akan meminta frasa kunci untuk mengenkripsi konten file asli `file1.txt`. Ini menghasilkan pembuatan file terenkripsi file1.txt.gpg.

### Mendekripsi dan Mengekstrak File

Untuk mendekripsi dan mengekstrak file terenkripsi, perintah berikut dapat digunakan.

```
gpg cfile.txt.gpg
```

## Referensi

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

