{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Berkas Sertifikat PKCS 7",
  "description":"Pelajari tentang format file P7C dan API yang dapat membuat dan membuka file P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file P7B?

File P7B adalah file sertifikat keamanan yang berisi sertifikat digital aman untuk mengautentikasi seseorang atau perangkat. Mirip dengan file sertifikat [.cer](/id/web/cer/), file P7B dapat diinstal menggunakan opsi "Instal Sertifikat" dengan menggunakan opsi klik kanan pada file. P7B menggunakan opsi pemformatan yang berbeda dari format file CER. Ini berisi satu atau lebih file sertifikat digital X.509 yang menggunakan pengkodean base64 (ASCII). File P7B diterima sebagai file [ZIP](/id/compression/zip/) atau diterima dari Otoritas Sertifikat.

## Format File P7B

File P7B disimpan sebagai file ASCII biasa yang dapat dibuka di editor teks apa pun. Ini berisi kunci publik yang merupakan string yang disandikan yang tidak berarti dari sudut pandang keterbacaan.

### Contoh Format File P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referensi ##

* [Kriptografi Kunci Publik](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Bagaimana cara membuat file P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

