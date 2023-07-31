{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ Script Sumber Daya Terkompilasi",
  "description":"Pelajari tentang format file RES dengan contoh RES dan API yang dapat membuat dan membuka file RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file RES?
File dengan akhiran atau ekstensi .res dapat termasuk dalam banyak kategori format file. Disini kita membahas format file RES yang merupakan C++ Compiled Resource Script; file biner yang dibuat oleh Microsoft Resource Compiler (rc) yang berisi data sumber daya; berdasarkan konten file resource-definition; relevan dengan proyek perangkat lunak induknya. File .res biasanya diformat ulang menjadi file objek sumber daya untuk menautkannya ke file aplikasi yang dapat dieksekusi.

## format file.RES
Format file RES milik Microsoft Resource Compiler (rc). Kompiler sumber daya adalah alat yang mengompilasi sumber daya seperti kursor, ikon, menu, dan kotak dialog, yang digunakan aplikasi Anda. File sumber daya biasanya memiliki ekstensi .res; berisi sumber daya, seperti kursor, gambar, dan informasi versi. File RES bisa berupa file sumber daya 16 atau 32-bit.
## Struktur file sumber daya
File sumber daya berisi serangkaian berbagai entri sumber daya. Setiap entri berisi header sumber daya dan data yang relevan. Header sumber daya biasanya selaras dengan DWORD dalam file dan berisi yang berikut ini:

- **DWORD** untuk menentukan ukuran header sumber daya
- **DWORD** untuk menentukan ukuran data sumber daya
- Jenis sumber daya
- Nama sumber daya
- Informasi sumber daya tambahan

Struktur header sumber daya menentukan format file RES. Data untuk sumber daya mengikuti header sumber daya. Beberapa sumber daya juga menambahkan pola tajuk grup khusus sumber daya untuk memberikan informasi tentang sekelompok sumber daya. Berikut adalah beberapa jenis entri sumber daya dan deskripsinya:

### Sumber Daya Tabel Akselerator
Tabel akselerator adalah entri sumber daya dalam file RES tanpa header grup. Pola **ACCELTABLEENTRY** menentukan setiap entri dalam tabel akselerator. File RES mungkin memiliki beberapa tabel akselerator.

### Kursor dan Sumber Daya Ikon
Meskipun, sistem menganggap setiap ikon dan kursor sebagai satu file, tetapi ini disimpan dalam file RES sebagai grup sumber daya ikon atau grup sumber daya kursor. Format file sumber ikon dan kursor sama. Header grup sumber daya mengikuti semua ikon individual atau komponen grup kursor di file .res.

### Sumber Daya Kotak Dialog
Kotak dialog juga direalisasikan sebagai entri sumber daya dalam file RES. Ini berisi satu pola header kotak dialog **DLGTEMPLATE** dan satu pola **DLGITEMTEMPLATE** untuk setiap kontrol tertentu di kotak dialog. Pola **DLGTEMPLATEEX** dan **DLGITEMTEMPLATEEX** menjelaskan format sumber daya kotak dialog yang diperluas.

### Sumber Daya Font
Sumber daya menu berisi pola **MENUHEADER** setelah satu atau beberapa pola **NORMALMENUITEM** atau **POPUPMENUITEM**, satu untuk setiap item menu di template menu. Pola **MENUEX_TEMPLATE_HEADER** dan **MENUEX_TEMPLATE_ITEM** menjelaskan format sumber daya menu yang diperluas.

### Sumber Daya Tabel Pesan
Tabel pesan terdiri dari teks yang diformat untuk ditampilkan sebagai pesan kesalahan atau dalam kotak pesan. Pola utama dalam resource tabel pesan adalah struktur **MESSAGE_RESOURCE_DATA**.

### Sumber Daya Versi
Pola utama dalam sumber daya versi adalah **VS_FIXEDFILEINFO**. Pola tambahan mencakup **VarFileInfo** untuk menyimpan data terkait informasi bahasa, dan **StringFileInfo** untuk informasi string khusus.




## Referensi

* [Format File Sumber Daya](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



