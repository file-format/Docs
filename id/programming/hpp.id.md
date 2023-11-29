{
"tanggal": "08-06-2023",
  "keywords": [
"file hp",
"apa itu file hpp",
"apa isi file hpp",
"contoh file hpp",
"apa format file hpp",
"mengajukan",
"ekstensi file hpp",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File HPP - File Header C++",
  "description":"Pelajari tentang format HPP dan API yang dapat membuat dan membuka file HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent" : "programming"
}
},
"mod terakhir": "08-06-2023"
}

## Apa itu file HPP?

Format file ".hpp" umumnya digunakan untuk file header dalam bahasa pemrograman C++. File header biasanya berisi deklarasi dan definisi fungsi, kelas, variabel, dan konstanta yang digunakan oleh file kode sumber lain dalam proyek C++.

Tujuan penggunaan file header adalah untuk menyediakan cara berbagi kode umum ke beberapa file kode sumber tanpa menduplikasi kode itu sendiri. Ketika file sumber C++ perlu mengakses deklarasi atau definisi dari file header, file header tersebut disertakan menggunakan arahan praprosesor `#include`.

Ekstensi file ".hpp" sering digunakan untuk menunjukkan bahwa suatu file adalah file header C++. Penggunaan ekstensi khusus ini untuk file header tidak diwajibkan, dan Anda mungkin juga menemukan file header dengan ".h" atau ekstensi lainnya. Pilihan perluasan sebagian besar merupakan masalah konvensi dan preferensi pribadi.

Ketika file sumber C++ menyertakan file header menggunakan `#include`, kompiler secara efektif menggabungkan konten file header dengan file sumber sebelum mengkompilasinya sebagai satu unit. Hal ini memungkinkan file sumber untuk mengakses deklarasi dan definisi dalam file header, memberikan informasi yang diperlukan bagi kompiler untuk melakukan pemeriksaan tipe dan pembuatan kode.

## Apa isi file HPP?

Berikut beberapa konten umum yang mungkin Anda temukan di file ".hpp":

- **Deklarasi fungsi:** File header sering kali menyertakan deklarasi fungsi tanpa implementasi sebenarnya. Deklarasi ini memberikan informasi tentang nama fungsi, tipe kembalian, dan parameter, sehingga file kode sumber lain dapat menggunakan fungsi tanpa perlu mengetahui detail implementasi.
- **Deklarasi kelas:** File header dapat berisi deklarasi kelas, termasuk nama kelas, variabel anggota, fungsi anggota, dan penentu akses. Dengan menyertakan deklarasi kelas dalam file header, file kode sumber lain dapat membuat objek kelas tersebut dan mengakses anggotanya.
- **Deklarasi konstan:** File header dapat menentukan konstanta, seperti variabel global atau nilai enum yang dimaksudkan untuk dibagikan ke beberapa file kode sumber. Konstanta ini dapat diakses dengan menyertakan file header di file sumber lain, sehingga memungkinkan mereka menggunakan konstanta yang ditentukan.
- **Definisi tipe:** File header mungkin berisi definisi tipe menggunakan kata kunci "typedef" atau alias tipe menggunakan kata kunci "menggunakan". Definisi ini menciptakan nama baru untuk tipe yang sudah ada, membuat kode lebih mudah dibaca dan dipelihara.
- **Definisi fungsi sebaris:** Dalam beberapa kasus, file header mungkin berisi definisi fungsi sebaris. Fungsi inline adalah fungsi kecil yang diperluas di lokasi panggilan daripada dipanggil sebagai fungsi terpisah. Menyertakan definisi fungsi sebaris dalam file header memungkinkan kompiler mengganti pemanggilan fungsi dengan isi fungsi secara langsung, sehingga berpotensi meningkatkan kinerja.

## Contoh File HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Apa format file HPPnya?

HPP adalah file teks biasa tetapi mengikuti aturan umum dan sintaksis bahasa pemrograman C++. Berikut rincian format umum dan struktur file ".hpp":

- **Pelindung header:** Biasanya, file ".hpp" diawali dengan pelindung header untuk mencegah penyertaan beberapa file yang sama. Hal ini dicapai dengan menggunakan arahan praprosesor seperti `#ifndef`, `#define` dan `#endif`. Penjaga header memastikan bahwa konten file hanya disertakan satu kali selama proses kompilasi.
- **Sertakan pernyataan:** Setelah pelindung header, Anda dapat menyertakan file header lain yang diperlukan menggunakan direktif `#include`. Ini mungkin termasuk header perpustakaan standar atau header khusus lainnya yang diperlukan oleh kode Anda.
- **Deklarasi dan Definisi:** Konten utama file ".hpp" adalah deklarasi dan, dalam beberapa kasus, definisi kelas, fungsi, konstanta, alias tipe, dan elemen lainnya. Misalnya, Anda dapat mendeklarasikan kelas menggunakan kata kunci `class`, fungsi menggunakan tipe kembaliannya, nama, dan daftar parameternya, serta konstanta menggunakan kata kunci `const` diikuti dengan tipe dan namanya.
- **Definisi Fungsi Sebaris:** Dalam kasus tertentu, Anda dapat menyertakan definisi fungsi sebaris secara langsung di file ".hpp". Fungsi inline biasanya didefinisikan di dalam badan kelas, artinya definisi fungsi disertakan bersama deklarasinya. Hal ini dapat dilakukan dengan mengawali definisi fungsi dengan kata kunci `inline`.
- **Deklarasi Namespace:** Jika Anda menggunakan namespace dalam kode, Anda dapat mendeklarasikannya dalam file ".hpp". Hal ini dilakukan dengan menggunakan kata kunci `namespace` diikuti dengan nama namespace dan menyertakan kode yang relevan dalam blok namespace.

## Referensi
* [File header (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

