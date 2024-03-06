{
  "date": "2019-10-11",
  "keywords": [
"crt",
"crt fails",
"crt faila formāts",
"crt faila tips",
"failu",
"veids",
"kas ir crt fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT — drošības sertifikāta faila formāts",
  "description": "Uzziniet par CRT faila formātu un API, kas var izveidot un atvērt CRT failus.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir CRT fails?

Fails ar paplašinājumu .crt ir drošības sertifikāta fails, ko izmanto drošas vietnes, lai izveidotu drošus savienojumus no tīmekļa servera ar pārlūkprogrammu. Drošas vietnes ļauj nodrošināt datu pārsūtīšanu, pieteikšanos, maksājumu karšu darījumus un nodrošināt aizsargātu vietnes pārlūkošanu. Ja atverat drošu vietni, adreses joslā tiek parādīta ikona bloķēšana. Noklikšķinot uz tā, varat skatīt detalizētu informāciju par instalēto sertifikātu. Starptautiski uzņēmumi, piemēram, Verisign un Thawte, izplata šos SSL sertifikātus.

## CRT faila formāts

CRT faili ir ASCII formātā, un tos var atvērt jebkurā teksta redaktorā, lai skatītu sertifikāta faila saturu. Tas atbilst X.509 sertifikācijas standartam, kas nosaka sertifikāta struktūru. Tas nosaka datu laukus, kas jāiekļauj SSL sertifikātā. CRT pieder PEM formātam sertifikātiem, kas ir Base64 ASCII kodēti faili.

### PEM faila struktūra

PEM failam var būt vairāki sertifikāti. Šādā gadījumā katram sertifikātam PEM failā ir šāda struktūra.

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

### CRT faila formāta piemērs

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Atsauces Nr.

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

