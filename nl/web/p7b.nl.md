{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7-certificaatbestand",
  "description":"Meer informatie over P7C-bestandsindeling en API's die P7C-bestanden kunnen maken en openen.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een P7B-bestand?

Een P7B-bestand is een beveiligingscertificaatbestand dat een beveiligd digitaal certificaat bevat voor de authenticatie van een persoon of een apparaat. Net als bij een [.cer](/nl/web/cer/) certificaatbestand, kan een P7B-bestand worden geïnstalleerd met behulp van de optie "Certificaat installeren" door met de rechtermuisknop op het bestand te klikken. P7B gebruikt een andere opmaakoptie dan het CER-bestandsformaat. Het bevat een of meer X.509 digitale certificaatbestanden die gebruik maken van base64 (ASCII)-codering. P7B-bestanden worden ontvangen als een [ZIP](/nl/compression/zip/)-bestand of ontvangen van de certificeringsinstantie.

## P7B-bestandsindeling

P7B-bestanden worden opgeslagen als gewone ASCII-bestanden die in elke teksteditor kunnen worden geopend. Het bevat de openbare sleutel die een gecodeerde reeks is die zinloos is vanuit het oogpunt van leesbaarheid.

### Voorbeeld van P7B-bestandsindeling

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenties ##

* [cryptografie met openbare sleutel](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hoe maak je een P7C-bestand aan?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

