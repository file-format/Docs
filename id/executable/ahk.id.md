{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file AHK dan API yang dapat membuat dan membuka file AHK.",
  "title" :"Format File AHK- File Skrip AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Apa itu file AHK?

File AHK adalah file skrip yang dibuat dengan aplikasi perangkat lunak AutoHotkey yang digunakan untuk otomatisasi tugas di Microsoft Windows. Ini berisi instruksi untuk otomatisasi tugas menggunakan tombol pintas yang dapat digunakan untuk melakukan tindakan instan. File dijalankan oleh AutoHotkey dan semua tindakan dilakukan secara berurutan. File AHK cukup kuat untuk melakukan tugas-tugas kompleks menggunakan hotkey yang ditentukan menggunakan hotkey. File AHK dapat dibuka dengan editor teks seperti Microsoft Notepad dan Notepad++.

## Format File AHK

File AHK disimpan ke disk sebagai file teks biasa dan berisi baris kode yang dapat dijalankan oleh AutoHotkey. AutoHotkey adalah bahasa skrip open-source gratis dan memungkinkan pengguna untuk membuat skrip sederhana hingga kompleks untuk melakukan tindakan seperti mengisi formulir, mengklik otomatis, mengeksekusi makro, dll. File AHK minimal dapat melakukan satu tindakan dan kemudian keluar .

Ada alat yang tersedia yang dapat digunakan untuk mengonversi file AHK ke [Exe](/id/executable/exe/).

### Contoh AHK

Contoh berikut menggunakan tombol Win+Z untuk menjalankan Microsoft Notepad atau membawanya ke depan jika sudah berjalan.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Bagaimana cara membuat file AHK?

Langkah-langkah berikut dapat digunakan untuk membuat file AHK. Ini mengasumsikan bahwa AutoHotkey sudah diinstal pada mesin.

* Klik kanan pada desktop Anda.
* Temukan "Baru" di menu.
* Klik "AutoHotkey Script" di dalam menu "New".
* Beri skrip nama baru.
* Temukan file yang baru dibuat di desktop Anda dan klik kanan.
* Klik "Edit Skrip".
* Sebuah jendela seharusnya muncul, mungkin Notepad.
* Simpan File.

## Referensi

* [AutoHotkey](https://www.autohotkey.com/)
* [File batch - oleh Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

