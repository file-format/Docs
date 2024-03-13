{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7B - PKCS 7 Sertifikat Faylı",
  "description": "P7C faylları yarada və aça bilən P7C fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-azb"
}
},
  "lastmod": "2019-09-10"
}

## P7B faylı nədir?

P7B faylı şəxsin və ya cihazın autentifikasiyası üçün təhlükəsiz rəqəmsal sertifikatı ehtiva edən təhlükəsizlik sertifikatı faylıdır. [.cer](/web/cer/) sertifikat faylına bənzər, P7B faylı faylda sağ klik seçimindən istifadə etməklə Sertifikatı quraşdır seçimindən istifadə etməklə quraşdırıla bilər. P7B CER fayl formatından fərqli formatlaşdırma seçimindən istifadə edir. O, base64 (ASCII) kodlamasından istifadə edən bir və ya daha çox X.509 rəqəmsal sertifikat faylını ehtiva edir. P7B faylları [ZIP](/compression/zip/) faylı kimi qəbul edilir və ya Sertifikat Təşkilatından alınır.

## P7B fayl formatı

P7B faylları istənilən mətn redaktorunda açıla bilən sadə ASCII faylları kimi saxlanılır. O, oxunaqlılıq baxımından mənasız olan kodlanmış sətir olan açıq açarı ehtiva edir.

### P7B Fayl Formatına Nümunə

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## İstinadlar ##

* [İctimai Açar Kriptoqrafiyası](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [P7C faylı Necə Yaradılır?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


