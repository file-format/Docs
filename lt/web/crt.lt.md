{
  "date": "2019-10-11",
  "keywords": [
"crt",
"crt failą",
"crt failo formatas",
"crt failo tipas",
"failą",
"tipo",
"kas yra crt failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT – saugos sertifikato failo formatas",
  "description": "Sužinokite apie CRT failo formatą ir API, kurios gali kurti ir atidaryti CRT failus.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra CRT failas?

Failas su plėtiniu .crt yra saugos sertifikato failas, naudojamas saugiose svetainėse, kad užmegztų saugų ryšį tarp žiniatinklio serverio ir naršyklės. Saugios svetainės suteikia galimybę apsaugoti duomenų perdavimą, prisijungimus, mokėjimo kortelių operacijas ir užtikrinti saugų naršymą svetainėje. Jei atidarote saugią svetainę, adreso juostoje pamatysite užrakto piktogramą. Jei spustelėsite jį, galėsite peržiūrėti išsamią įdiegto sertifikato informaciją. Tarptautinės kompanijos, tokios kaip Verisign ir Thawte, platina šiuos SSL sertifikatus.

## CRT failo formatas

CRT failai yra ASCII formato ir gali būti atidaryti bet kuriame teksto rengyklėje, kad būtų galima peržiūrėti sertifikato failo turinį. Jis atitinka X.509 sertifikavimo standartą, kuris apibrėžia sertifikato struktūrą. Jis apibrėžia duomenų laukus, kurie turi būti įtraukti į SSL sertifikatą. CRT priklauso PEM formatui sertifikatams, kurie yra Base64 ASCII koduoti failai.

### PEM failo struktūra

PEM failas gali turėti kelis sertifikatus. Tokiu atveju kiekvienas PEM failo sertifikatas turi tokią struktūrą.

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

### CRT failo formato pavyzdys

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Nuorodos Nr.

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

