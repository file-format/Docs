{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extension", "file", "format", "system", "Driver", "System File", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Format File Sistem",
  "description":"Pelajari tentang format file SYS dan API yang dapat membuat dan membuka file SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Apa itu file SYS? ##

File SYS adalah "File sistem" yang digunakan di OS Windows dan aplikasi MS-DOS. File-file ini tidak dapat dibuka secara langsung dan terdiri dari driver dan konfigurasi perangkat. File SYS bertanggung jawab untuk memuat file fungsi inti dari sistem operasi. Ini dianggap sebagai file penting dari driver perangkat dan juga dapat digunakan saat masalah apa pun dari pembalap harus diselesaikan. Ini bertanggung jawab atas berfungsinya sistem komputer, dan file .sys harus benar dan lengkap.


## Spesifikasi Teknis ##

File .sys sebenarnya adalah subset dari format [BMP](/id/image/bmp/) karena hanya memungkinkan kombinasi tertentu. Format biasa dari file-file ini adalah seperti LOGOS.SYS, LOGOW.SYS, dan LOGO.SYS. File lain tidak memiliki format ini.

File-file ini sebagian besar digunakan dalam direktori *C* Windows pada saat instalasi. Sebagian besar masalah seputar driver perangkat diselesaikan dengan memperbarui OS Windows. Detail dan informasi dari file-file ini dapat dilihat dengan menggunakan program bawaan OS Windows. Ini juga terdiri dari referensi ke berbagai modul dalam sistem operasi.
Beberapa contoh file sistem adalah:

* IO.SYS (Ini menyimpan driver perangkat dari sistem operasi disk)
* MSDOS.SYS (Ini berisi kernel atau kode inti dari sistem operasi)
* CONFIG.SYS (Ini berisi berbagai opsi konfigurasi)
* KEYBOARD.SYS (Ini berisi informasi terkait tata letak keyboard)
* COUNTRY.SYS (Informasi terkait contan country dan codepage ini)

## Format File SYS ##

Microsoft mengembangkan file dengan ekstensi .sys. Variabel dan fungsi disertakan dalam file SYS. Ini sebagian besar digunakan oleh sistem operasi Microsoft. File-file ini terutama terletak di direktori root disk:

* C:\Windows\system32\driver
* C:\Windows\WinSxS

Beberapa peringatan umum tentang file SYS adalah sebagai berikut:

* Nama file ini tidak boleh diubah karena file ini bertanggung jawab atas fungsi inti dan variabel sistem operasi
* File-file ini tidak boleh dihapus karena tidak adanya file-file ini dapat menyebabkan kesalahan
* File .sys tidak boleh diunduh dari internet sampai Anda yakin tentang keabsahan sumbernya
* Seseorang tidak boleh mengacaukan file-file ini karena mengubahnya atau mengotak-atik ini menyebabkan kesalahan sistem yang serius
* Jika file-file ini rusak oleh beberapa virus atau malware, ini harus diinstal ulang

## Contoh SYS ##

Berikut ini adalah contoh file konfigurasi sistem SYS sederhana:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
