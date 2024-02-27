{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7B - PKCS 7 certifikatfil",
  "description": "Lær om P7C-filformater og API'er, der kan oprette og åbne P7C-filer.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-dab"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en P7B fil?

En P7B-fil er en sikkerhedscertifikatfil, der indeholder et sikkert digitalt certifikat til godkendelse af en person eller en enhed. I lighed med en [.cer](/web/cer/)-certifikatfil kan en P7B-fil installeres ved at bruge Installer certifikat-indstillingen ved at bruge højreklik-muligheden på filen. P7B bruger en anden formateringsmulighed end CER-filformatet. Den indeholder en eller flere X.509 digitale certifikatfiler, der bruger base64 (ASCII)-kodning. P7B-filer modtages som en [ZIP](/compression/zip/)-fil eller modtages fra certifikatmyndigheden.

## P7B filformat

P7B-filer gemmes som almindelige ASCII-filer, der kan åbnes i enhver teksteditor. Den indeholder den offentlige nøgle, der er en kodet streng, som er meningsløs fra et læsbarhedssynspunkt.

### Eksempel på P7B filformat

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencer ##

* [Public-key_cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Hvordan opretter man P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


