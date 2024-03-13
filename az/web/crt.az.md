{
  "date": "2019-10-11",
  "keywords": [
"crt",
"crt faylı",
"crt fayl formatı",
"crt fayl növü",
"fayl",
"növü",
"crt faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT - Təhlükəsizlik Sertifikatı Fayl Formatı",
  "description": "CRT faylları yarada və aça bilən CRT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-azt"
}
},
  "lastmod": "2019-09-10"
}

## CRT faylı nədir?

.crt uzantılı fayl, veb serverdən brauzerə təhlükəsiz bağlantılar yaratmaq üçün təhlükəsiz veb-saytlar tərəfindən istifadə edilən təhlükəsizlik sertifikatı faylıdır. Təhlükəsiz veb-saytlar məlumat ötürülməsi, giriş, ödəniş kartı əməliyyatlarının təhlükəsizliyini təmin edir və sayta qorunan baxışı təmin edir. Təhlükəsiz veb saytı açsanız, ünvan çubuğunda kilid işarəsini görürsünüz. Bunun üzərinə klikləsəniz, quraşdırılmış sertifikatın təfərrüatlarına baxa bilərsiniz. Verisign və Thawte kimi beynəlxalq şirkətlər bu SSL sertifikatlarını yayırlar.

## CRT fayl formatı

CRT faylları ASCII formatındadır və sertifikat faylının məzmununa baxmaq üçün istənilən mətn redaktorunda açıla bilər. O, sertifikatın strukturunu müəyyən edən X.509 sertifikatlaşdırma standartına uyğundur. SSL sertifikatına daxil edilməli olan məlumat sahələrini müəyyənləşdirir. CRT, Base64 ASCII kodlu faylları olan sertifikatların PEM formatına aiddir.

### PEM Fayl Strukturu

PEM faylının bir neçə sertifikatı ola bilər. Belə olan halda, PEM faylındakı hər bir sertifikat aşağıdakı strukturu izləyir.

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

### CRT fayl formatı nümunəsi

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## İstinadlar ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

