{
  "date" : "2021-06-24",
  "keywords" :[ "file bat", "apa itu file bat", "file", "contoh file bat", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file BAT dan API yang dapat membuat dan membuka file BAT.",
  "title" :"BAT - Format File Batch",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Apa itu file BAT?
File BAT dikenal sebagai file batch yang berjalan dengan DOS dan semua versi Windows, di bawah cmd.exe. Ini terdiri dari serangkaian perintah baris dalam teks biasa yang akan dieksekusi oleh juru bahasa baris perintah untuk melakukan tugas yang berbeda, seperti menjalankan utilitas pemeliharaan di dalam Windows atau memulai program tipikal. File batch dapat menyertakan perintah apa pun yang dapat diterima oleh juru bahasa secara interaktif dan menggunakan struktur kode yang memungkinkan percabangan dan perulangan bersyarat seperti yang tertulis di dalam file batch.
## format file BAT
Format file BAT hanyalah sebuah skrip yang digabungkan untuk mengotomatiskan urutan perintah yang sifatnya berulang. Istilah "batch" digunakan untuk pemrosesan batch, Ini dapat dianggap sebagai "eksekusi non-interaktif". Oleh karena itu file batch mungkin tidak memproses kumpulan dari banyak data. Di Disk Operating System (DOS) lama, file batch dijalankan di bawah antarmuka baris perintah dengan mengetikkan nama file dan ekstensi .bat. Sistem operasi berbasis antarmuka grafis Microsoft sebelumnya seperti Microsoft Windows bergantung pada DOS. Pengguna harus menggunakan DOS untuk melakukan operasi biasa seperti memperbaiki, mengoptimalkan, atau menginstal ulang Windows. Kemudian Microsoft memperkenalkan Windows NT yang tidak tergantung pada sistem operasi DOS. Oleh karena itu, file batch dapat dijalankan dengan menggunakan Command Prompt atau **cmd.exe** di sistem operasi Microsoft modern.
### Parameter file batch
Prompt perintah mendukung sejumlah variabel khusus seperti **%0, %1 hingga %9** untuk merujuk ke nama dan jalur tugas batch dan sembilan parameter panggilan dari dalam tugas batch. Parameter yang tidak ada diganti dengan string yang memiliki panjang nol. Meskipun, mereka dapat digunakan mirip dengan variabel lingkungan, tetapi tidak disimpan di lingkungan. Microsoft dan IBM menyebut variabel-variabel ini sebagai parameter pengganti, Sementara Novell, Digital Research, dan Caldera memperkenalkan variabel pengganti istilah untuk mereka.

Berikut adalah beberapa perintah file Batch yang berguna:
| Komando | Deskripsi |
------|------------|
| VER | Perintah batch ini menunjukkan versi MS-DOS yang Anda gunakan. |
|ASSOC| Ini adalah perintah batch yang mengaitkan ekstensi dengan jenis file (FTYPE), menampilkan asosiasi yang ada, atau menghapus asosiasi. |
|CD| Perintah batch ini membantu membuat perubahan pada direktori yang berbeda, atau menampilkan direktori saat ini. |
|CLS| Perintah batch ini membersihkan layar. |
|SALIN| Perintah batch ini digunakan untuk menyalin file dari satu lokasi ke lokasi lain. |
|DEL| Perintah batch ini menghapus file dan bukan direktori. |
|DIR| Perintah batch ini mencantumkan isi direktori. |
|TANGGAL| Perintah batch ini membantu menemukan tanggal sistem. |
|ECHO| Perintah batch ini menampilkan pesan, atau mengaktifkan atau menonaktifkan gema perintah. |
|KELUAR| Perintah batch ini keluar dari konsol DOS. |
|MD| Perintah batch ini membuat direktori baru di lokasi saat ini. |
|PINDAHKAN| Perintah batch ini memindahkan file atau direktori antar direktori. |
|PATH| Perintah batch ini menampilkan atau menetapkan variabel path. |
|JEDA| Perintah batch ini meminta pengguna dan menunggu baris input dimasukkan. |
|PROMPT| Perintah batch ini dapat digunakan untuk mengubah atau mereset prompt cmd.exe. |
|RD| Perintah batch ini menghapus direktori, tetapi direktori harus kosong sebelum dapat dihapus. |
|REN| Mengganti nama file dan direktori |
|REM| Perintah batch ini digunakan untuk komentar dalam file batch, mencegah konten komentar dieksekusi. |
|MULAI| Perintah batch ini memulai program di jendela baru, atau membuka dokumen. |
|WAKTU| Perintah batch ini mengatur atau menampilkan waktu. |
|JENIS| Perintah batch ini mencetak konten file atau file ke output. |
|VOL| Perintah batch ini menampilkan label volume. |
|ATTRIB| Menampilkan atau mengatur atribut file di direktori curret |
|CHKDSK| Perintah batch ini memeriksa disk untuk masalah apa pun. |
|PILIHAN| Perintah batch ini memberikan daftar opsi kepada pengguna. |
|CMD| Perintah batch ini memanggil contoh lain dari command prompt. |
|KOMPOS| Perintah batch ini membandingkan 2 file berdasarkan ukuran file. |
|KONVERSI| Perintah batch ini mengubah volume dari sistem file FAT16 atau FAT32 ke sistem file NTFS. |
|DRIVERQUERY| Perintah batch ini menunjukkan semua driver perangkat yang diinstal dan propertinya. |
|PERLUAS| Perintah batch ini mengekstrak file dari file kabinet .cab terkompresi. |
|TEMUKAN| Perintah batch ini mencari string dalam file atau input, menghasilkan baris yang cocok. |
|FORMAT| Perintah batch ini memformat disk untuk menggunakan sistem file yang didukung Windows seperti FAT, FAT32 atau NTFS, sehingga menimpa konten disk sebelumnya. |
|BANTUAN| Perintah batch ini menunjukkan daftar perintah yang disediakan Windows. |
|IPCONFIG| Perintah batch ini menampilkan Konfigurasi IP Windows. Menampilkan konfigurasi berdasarkan koneksi dan nama koneksi tersebut. |
|LABEL| Perintah batch ini menambah, menyetel, atau menghapus label disk. |
|LEBIH| Perintah batch ini menampilkan konten file atau file, satu layar dalam satu waktu. |
|BERSIH| Menyediakan berbagai layanan jaringan, tergantung pada perintah yang digunakan. |
|PING| Perintah batch ini mengirimkan paket "echo" ICMP/IP melalui jaringan ke alamat yang ditentukan. |
|MATIKAN| Perintah batch ini mematikan komputer, atau log off pengguna saat ini. |
|SORT| Perintah batch ini mengambil input dari file sumber dan mengurutkan isinya menurut abjad, dari A ke Z atau Z ke A. Outputnya dicetak di konsol. |
|SUBS| Perintah batch ini memberikan huruf drive ke folder lokal, menampilkan tugas saat ini, atau menghapus tugas. |
|SISTEMINFO| Perintah batch ini menunjukkan konfigurasi komputer dan sistem operasinya. |
|TASKILL| Perintah batch ini mengakhiri satu atau lebih tugas. |
|DAFTAR TUGAS| Perintah batch ini mencantumkan tugas, termasuk nama tugas dan id proses (PID). |
|XCOPY| Perintah batch ini menyalin file dan direktori dengan cara yang lebih canggih. |
|POHON| Perintah batch ini menampilkan pohon dari semua subdirektori dari direktori saat ini ke tingkat rekursi atau kedalaman apa pun. |
|FC |Perintah kumpulan ini mencantumkan perbedaan aktual antara dua file. |
|DISKPART |Perintah batch ini menampilkan dan mengonfigurasi properti partisi disk. |
|TITLE |Perintah batch ini menetapkan judul yang ditampilkan di jendela konsol. |
|SET | Menampilkan daftar variabel lingkungan pada sistem saat ini. |

## Contoh file BAT
Skrip batch biasanya disimpan sebagai file teks sederhana; berisi perintah yang dieksekusi secara berurutan. File-file ini disimpan dengan ekstensi .bat; dikenali dan dijalankan dengan menggunakan perangkat lunak **Command Interpreter**. Perangkat lunak ini tersedia secara native di Microsoft Windows dengan nama **cmd.exe**.

Berikut adalah contoh Batch Script yang menghapus semua file di direktori saat ini:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referensi

* [Skrip Kumpulan - Panduan Cepat](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [File batch - oleh Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

