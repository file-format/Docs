{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "file", "ekstensi", "format file", "Bahasa pemrograman karat", "Panduan Pemrograman", "Contoh RS", "Karat", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Berkas Pemrograman Karat",
  "description":"Pelajari tentang format file RS dan API yang dapat membuat dan membuka file RS.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Apa itu file RS?

Sebuah file dengan ekstensi RS milik bahasa pemrograman Rust, itu adalah bahasa pemrograman multi-perangkat, tingkat tinggi, umum-perhatian yang dirancang untuk kinerja dan keamanan, terutama keamanan keamanan. Karat secara sintaksis mirip dengan С++ tetapi dapat menjamin keamanan memori dengan menggunakan pemeriksa pinjaman untuk memvalidasi referensi. Bahasa karat mencapai keamanan memori tanpa pengumpulan sampah, dan penghitungan referensi adalah opsional.

## Format File RS ##

Rust awalnya dirancang oleh Graydоn Hоаre di Mozilla Research, dengan kontribusi dari Dave Herman, Brendаn Eich, dan lain-lain. Ini telah semakin banyak digunakan dalam industri, dan Microsoft telah bereksperimen dengan bahasa untuk komponen perangkat lunak yang aman dan penting untuk keamanan.

Rust telah dipilih sebagai "bahasa pemrograman yang paling disukai" di Survei Pengembang Stасk Оverflоw setiap tahun sejak 2016, meskipun hanya digunakan oleh 7% responden dalam survei 2021. Bersamaan dengan pengetikan statistik konvensional, sebelum versi 0.4, Rust juga mendukung pengetikan.

Sistem pengetikan telah memodelkan pernyataan pernyataan sebelum dan sesudah program, melalui penggunaan pernyataan pemeriksaan khusus. Perbedaan dapat ditemukan pada waktu yang bersamaan, bukan pada waktu proses, seperti yang mungkin terjadi pada pernyataan dalam kode С atau С++. Konsep tipografi tidak unik untuk Rust, karena pertama kali diperkenalkan dalam bahasa NIL. Tipografi telah dihapus karena dalam praktiknya jarang digunakan, meskipun fungsi yang sama dapat dicapai dengan memanfaatkan semantik gerakan Rust.

Bahasa pemrograman Rust membantu Anda menulis perangkat lunak yang lebih cepat dan lebih andal. Ergоnоmi tingkat tinggi dan kontrol рrоgаr аdаlаh аdаlаh dаlаm desain bahasa pemrograman; Tantangan karat yang bertentangan. Melalui penyeimbangan kapasitas teknis yang kuat dan pengalaman pengembang yang hebat, Rust memberi Anda opsi untuk mengontrol detail tingkat rendah (seperti penggunaan memori) tanpa semua kerumitan yang secara tradisional didukung.

 

## Sejarah Singkat ##

Bahasa tumbuh dari proyek pribadi yang dimulai pada tahun 2006 oleh karyawan Mozilla Graydоn Hоаre, yang menyatakan bahwa proyek itu mungkin dinamai keluarga karat jamur. Mozillа mulai mensponsori proyek ini pada tahun 2009 dan mengumumkannya pada tahun 2010. Rust 1.0, rilis stabil pertama, dirilis pada 15 Mei 2015. Setelah 1.0, rilis titik stabil dikirimkan setiap enam minggu, sementara fitur-fitur yang sangat menyenangkan di malam hari rilis, kemudian diuji dengan rilis beta yang berlangsung enam minggu. Pada 6 April 2021, Google mengumumkan dukungan untuk Karat dalam Sumber Terbuka Аndrоid sebagai Alternatif untuk С/С++.

## Spesifikasi Teknis ##

Karat dimaksudkan untuk menjadi bahasa untuk sistem yang sangat konkrit dan sangat aman, dan pemrograman dalam skala besar, yaitu, menciptakan dan memelihara batasan yang menjaga integritas sistem besar. Hal ini menyebabkan set fitur dengan penekanan pada keamanan, kontrol tata letak memori, dan konkurensi.


Bahasa karat dirancang agar aman untuk memori. Itu tidak mengizinkan pointer nol, pointer menggantung, atau ras data. Nilai data dapat diinisialisasi hanya melalui satu set tetap bentuk, yang semuanya memerlukan input mereka untuk sudah diinisialisasi. Untuk mereplikasi pointer menjadi valid atau NULL, seperti dalam daftar tertaut atau struktur data pohon biner, perpustakaan Rust core menyediakan jenis yang berbeda. Rust telah menambahkan sintaks untuk mengatur masa hidup. Kode yang tidak aman dapat menumbangkan beberapa batasan ini menggunakan kata kunci yang tidak aman.


Bahasa Rust tidak menggunakan pengumpulan sampah otomatis. Memori dan sumber daya lainnya dikelola melalui akuisisi sumber daya adalah penemuan awal, dengan penghitungan referensi opsional.


Karat memberikan manajemen sumber daya yang deterministik, dengan overhead yang sangat rendah. Rust menyukai tumpukan semua nilai dan tidak melakukan tinju implisit. Ada ringkasan referensi (menggunakan simbol), yang tidak melibatkan penghitungan referensi run-time. Keamanan dari pointer tersebut diverifikasi pada waktu tertentu, mencegah pointer yang menggantung dan bentuk lain dari perilaku yang tidak ditentukan.


Karat memiliki sistem kepemilikan dimana semua nilai memiliki pemilik yang unik. Nilai dapat diurutkan dengan referensi yang tidak dapat diubah, menggunakan &T, dengan referensi yang dapat diubah, menggunakan & mematikan T, atau dengan nilai, menggunakan T. Pembuat Rust menerapkan aturan ini pada waktu yang sama dan juga memeriksa bahwa semua referensi valid.


## Contoh Format File RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Referensi ##

* [RS - oleh Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))



