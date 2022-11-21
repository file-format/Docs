{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File PEM - Format File Sertifikat Surat yang Ditingkatkan Privasi",
  "description":"Pelajari tentang format file PEM dan API yang dapat membuat dan membuka file PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Apa itu file PEM?

File PEM adalah file sertifikat keamanan yang digunakan untuk membuat saluran komunikasi yang aman antara server web dan browser. Ini dikodekan Base64 dan mungkin berisi kunci pribadi, sertifikat server, dan/atau kombinasi dari sertifikat lainnya. File PEM mirip dengan file sertifikat .der dalam hal penggunaan tetapi disimpan sebagai teks yang disandikan Base64 daripada data biner. Format file sertifikat serupa lainnya termasuk file [.cer](/id/web/cer/) dan [.crt](/id/web/crt/).

Aplikasi yang dapat **membuka file PEM** meliputi editor teks seperti Microsoft Notepad dan Apple TextEdit.

## Format File PEM

PEM adalah format file wadah yang menentukan struktur dan jenis pengkodean file yang digunakan untuk menyimpan data. File PEM disimpan ke disk sebagai format file berenkode Base64 yang tidak dapat dibaca manusia. Standar mendefinisikan bahwa file PEM dimulai dengan:

```
-----BEGIN <type>-----
```
dan diakhiri dengan:
```
-----END <type>-----
```

Semua konten lain di dalamnya disandikan base64 (huruf besar dan kecil, angka, +, dan /). File PEM tunggal dapat terdiri dari beberapa blok yang dapat digunakan oleh program lain. Jika file PEM berisi banyak sertifikat, setiap sertifikat dipisahkan oleh masing-masing blok sebagai berikut:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Contoh File PEM

File PEM dengan blok SERTIFIKAT biasanya terlihat seperti berikut:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

File PEM dengan RSA dimulai seperti berikut.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referensi ##

* [Kriptografi Kunci Publik](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Bagaimana cara membuat file P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

