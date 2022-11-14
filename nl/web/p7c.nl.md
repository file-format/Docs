{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7-certificaatbestand",
  "description":"Meer informatie over P7C-bestandsindeling en API's die P7C-bestanden kunnen maken en openen.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een P7C-bestand?

Een P7C-bestand is, net als andere beveiligingscertificaatbestanden, een digitaal certificaat dat wordt gebruikt om de identiteit via het netwerk te verifiëren. Toepassingen die certificaten gebruiken, verifiëren de identiteit met behulp van de openbare sleutel die in deze certificaatbestanden is opgenomen. Public-key cryptografie, of asymmetrische cryptografie, maakt gebruik van een paar sleutels waarvan de ene de openbare sleutel is en de andere bekend staat als de privésleutel. De privésleutel wordt veilig bewaard voor effectieve beveiliging, terwijl de openbare sleutel met anderen kan worden gedeeld. Andere veelgebruikte bestandsindelingen voor certificaten zijn onder meer [CRT](/nl/web/crt/), DER en PEM.

## P7C-bestandsindeling - Meer informatie

P7C-bestanden worden op schijf opgeslagen als binaire bestanden en bevatten de openbare sleutelinformatie die is gegenereerd met behulp van cryptografische algoritmen op basis van wiskundige problemen. Deze kunnen in elke teksteditor worden geopend, maar hun inhoud is niet in voor mensen leesbare vorm. Enkele van de toepassingen die P7C-bestanden kunnen openen, zijn Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager en Microsoft Windows Contacts.

### Voorbeeld van P7C-bestandsindeling

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenties ##

* [cryptografie met openbare sleutel](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hoe maak je een P7C-bestand aan?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

