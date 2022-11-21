{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt file", "crt file format", "crt file type", "file", "type", "apa itu file crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Format File Sertifikat Keamanan",
  "description":"Pelajari tentang format file CRT dan API yang dapat membuat dan membuka file CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file CRT?

File dengan ekstensi .crt adalah file sertifikat keamanan yang digunakan oleh situs web aman untuk membangun koneksi aman dari server web ke browser. Situs web yang aman memungkinkan untuk mengamankan transfer data, login, transaksi kartu pembayaran, dan menyediakan penjelajahan yang dilindungi ke situs. Jika Anda membuka situs web yang aman, Anda akan melihat ikon "kunci" di bilah alamat. Jika Anda mengkliknya, Anda dapat melihat detail sertifikat yang diinstal. Perusahaan internasional seperti Verisign dan Thawte mendistribusikan sertifikat SSL ini.

## Format File CRT

File CRT dalam format ASCII dan dapat dibuka di editor teks apa pun untuk melihat konten file sertifikat. Ini mengikuti standar sertifikasi X.509 yang mendefinisikan struktur sertifikat. Ini menentukan bidang data yang harus disertakan dalam sertifikat SSL. CRT termasuk dalam format sertifikat PEM yang merupakan file yang disandikan Base64 ASCII.

### Struktur File PEM

File PEM dapat memiliki beberapa sertifikat. Dalam kasus seperti itu, setiap sertifikat dalam file PEM mengikuti struktur berikut.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Contoh Format File CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referensi ##

* [Kunci Publik, Kunci Pribadi, dan Sertifikat](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

