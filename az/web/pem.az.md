{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEM Faylı - Məxfilik Təkmilləşdirilmiş Poçt Sertifikatı Fayl Formatıdır",
  "description": "PEM fayl formatı və PEM faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-azm"
}
},
  "lastmod": "2022-09-14"
}

## PEM faylı nədir?

PEM faylı veb server və brauzer arasında təhlükəsiz rabitə kanalı yaratmaq üçün istifadə edilən təhlükəsizlik sertifikatı faylıdır. O, Base64 kodludur və şəxsi açar, server sertifikatı və/yaxud digər sertifikatların birləşməsindən ibarət ola bilər. PEM faylları istifadə baxımından .der sertifikat fayllarına bənzəyir, lakin ikili məlumat deyil, Base64 kodlu mətn kimi saxlanılır. Digər oxşar sertifikat fayl formatlarına [.cer](/web/cer/) və [.crt](/web/crt/) faylları daxildir.

**PEM fayllarını** aça bilən proqramlara Microsoft Notepad və Apple TextEdit kimi mətn redaktorları daxildir.

## PEM fayl formatı

PEM məlumatların saxlanması üçün istifadə olunan faylın strukturunu və kodlaşdırma növünü təyin edən konteyner fayl formatıdır. PEM faylları diskdə insan tərəfindən oxuna bilməyən Base64 kodlu fayl formatı kimi saxlanılır. Standart PEM faylının aşağıdakılarla başladığını müəyyən edir:

```
-----BEGIN <type>-----
```
və bununla bitir:
```
-----END <type>-----
```

Bunların içərisindəki bütün digər məzmunlar base64 kodludur (böyük və kiçik hərflər, rəqəmlər, + və /). Tək bir PEM faylı digər proqramlar tərəfindən istifadə oluna bilən bir neçə blokdan ibarət ola bilər. PEM faylında bir neçə sertifikat varsa, hər bir sertifikat aşağıdakı kimi fərdi bloklarla ayrılır:

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

### PEM fayl nümunəsi

SERTİFİKAT bloklu PEM faylı adətən aşağıdakı kimi görünür:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

RSA ilə PEM faylı aşağıdakı kimi başlayır.

```
-----BEGIN RSA PRIVATE KEY-----
```

## İstinadlar ##

* [İctimai Açar Kriptoqrafiyası](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [P7C faylı Necə Yaradılır?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


