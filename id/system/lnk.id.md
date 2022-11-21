{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "ekstensi", "file", "format", "sistem", "file LNK", "tautan", "file LNK", "dokumen LNK", "aplikasi", "program" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Format File Tautan",
  "description":"Pelajari tentang format file LNK dan API yang dapat membuat dan membuka file LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Apa itu file LNK? ##

File LNK, analog dengan identitas pada sistem Mac, adalah alternatif Windows atau "tautan" yang berfungsi sebagai koneksi ke folder atau program dokumen gambar asli. Ini berisi jenis, posisi, dan nama file tujuan pintasan, serta aplikasi yang membuka dokumen target dan tombol pintasan tambahan.

Di Windows, luruskan file, folder, atau program yang dapat dieksekusi dan pilih Buat pintasan. Lokasi format file dan direktori "Awal" adalah dua fitur dasar file LNK. Format file dari file LNK disamarkan, dan panah melengkung menunjukkan bahwa itu adalah pintasan.

## Format File LNK ##

Format file LNK biasanya memiliki ikon yang sama dengan file tujuannya, tetapi dengan tambahan panah melengkung kecil untuk menunjukkan bahwa file tersebut mengarah ke lokasi yang berbeda. Saat pintasan diklik dua kali, pintasan tersebut berperilaku seolah-olah pengguna telah mengklik dua kali file yang sebenarnya.

File LNK yang berisi pintasan aplikasi dapat memiliki properti yang memengaruhi cara program berjalan. Untuk mengubah atribut, klik kanan file pintasan dan pilih **Properti**, lalu ubah kolom Target.

Alih-alih menjadi ekstensi file, file LNK adalah ekstensi Windows Explorer. Sebagai ekstensi terminal, dokumen .lnk hanya dapat digunakan di Windows Explorer untuk menggantikan file, dan mereka memiliki tujuan lain di Windows Explorer selain berfungsi sebagai pintasan ke dokumen lokal. File-file ini dimulai dengan huruf "L" juga.

Meskipun tautan pintasan ke file dan direktori tertentu saat dibuat, pintasan tersebut mungkin tidak dapat dioperasikan jika target diubah ke lokasi yang berbeda. Explorer akan mulai memperbaiki folder pintasan yang mengarah ke target mati saat dibuka.


## Spesifikasi Teknis ##

Hanya ketika pengaturan tampilan folder "Sembunyikan ekstensi untuk jenis file yang dikenali" tidak dicentang, Windows tidak menampilkan ekstensi dokumen .lnk untuk pintasan dokumen. Meskipun tidak disarankan, Anda dapat mengaktifkan ekstensi file untuk ditampilkan dengan menghapus properti "NeverShowExt" dari item registri Windows file HKEY_CLASSES_ROOT\lnk.

Untuk melakukannya, lakukan langkah-langkah ini:

* Buka "Editor Registrasi" dengan memasukkan "Regedit" ke dalam bidang pencarian bilah tugas dan memilih program
* Dalam aplikasi, navigasikan ke lokasi file Computer\HKEY HKEY_CLASSES_ROOT\lnk
* Buat cadangan item dengan mengklik kanan dan memilih Ekspor
* Pilih dan hapus atribut "NeverShowExt".
* Windows harus di-restart


## Referensi ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
