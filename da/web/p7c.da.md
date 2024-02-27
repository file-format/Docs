{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7C - PKCS 7 certifikatfil",
  "description": "Lær om P7C-filformater og API'er, der kan oprette og åbne P7C-filer.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-dac"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en P7C fil?

En P7C-fil er ligesom andre sikkerhedscertifikatfiler et digitalt certifikat, der bruges til at autentificere identitet over netværket. Programmer, der bruger certifikater, godkender identitet ved hjælp af den offentlige nøgle, der er inkluderet i disse certifikatfiler. Offentlig nøglekryptering, eller asymmetrisk kryptografi, bruger et par nøgler, hvoraf den ene er den offentlige nøgle, og den anden er kendt som privat nøgle. Den private nøgle holdes sikker for effektiv sikkerhed, mens den offentlige nøgle kan deles med andre. Andre almindelige certifikatfilformater omfatter [CRT](/web/crt/), DER og PEM.

## P7C filformat - flere oplysninger

P7C-filer gemmes på disken som binære filer og inkluderer den offentlige nøgleinformation, der er genereret ved hjælp af kryptografiske algoritmer baseret på matematiske problemer. Disse kan åbnes i enhver teksteditor, men deres indhold er ikke i menneskelig læsbar form. Nogle af de programmer, der kan åbne P7C-filer, inkluderer Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager og Microsoft Windows Contacts.

### Eksempel på P7C-filformat

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencer ##

* [Public-key_cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Hvordan opretter man P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


