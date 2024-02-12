{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File CUBE - File Kubus Gaussian - Apa itu file .cube dan cara membukanya?",
  "description" : "Pelajari tentang File Gaussian Cube dan cara membukanya.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-id-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Apa itu berkas KUBUS?

Format file CUBE, juga dikenal sebagai file Gaussian Cube (.cube) digunakan dalam kimia komputasi untuk menyimpan data molekul, khususnya informasi kerapatan elektron yang dihasilkan dari perhitungan kimia kuantum. Format ini umumnya dikaitkan dengan **paket perangkat lunak Gaussian**, yang banyak digunakan untuk melakukan penghitungan struktur elektronik ab initio.

File Gaussian Cube menyimpan data tiga dimensi, biasanya mewakili kerapatan elektron atau sifat molekul lainnya, yang diperoleh melalui perhitungan kimia kuantum. File tersebut berisi bagian header dengan metadata (seperti asal, jumlah titik data di sepanjang setiap sumbu, dan jarak), diikuti dengan kisi-kisi nilai numerik yang mewakili properti yang diinginkan (misalnya, kerapatan elektron) di setiap titik kisi dalam ruang.

File Gaussian Cube (.cube) adalah file teks biasa dengan struktur tertentu. Header berisi informasi tentang sistem molekuler dan grid data, dan nilai data disusun dalam format grid tiga dimensi. File Gaussian Cube sering digunakan untuk memvisualisasikan sifat molekul menggunakan perangkat lunak visualisasi molekul. Program seperti **VMD (Visual Molecular Dynamics)** atau **PyMOL** dapat membaca file Gaussian Cube untuk menampilkan permukaan molekul, kerapatan elektron, atau properti terhitung lainnya.

## Contoh sederhana file Gaussian Cube:

```
Contoh File Kubus
Dihasilkan oleh Gaussian
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (nilai data kerapatan elektron pada setiap titik grid)
```

## Tentang Gaussian

Gaussian adalah rangkaian aplikasi perangkat lunak untuk kimia kuantum dan kimia komputasi. Fokus utama Gaussian adalah pada metode kimia kuantum ab initio, yang merupakan pendekatan yang sangat akurat namun intensif komputasi untuk mempelajari struktur elektronik molekul. Perangkat lunak ini banyak digunakan dalam penelitian dan akademik untuk berbagai aplikasi, termasuk memprediksi sifat molekul, mempelajari mekanisme reaksi, dan mengeksplorasi struktur molekul.

## Tentang NWChem

NWChem adalah perangkat lunak kimia komputasi sumber terbuka yang dirancang untuk simulasi kimia kuantum berkinerja tinggi. Ia menggunakan metode ab initio seperti Hartree-Fock dan teori fungsional kepadatan, mendukung komputasi paralel untuk penghitungan cluster yang efisien, dan dapat diterapkan di berbagai bidang ilmiah, termasuk kimia komputasi, biokimia, dan ilmu material. NWChem terkenal karena keserbagunaannya, memungkinkan peneliti mempelajari berbagai sistem kimia, dan sifat sumber terbukanya mendorong kontribusi dan penyesuaian komunitas.

## Tentang VMD

VMD, singkatan dari Visual Molecular Dynamics, adalah program visualisasi molekuler yang kuat dan banyak digunakan untuk menampilkan, menganalisis, dan menganimasikan lintasan dinamika molekuler (MD), serta struktur molekul statis. Ini sangat populer di bidang kimia komputasi, biologi molekuler, dan bioinformatika struktural. VMD unggul dalam memvisualisasikan struktur molekul, memberikan rendering 3D molekul dan kompleks molekul berkualitas tinggi. Ini mendukung berbagai format file molekuler.

## Tentang PyMOL

PyMOL adalah sistem visualisasi molekuler dan alat perangkat lunak yang digunakan untuk visualisasi tiga dimensi struktur molekul. Ini sangat populer di bidang biologi struktural, bioinformatika, dan kimia komputasi. PyMOL menyediakan rendering 3D struktur molekul berkualitas tinggi, memungkinkan pengguna memvisualisasikan dan menjelajahi bentuk, permukaan, dan interaksi makromolekul biologis.

## Bagaimana cara membuka file CUBE?

File CUBE dapat dibuka dan direferensikan menggunakan program berikut.

- **NWChem** (Gratis) untuk (Windows, MAC, Linux)

## Referensi
* [Format File Kubus Gaussian](https://paulbourke.net/dataformats/cube/)
