{
  "date" : "2021-06-30",
  "keywords" :[ "file mst", "format file mst", "apa itu file mst", "file", "contoh mst", "ekstensi file mst", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file MST dan API yang dapat membuat dan membuka file MST.",
  "title" :"MST - File Paket Pemasang Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Apa itu file MST?
File dengan ekstensi .mst digunakan untuk mengubah konten paket MSI. Mereka biasanya digunakan oleh administrator sistem untuk menerapkan pengaturan kustom ke file MSI yang sudah ada. File MST digunakan bersama dengan paket MSI asli dalam sistem distribusi perangkat lunak mereka seperti kebijakan grup. File MST umumnya digunakan dalam pengembangan dan pengujian perangkat lunak untuk mengonfigurasi versi perangkat lunak yang sedang dikembangkan.

## format file MST
File MST atau Transform digunakan untuk mengumpulkan opsi penginstalan untuk program yang menggunakan Penginstal Microsoft Windows dalam file. File-file ini umumnya digunakan pada baris perintah Penginstal (MSIEXEC.EXE), atau digunakan dalam Kebijakan Grup penginstalan perangkat lunak; dalam domain Direktori Aktif Microsoft. File MST juga dapat digunakan dengan penginstal yang dapat dieksekusi yang dibungkus. Kasus umum adalah seseorang ingin meneruskan parameter baris perintah ke penginstal yang dibungkus. Untuk melakukannya, Anda memerlukan file MST yang menambahkan properti WRAPPED_ARGUMENTS ke tabel properti. File-file ini tidak dapat dibuat atau diedit menggunakan editor umum. Alat khusus tersedia untuk tujuan ini.

### Bagaimana cara menggunakan file MST?
File MST dapat dihasilkan dengan menggunakan berbagai alat dan Ocra umumnya digunakan untuk menghasilkan file MST. Kemudian pengaturan dapat disesuaikan sesuai kebutuhan dan menyimpannya di lokasi tertentu. Setelah itu file MST dapat digunakan bersamaan dengan file MSI. Jika Anda ingin menguji file ini; gunakan sintaks berikut pada baris perintah

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMASI properti

Anda juga dapat menggunakan properti **TRANSFORMS** dari penginstal Windows yang sebenarnya adalah daftar transformasi yang diterapkan penginstal saat menginstal paket. Pemasang menjalankan transformasi dalam urutan yang sama seperti yang tercantum dalam properti TRANSFORM. Transformasi dapat ditentukan berdasarkan nama file dengan ekstensi .mst atau path lengkap. Untuk menentukan lebih dari satu transformasi, pisahkan setiap nama file atau titik koma seperti contoh berikut.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referensi

* [File Transformasi MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS property](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


