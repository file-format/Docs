{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7C - PKCS 7 Sertifikat Faylı",
  "description": "P7C faylları yarada və aça bilən P7C fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-azc"
}
},
  "lastmod": "2019-09-10"
}

## P7C faylı nədir?

P7C faylı, digər təhlükəsizlik sertifikatı faylları kimi, şəbəkə üzərindən şəxsiyyəti təsdiqləmək üçün istifadə olunan rəqəmsal sertifikatdır. Sertifikatlardan istifadə edən proqramlar bu sertifikat fayllarına daxil olan açıq açardan istifadə edərək şəxsiyyəti təsdiqləyir. Açıq açar kriptoqrafiyası və ya asimmetrik kriptoqrafiya, biri açıq açar, digəri isə özəl açar kimi tanınan cüt açarlardan istifadə edir. Şəxsi açar effektiv təhlükəsizlik üçün təhlükəsiz saxlanılır, açıq açar isə başqaları ilə paylaşıla bilər. Digər ümumi sertifikat fayl formatlarına [CRT](/web/crt/), DER və PEM daxildir.

## P7C Fayl Format - Ətraflı Məlumat

P7C faylları ikili fayllar kimi diskdə saxlanılır və riyazi problemlərə əsaslanan kriptoqrafik alqoritmlərdən istifadə etməklə yaradılan açıq açar məlumatlarını ehtiva edir. Bunlar istənilən mətn redaktorunda açıla bilər, lakin onların məzmunu insanların oxuna biləcəyi formada deyil. P7C fayllarını aça bilən bəzi proqramlara Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager və Microsoft Windows Contacts daxildir.

### P7C Fayl Formatına Nümunə

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## İstinadlar ##

* [İctimai Açar Kriptoqrafiyası](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [P7C faylı Necə Yaradılır?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


