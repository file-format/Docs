{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class", "apa itu file kelas", "cara membuka file kelas", "ekstensi", "file", "file kelas", "format file kelas", "ekstensi .class ", "file kelas dalam java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Kelas - Format File Kelas Java",
  "description":"Pelajari tentang format file Kelas dan API yang dapat membuat dan membuka file Kelas.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file Kelas?

File **Class di Java** adalah hasil kompilasi dari class [.java](/id/programming/java/) yang sebenarnya dijalankan oleh Java Virtual Machine (JVM). File kelas dapat dieksekusi secara individual dan juga dapat menjadi bagian dari file [JAR](/id/programming/jar/) sebagai bundel bersama dengan file paket lainnya. Ini dapat dibuat menggunakan perintah **`javac`** dari antarmuka baris perintah. Beberapa Java IDE seperti [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/Eclipse-ide-java-developers) dan NetBeans menyediakan file keluaran .class dari proyek Java file.

## Format File Kelas

File kelas Java terdiri dari bytecode yang merupakan kode perantara untuk dijalankan oleh JVM. File kelas terdiri dari aliran byte 8-bit dan item data multibyte selalu disimpan dalam urutan big-endian.

### Struktur Berkas Kelas

Struktur file kelas adalah seperti yang ditunjukkan di bawah ini.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
di mana:

* u1 = jumlah satu byte yang tidak ditandatangani
* u2 = jumlah dua byte yang tidak ditandatangani
* u4 = jumlah empat byte yang tidak ditandatangani

Detail struktur file .class juga dijelaskan dalam [format file kelas] Oracle (https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) dan dapat dirujuk oleh pengembang untuk referensi. Ringkasan bidang-bidang ini adalah sebagai berikut.

* `magic` - Item ajaib memasok nomor ajaib yang mengidentifikasi format file kelas; itu memiliki nilai 0xCAFEBABE.
* `minor_version`, `major_version` - Nilai item versi_minor dan versi_mayor adalah nomor versi minor dan mayor dari file kelas ini.
* `constant_pool_count` - Nilai dari item constant_pool_count sama dengan jumlah entri dalam tabel constant_pool ditambah satu. Indeks constant_pool dianggap valid jika lebih besar dari nol dan lebih kecil dari constant_pool_count, dengan pengecualian untuk konstanta bertipe long dan double.
* `constant_pool[]` - Constant_pool adalah tabel struktur (§4.4) yang mewakili berbagai konstanta string, nama kelas dan antarmuka, nama bidang, dan konstanta lain yang dirujuk dalam struktur ClassFile dan substrukturnya. Format setiap entri tabel constant_pool ditunjukkan oleh byte "tag" pertamanya.
* `access_flags` - Nilai item access_flags adalah mask dari flag yang digunakan untuk menunjukkan izin akses dan properti kelas atau antarmuka ini.
* `this_class` - Nilai dari item this_class harus berupa indeks yang valid ke dalam tabel constant_pool.
* `super_class` - Untuk kelas, nilai item super_class harus nol atau harus berupa indeks yang valid ke dalam tabel constant_pool.
* `interfaces_count` - Nilai item interfaces_count memberikan jumlah antarmuka super langsung dari kelas atau tipe antarmuka ini.
* `interfaces[]` - Setiap nilai dalam array interfaces harus berupa indeks yang valid ke dalam tabel constant_pool.
* `fields_count` - Nilai dari item field_count memberikan jumlah struktur field_info dalam tabel field.
* `fields[]` - Setiap nilai dalam tabel field harus berupa struktur field_info yang memberikan deskripsi lengkap tentang field di kelas atau antarmuka ini.
* `methods_count` - Nilai dari item methods_count memberikan jumlah struktur info_metode dalam tabel metode.
* `methods[]` - Setiap nilai dalam tabel metode harus berupa struktur info_metode yang memberikan deskripsi lengkap tentang metode di kelas atau antarmuka ini. Jika tak satu pun dari flag ACC_NATIVE dan ACC_ABSTRACT diatur dalam item access_flags dari struktur method_info, instruksi Java Virtual Machine yang mengimplementasikan metode juga disediakan.
* `attributes_count` - Nilai item attribute_count memberikan jumlah atribut (§4,7) dalam tabel atribut kelas ini.
* `attributes[]` - Setiap nilai tabel atribut harus berupa struktur attribute_info.




## Referensi

* [Format File kelas](https://docs.Oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

