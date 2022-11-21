{
  "date" : "2020-01-11",
  "keywords" :[ "file x", "format file x", "apa itu file x", "file", "contoh x", "ekstensi file x", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Format File DirectX 2.0",
  "description":"Pelajari tentang format file DirectX X dan API yang dapat membuka dan membuat file DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Apa itu file X?

File dengan ekstensi .x mengacu pada [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) format file warisan Grafik 3D yang diperkenalkan dengan Microsoft DirectX 2.0. Itu digunakan untuk rendering grafik 3D dalam game dan menentukan struktur untuk jerat, tekstur, animasi, dan objek yang ditentukan pengguna. Sudah ditinggalkan sejak 2014 karena format file Autodesk FBX berfungsi lebih baik sebagai format yang lebih modern. X digerakkan oleh template dan bebas dari pengetahuan penggunaan apa pun.

Anda dapat membuka file DirectX X menggunakan Microsoft DirectX dan editor teks biasa.

## Format File X

[Referensi file X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) berisi informasi referensi untuk elemen API yang digunakan untuk bekerja dengan file DirectX .x. Format ini menyediakan primitif data tingkat rendah yang digunakan oleh aplikasi lain untuk menentukan primitif tingkat lebih tinggi melalui templat data. DirectX 6.0 memperkenalkan antarmuka dan metode yang memungkinkan membaca dari dan menulis ke file .x. DirectX 3.0 memperkenalkan versi biner dari format file ini.

[Referensi format file X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) yang ditentukan oleh DirectX 9 berisi informasi referensi untuk .x file dalam Pengodean Biner dan Teks.

### Pengodean Biner

[format biner](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) mendefinisikan format DirectX X sebagai representasi token dari format teks. Token ini dapat berdiri sendiri untuk memberikan struktur tata bahasa atau dapat menjadi token pembawa catatan yang memasok data yang diperlukan.

#### Judul

Header biner dapat dibaca dan ditulis menggunakan definisi berikut.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Pengodean Teks

File DirectX .x tidak bergantung pada cara file digunakan dan tidak spesifik untuk aplikasi apa pun. Pendekatan berbasis template ini memungkinkan format file .x digunakan oleh aplikasi klien apa pun.


#### Judul

Header dengan panjang variabel adalah wajib dan harus berada di awal aliran data. Header berisi data berikut.

|Jenis |Sub Jenis |Ukuran |Isi |Arti Konten|
---|---|---|---|---|
|Angka Ajaib (wajib)| | 4 byte |xof |
|Nomor Versi (wajib) |Nomor Utama |2 byte |03 |Versi utama 3|
| |Bilangan Kecil |2 byte |02 |Versi kecil 2|
|Jenis Format (wajib)| |4 byte |"txt " |Berkas Teks|
| | | |"bin"| Berkas Biner|
| | | |"tzip"| File Teks Terkompresi MSZip|
| | | |"bzip"| Berkas Biner Terkompresi MSZip|
|Ukuran float (wajib)| |4 byte| 0064| pelampung 64-bit|
| | | |0032 |32-bit float|


## Referensi

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Referensi Format File DirectX 9](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

