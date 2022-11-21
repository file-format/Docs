{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Berkas Sertifikat PKCS 7",
  "description":"Pelajari tentang format file P7C dan API yang dapat membuat dan membuka file P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file P7C?

File P7C, seperti file sertifikat keamanan lainnya, adalah sertifikat digital yang digunakan untuk mengautentikasi identitas melalui jaringan. Aplikasi yang menggunakan sertifikat mengautentikasi identitas menggunakan kunci publik yang disertakan dalam file sertifikat ini. Kriptografi kunci publik, atau kriptografi asimetris, menggunakan sepasang kunci yang salah satunya adalah kunci publik dan yang lainnya dikenal sebagai kunci privat. Kunci pribadi disimpan dengan aman untuk keamanan yang efektif, sedangkan kunci publik dapat dibagikan dengan orang lain. Format file sertifikat umum lainnya mencakup [CRT](/id/web/crt/), DER, dan PEM.

## Format File P7C - Informasi Lebih Lanjut

File P7C disimpan ke disk sebagai file biner dan menyertakan informasi kunci publik yang dihasilkan menggunakan algoritme kriptografi berdasarkan masalah matematika. Ini dapat dibuka di editor teks apa pun tetapi kontennya tidak dalam bentuk yang dapat dibaca manusia. Beberapa aplikasi yang dapat membuka file P7C antara lain Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager, dan Microsoft Windows Contacts.

### Contoh Format File P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referensi ##

* [Kriptografi Kunci Publik](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Bagaimana cara membuat file P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

