{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MDMP - Format File Windows Minidump",
  "description":"Pelajari tentang format file MDMP dan API yang dapat membuat dan membuka file MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Apa itu file MDMP?

File MDMP adalah dump memori dari aplikasi di Microsoft Windows yang dibuat saat aplikasi menutup secara tidak normal atau macet. Ini berisi informasi dan data dump yang dapat digunakan untuk men-debug penyebab crash. File MDMP berlaku pada aplikasi yang dibuat oleh platform apa pun seperti Java, C++, .NET, dan lainnya. Selain MDMP,

Aplikasi yang dapat membuka file MDMP antara lain Microsoft Visual Studio Debugger.

## Format File MDMP

File MDMP disimpan sebagai file biner ke disk dan dapat dibuka dengan debugger Microsoft Visual Studio. Ini berisi informasi berikut untuk membantu mengidentifikasi alasan crash.

* Detail pesan Stop, parameternya, dan data lainnya
* Daftar driver yang dimuat
* Prosesor konteks (PRCB) untuk prosesor yang berhenti bekerja
* Proses informasi dan konteks kernel (EPROCESS) untuk proses yang berhenti
* Proses informasi dan konteks kernel (ETHREAD) untuk utas yang berhenti
* Tumpukan panggilan mode kernel untuk utas yang berhenti

Informasi ini membantu untuk mengetahui apa yang terjadi, memperbaiki masalah dan mencegahnya terjadi lagi.

### Analisis Minidump

Windows memerlukan file paging pada volume boot untuk membuat file dump memori. File halaman dibuat pada volume boot dan harus berukuran minimal 2 megabyte (MB). File dump dibuat saat aplikasi macet. Jika terjadi masalah kedua, file dump memori kecil kedua dibuat sementara yang sebelumnya dipertahankan. Nama file dump berbeda untuk menghindari penimpaan.

Windows menyimpan daftar semua berkas dump memori di map %SystemRoot%\Minidump. Anda dapat menganalisis file MDMP dengan menjalankannya di Visual Studio Debugger seperti yang tercantum dalam langkah-langkah di bawah ini.

## Bagaimana cara membuka file MDMP di Visual Studio?

Langkah-langkah berikut dapat digunakan untuk membuka file MDMP di Visual Studio.

* Di Visual Studio, dari menu File, pilih Open | Tempat Sampah Kecelakaan .
* Arahkan ke file dump yang ingin Anda buka.
* Pilih Buka.

## Referensi

* [Cara membaca file dump memori kecil yang dibuat oleh Windows jika terjadi kerusakan](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

