{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "ekstensi", "file", "format", "sistem", "Inisiasi", "ekstensi direktori", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Format File Inisiasi",
  "description":"Pelajari tentang format file INI dan API yang dapat membuat dan membuka file INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Apa itu file INI? ##

File INI adalah dokumen konfigurasi pesan untuk program komputer yang berisi kunci publik untuk karakteristik dan bagian yang mengatur atribut dalam kerangka kerja dan tata bahasa. Dokumen konfigurasi format file sistem ini mendapatkan namanya dari ekstensi direktori sistem operasi MS-DOS INI, yang berarti inisiasi. Ini mempopulerkan bentuk pengaturan perangkat lunak ini. Banyak program pada aplikasi perangkat lunak lain menggunakan berbagai penambahan nama file, seperti CONF dan [CFG](/id/system/cfg/), meskipun format tersebut telah membentuk standar tidak resmi dalam banyak situasi konfigurasi.

## Sejarah Singkat File INI##

Awalnya, teknik konfigurasi program utama Windows adalah format file teks yang terdiri dari baris teks dengan satu pasangan penting per baris, dibagi menjadi beberapa bagian. Driver perangkat, tipografi, dan peluncur awal semuanya disimpan dalam format ini. Pengaturan individual juga biasanya disimpan dalam file INI oleh aplikasi.
Hingga Windows 3.1x, format ini didukung pada platform Microsoft Windows 16-bit. Dimulai dengan Windows 95, Microsoft mulai mendorong pengembang untuk menggunakan Windows Registry daripada file INI untuk konfigurasi.

## File INI - Spesifikasi Format File

### Kunci/Properti ###

Kunci/properti adalah elemen paling dasar dari file INI. Simbol sama dengan (=) memisahkan nama dan nilai setiap kunci. Di sebelah kiri tanda sama dengan adalah tempat nama ditampilkan. Simbol yang sama dan titik koma adalah huruf rahasia di sistem Windows sehingga tidak dapat digunakan di kunci. Karakter apa pun dapat digunakan dalam nilai.

```
name=value
```

### Bagian ###

Komentar bagian muncul dalam tanda kurung siku ([]) pada barisnya sendiri. Setelah definisi bagian, semua kunci ditautkan ke bagian itu. Bagian selesai pada penunjukan bagian berikutnya atau akhir dokumen; tidak ada pemisah "akhir bagian" khusus. Bagian tidak dapat ditumpuk; mereka hanya dapat diberi nama satu kali dan tidak perlu ditautkan.

```
[section]
a=a
b=b
```

### Mengubah fitur ###

Format file INI tidak memiliki definisi yang diterima secara global. Banyak aplikasi komputer menyertakan fungsi selain yang telah disebutkan. Daftar di bawah ini mencakup beberapa karakteristik umum yang mungkin disertakan atau tidak disertakan dalam setiap program.

* Komentar
* Melarikan diri karakter
* Duplikat nama


## INI Contoh ##

Contoh file INI terlihat sebagai berikut:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Referensi ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

