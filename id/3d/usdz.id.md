{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "file usdz", "format file usdz", "format file", "3d", "unduhan file usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Format ZIP Uraian Adegan Universal",
  "description":"Pelajari tentang format file USDZ dan API yang dapat membuka dan membuat file USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Apa itu file USDZ?

File dengan .usdz adalah arsip ZIP yang tidak terkompresi dan tidak terenkripsi untuk format file [USD](/id/3d/usd/) (Universal Scene Description) yang berisi dan proksi untuk file dengan format lain (seperti tekstur, dan animasi) yang disematkan di dalamnya arsip dan menjalankannya langsung dengan run-time USD tanpa perlu membongkar. File USDZ adalah paket yang desainnya didasarkan pada abstraksi level-Ar baru dari sebuah paket. Usdz terdaftar di IANA dan memiliki nama jenis media model dan nama subtipe vnd.usd+zip dan detailnya dapat ditemukan di [halaman pendaftaran IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Format File USDZ

File USDZ didasarkan pada format file ZIP yang mengarsipkan file individual dalam wadahnya. Hal ini memungkinkan ujung penerima untuk hanya mengekstrak konten dan menggunakan file deskripsi adegan USD normal untuk bekerja dengan dan memeriksa. Hampir semua sistem operasi menyediakan dukungan bawaan untuk format file ZIP dan memilih format pengarsipan ini daripada metode khusus apa pun memudahkan file USDZ berguna sebagai protokol transportasi sederhana.

### Kendala ZIP

Format file USDZ menggunakan format file ZIP tanpa `kompresi` dan `enkripsi`. Ini ditujukan oleh desain untuk memenuhi dua persyaratan:

* Untuk paket yang sudah dimuat ke dalam memori atau sebagai file tunggal di disk, API tersedia dalam USD untuk mengakses data yang terdapat di dalam image
* Seharusnya tidak perlu mengekstrak file ke disk atau mengalokasikan lebih banyak penyimpanan heap

Dengan USDZ, kedua persyaratan ini terpenuhi karena sebagian besar format gambar itu sendiri memungkinkan skema kompresi internal, menghasilkan ukuran file yang ringkas.

### Persyaratan Tata Letak

Paket USDZ memerlukan tata letak file di dalam paket adalah bahwa data untuk setiap file harus dimulai dengan kelipatan 64 byte dari awal paket. Namun, paket harus dimulai dengan file [USD](/id/3d/usd/) asli jika menargetkan paket dengan referensi sederhana. Dalam kasus seperti itu, file USD pertama ini disebut sebagai Lapisan Default. Klien yang ingin mengirimkan "konten yang dapat dialirkan" mungkin juga ingin mempertimbangkan batasan tata letak lainnya.

## unduhan file USDZ
Karena file usdz dikemas dengan file gambar dan usd berkualitas tinggi lainnya, mereka dapat menempati penyimpanan disk yang lebih besar. Di sini Anda dapat menemukan file contoh USDZ sederhana dan lebih kecil untuk diunduh:

- [Sampel.usdz](../sample.usdz)

## Referensi

* [Spesifikasi Format File USDZ](https://openusd.org/release/spec_usdz.html)
