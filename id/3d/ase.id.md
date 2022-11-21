{
  "date" : "2021-01-22",
  "keywords" :[ "ASE", "file", "format", "jenis file", "ekstensi", "apa itu file ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file ASE dan API yang dapat membuka dan membuat file ASE.",
  "title" :"ASE - File Ekspor Adegan ASCII Autodesk",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Apa itu file ASE?

File dengan ekstensi .ase adalah format file Autodesk ASCII Scene Export yang merupakan representasi ASCII dari sebuah scene, berisi informasi 2D atau 3D saat mengekspor data scene menggunakan Autodesk. Autodesk menyediakan opsi untuk menyertakan komponen adegan saat mengekspor data adegan. Anda dapat memasukkan definisi Mesh bersama dengan informasi titik dan wajah, Deskripsi material, mengubah data animasi untuk objek, menyelesaikan definisi mesh dari setiap n bingkai, data animasi untuk kamera dan lampu, dan pengaturan sambungan IK.

## Format File ASE - Informasi Lebih Lanjut

File ASE adalah file teks yang disimpan dalam format ASCII yang dapat dibuka di editor teks apa pun. File ASE dapat berisi jenis informasi berikut yang disediakan oleh Autodesk.

### Opsi Keluaran

* `Mesh Definition` - Mengekspor definisi setiap mesh, termasuk informasi titik dan wajah untuk objek geometris. Selain itu, mengaktifkan ini akan mengaktifkan item dalam kotak grup Opsi Jala, yang dijelaskan di bawah.
* `Bahan` - Termasuk deskripsi bahan. Jika suatu material tidak ditugaskan ke suatu objek, warna wireframe-nya akan diekspor. Semua level pohon materi disertakan, jadi ini bisa menghasilkan banyak teks.
* `Transform Animation Keys` - Termasuk data animasi transformasi untuk objek. Jika objeknya adalah kamera target atau lampu sorot, ini akan menyertakan data animasi target.
* `Animated Mesh` - Mengekspor definisi mesh lengkap dari setiap n frame. Frekuensi ditentukan oleh spinner Keluaran Pengontrol, dijelaskan di bawah ini. Setiap blok berisi informasi yang sama yang ditentukan dalam kotak grup Mesh Options, dijelaskan di bawah ini. Mengaktifkannya dapat menghasilkan file besar, bahkan untuk adegan kecil.
* `Pengaturan Kamera/Cahaya Animasi` - Mengekspor data animasi untuk kamera dan lampu, seperti warna, intensitas, falloff, bias peta, dan sebagainya. Keluarkan satu blok setiap n bingkai, seperti yang ditentukan oleh pemintal Output Pengontrol.
* `Inverse Kinematic Joints` - Mengekspor pengaturan gabungan IK di cabang Hirarki.

### Tipe Objek

Item di sini memungkinkan Anda menentukan kategori objek mana yang ingin Anda sertakan dalam output. Anda dapat menyertakan objek geometris, bentuk, kamera, lampu, dan objek pembantu.

* Geometris
* Bentuk
* Kamera
* Lampu
* Pembantu

### Opsi Jaring

* `Mesh Normals` - Mengekspor wajah dan titik normal. Normal dari wajah dicantumkan terlebih dahulu, diikuti oleh normal dari tiga simpul yang menopang wajah. Mengaktifkan ini menghasilkan file yang jauh lebih besar.
* `Koordinat Pemetaan` - Mengekspor daftar simpul dan permukaan pemetaan, menurut struktur TVert dan TVFace yang dijelaskan dalam Kit Pengembangan Perangkat Lunak 3ds Max. Jika objek menggunakan pemetaan wajah, daftar peta wajah akan diekspor yang berisi koordinat UVW untuk setiap wajah.
* `Vertex Colors` - Mengekspor warna vertex.

### Keluaran Pengontrol

* `Use Keys` - Mengekspor nilai kunci. Jika controller tidak menggunakan kunci, maka metode Force Sample digunakan. Dalam kasus pengontrol transformasi, opsi Gunakan Tombol hanya berfungsi jika semua pengontrol transformasi adalah Linear/TCB atau Bezier. Jika salah satu track transformasi menggunakan jenis pengontrol yang berbeda, maka metode Force Sample digunakan untuk semua track transformasi.
* `Force Samples` - Nilai pengontrol sampel berdasarkan frekuensi yang ditentukan dalam Bingkai per Pengontrol Sampel.

## Referensi

* [Autodesk - Mengekspor ke ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

