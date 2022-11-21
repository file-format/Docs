{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file KEY dan API yang dapat membuat dan membuka file KEY.",
  "title" :"Format File KUNCI - File Kunci Pribadi Mail yang Disempurnakan Privasi",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Apa itu file KUNCI?

File KEY adalah bagian pribadi dari mekanisme keamanan yang disimpan ke disk dalam format file Privacy-Enhanced Mal (PEM). Ini digunakan untuk mendekripsi informasi yang dipertukarkan antara browser web dan server web yang melayani permintaan penelusuran. File KEY berisi string yang disandikan yang tidak berguna untuk mata manusia tetapi merupakan inti dari pertukaran informasi enkripsi/dekripsi sebagai bagian dari sertifikat SSL di server web. File KEY dibuat secara otomatis dan dipasang di ujung klien.

Anda dapat membuka file **KEY** dengan editor teks apa pun seperti Microsoft Notepad (Windows), Apple TextEdit (Mac), atau GitHub Atom (lintas platform). File KEY mirip dengan format file [CRT](/id/web/crt/) dan [CER](/id/web/cer/).

## Format File KUNCI - Informasi Lebih Lanjut

File KEY disimpan ke disk sebagai file teks biasa tetapi merupakan string yang disandikan yang tidak mudah dibaca oleh manusia. Praktisnya, pengguna tidak memiliki pemahaman tentang string saat dibuka di editor teks. Sertifikat kunci privat bersifat rahasia dan tidak boleh dibagikan dengan siapa pun. Proses lengkap mengamankan pertukaran informasi melalui internet melibatkan:

* **Kunci Publik** - digunakan untuk mengenkripsi informasi pengguna untuk pertukaran data antara browser dan server web
* **Kunci Pribadi** - digunakan untuk mendekripsi informasi saat diterima oleh server web

Sertifikat SSL, juga dikenal sebagai sertifikat X.509, bersifat unik untuk setiap situs web. File KEY menggunakan sintaks berikut:

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

### Contoh Berkas KUNCI

Berikut adalah contoh file Kunci pribadi.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referensi

* [Kunci Publik, Kunci Pribadi, dan Sertifikat](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

