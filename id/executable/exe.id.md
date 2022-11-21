{
  "date" : "2021-06-30",
  "keywords" :[ "file exe", "format file exe", "apa itu file exe", "file", "contoh exe", "ekstensi file exe", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"File .exe adalah file Microsoft Executable yang dijalankan di OS Windows. Ketahui lebih banyak tentang format file EXE.",
  "title" :"Apa itu file EXE yang Dapat Dieksekusi?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Apa itu file EXE?

Kata EXE adalah kependekan dari **executable**. File .exe adalah program yang dapat dijalankan di sistem operasi Microsoft Windows. Pengembang aplikasi kebanyakan menerbitkan program mereka untuk OS Windows dalam format yang dapat dieksekusi sebagai file exe. Ini adalah format file standar untuk menjalankan aplikasi di Windows. **Setup.exe**, **Install.exe** dan **cmd.exe** adalah beberapa nama file EXE yang umum dan familiar.

## Berformat EXE

Kompiler MS-DOS diperkenalkan dengan model memori yang memiliki batasan memori 64K. Konsep umumnya adalah mengatur register segmen yang berbeda di CPU x86 (CS, DS, ES, SS) untuk menunjuk ke segmen yang berbeda atau sama, sehingga memungkinkan berbagai tingkat akses ke memori. Beberapa model memori khusus adalah:

- **Tiny**: Semua akses memori adalah 16-bit (register segmen tidak berubah). Menghasilkan file .COM alih-alih file .EXE.
- **Kecil**: Semua akses memori adalah 16-bit (register segmen tidak berubah).
- **Ringkas**: Alamat data mencakup segmen dan offset, memuat ulang register DS atau ES saat mengakses dan mengizinkan hingga 1 juta data. Akses kode tidak mengubah register CS, memungkinkan 64K kode.
- **Sedang**: Alamat kode mencakup alamat segmen, memuat ulang CS saat mengakses, dan mengizinkan hingga 1 juta kode. Akses data tidak mengubah register DS dan ES, memungkinkan 64K data.
- **Besar**: Alamat kode dan data adalah pasangan (segmen, offset), selalu memuat ulang alamat segmen. Seluruh ruang memori 1M byte tersedia untuk kode dan data.
- **Besar**: Sama seperti model besar, dengan aritmatika tambahan yang dihasilkan oleh kompiler untuk mengizinkan akses ke larik yang lebih besar dari 64K.

Pengembang harus memutuskan model mana yang harus dipilih saat membuat file exe.

### Format Berkas EXE Portabel

Format file portabel yang dapat dieksekusi (PE) berisi sejumlah header informasi, berikut ini adalah daftar header:

- **Header DOS**: Header MS-DOS memastikan kompatibilitas mundur, atau penurunan jenis file baru secara halus.
- **PE Header**: Pada offset 60 (0x3C) dari awal header DOS adalah penunjuk ke header File PE
- **COFF Header**: COFF header memiliki beberapa informasi yang berguna untuk file yang dapat dieksekusi, dan beberapa informasi yang lebih berguna untuk file objek.
- **Header Opsional PE**: Header Opsional PE terjadi langsung setelah header COFF, dan beberapa sumber bahkan menampilkan dua header sebagai bagian dari struktur yang sama.
- **Tabel Bagian**: Segera setelah Header Opsional PE, kami menemukan tabel bagian. Tabel bagian terdiri dari larik struktur IMAGE_SECTION_HEADER.
- **Bagian yang Dapat Dipetakan**: Dapat menghemat ruang di memori dengan memetakan kode perpustakaan ke lebih dari satu proses.

## Bisakah Anda menjalankan file EXE di Mac?

File exe tidak digunakan sebagai file yang dapat dieksekusi di Mac OS. Namun, jika Anda ingin menjalankan file exe di Mac OS, metode berikut dapat digunakan.

1. **Wine** - Wine adalah solusi sempurna bagi orang yang ingin menggunakan aplikasi PC mereka di sistem Mac. Ini adalah singkatan dari "Wine Is Not A Emulator," artinya. Wine menciptakan lingkungan direktori yang sama seperti yang digunakan oleh Microsoft sehingga Anda dapat menjalankan aplikasi Windows dengan menggunakannya.
2. **Mesin Virtual** - Buat Mesin Virtual Windows menggunakan Parallel Desktop atau VM Virtual Box dan jalankan aplikasi Anda di dalam mesin virtual.
3. **Boot Camp** - Menginstal dan mengonfigurasi Windows Boot Camp di Mac OS memungkinkan Anda menjalankan OS Windows di mesin Mac.

## Referensi

* [.exe- oleh Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

