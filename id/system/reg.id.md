{
"tanggal": "07-03-2023",
  "keywords": [
"file registrasi",
"apa itu file reg",
"mengajukan",
"ekstensi file reg",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File REG - File Registri Windows",
  "description":"Pelajari tentang format REG dan API yang dapat membuat dan membuka file REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent": "sistem"
}
},
"mod terakhir": "07-03-2023"
}

## Apa itu file REG?

File REG adalah format file yang digunakan untuk mengimpor atau mengekspor data Registri Windows. Registri Windows adalah basis data hierarki yang menyimpan pengaturan konfigurasi dan opsi untuk sistem operasi Windows dan aplikasi yang diinstal. Registri berisi informasi seperti preferensi pengguna, pengaturan aplikasi, data konfigurasi perangkat keras dan perangkat lunak, dan banyak lagi.

File REG biasanya memiliki ekstensi file ".reg" dan merupakan file teks biasa yang berisi serangkaian entri registri dan nilai dalam format tertentu. Formatnya terdiri dari bagian header yang mengidentifikasi file sebagai file registri, diikuti oleh serangkaian pasangan kunci dan nilai yang mewakili entri registri.

## Format File REG - Informasi Lebih Lanjut

Berikut adalah contoh format file reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Baris pertama file menentukan versi editor registri. Baris berikut berisi entri registri dalam format jalur kunci diikuti dengan nama nilai dan data nilai. Dalam contoh ini, file reg berisi dua entri: satu yang menambahkan program bernama "Example.exe" ke daftar startup Windows, dan satu lagi yang menetapkan nilai "Tersembunyi" di pengaturan lanjutan Windows Explorer ke "true".

File reg dapat dibuat dan diedit menggunakan editor teks seperti Notepad. Mereka sering digunakan untuk tujuan pencadangan dan pemulihan, serta untuk mengonfigurasi beberapa komputer dengan pengaturan registri yang sama.

## Impor atau Ekspor Registri Windows

File REG adalah jenis file yang digunakan untuk mengimpor atau mengekspor data dari Windows Registry. Registri Windows adalah basis data hierarki yang menyimpan pengaturan konfigurasi dan opsi untuk sistem operasi Windows dan aplikasi yang diinstal. Registri berisi informasi seperti preferensi pengguna, pengaturan aplikasi, data konfigurasi perangkat keras dan perangkat lunak, dan banyak lagi.

File reg dapat digunakan untuk membuat atau mengubah entri registri, dan sering kali digunakan untuk tujuan pencadangan dan pemulihan, serta untuk mengonfigurasi beberapa komputer dengan pengaturan registri yang sama. Berikut cara menggunakan file reg untuk menambahkan entri registri baru ke Windows Registry:

1. Buat file teks baru menggunakan editor teks seperti Notepad.
2. Ketik entri registri dalam format yang benar. Formatnya terdiri dari bagian header yang mengidentifikasi file sebagai file registri, diikuti oleh serangkaian pasangan kunci dan nilai yang mewakili entri registri. Berikut ini contohnya:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Ini menciptakan kunci baru yang disebut "Contoh" di bawah kunci "Perangkat Lunak" di kumpulan registri pengguna saat ini, dan menetapkan nilai "Pengaturan1" ke "Nilai1".

3. Simpan file dengan ekstensi file .reg.
4. Klik dua kali pada file .reg untuk menambahkan entri registri baru ke Windows Registry.

Anda akan diminta untuk mengonfirmasi bahwa Anda ingin menambahkan entri ke registri. Setelah Anda mengonfirmasi, entri baru akan ditambahkan ke registri, dan Anda dapat memverifikasinya menggunakan alat Editor Registri.

## Referensi
* [Registrasi Windows](https://en.wikipedia.org/wiki/Windows_Registry)

