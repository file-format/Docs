{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AIDL - File Bahasa Definisi Antarmuka Android",
  "description":"Pelajari tentang apa itu format file AIDL dengan contoh dan API yang dapat membuat dan membuka file AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Apa itu file AIDL?

File AIDL (Android Interface Definition Language) memungkinkan pengembang Android menjalin komunikasi antara berbagai aplikasi. Berdasarkan antarmuka pemrograman, klien dan layanan setuju untuk berkomunikasi menggunakan komunikasi antarproses (IPC). File AIDL berisi kode sumber [Java](/id/programming/java/) untuk menentukan antarmuka ini dan kontrak untuk komunikasi antar aplikasi.

Anda dapat membuka file AIDL dengan Google Android Studio atau editor teks seperti Microsoft Notepad dan Notepad++.

## Format File AIDL - Informasi Lebih Lanjut

AIDL adalah file teks yang berisi antarmuka untuk komunikasi antar aplikasi. OS Android tidak mengizinkan satu proses untuk mengakses memori proses lain. Ini mengarahkan proses untuk membagi objek mereka menjadi primitif untuk memahami sistem operasi yang mendasarinya dan membangun proses struktur komunikasi untuk pengembang.

### Jenis Data apa yang didukung oleh AIDL?

AIDL mendukung tipe data berikut secara default.

* Semua tipe primitif dalam bahasa pemrograman Java (seperti int, long, char, boolean, dan sebagainya)
* Rangkaian
* CharSequence
* Daftar
* Peta

## Contoh File AIDL

Berikut adalah contoh file AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Referensi

* [Bahasa Definisi Antarmuka Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

