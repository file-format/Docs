{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt-bestand", "crt-bestandsformaat", "crt-bestandstype", "bestand", "type", "wat is een crt-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - bestandsindeling beveiligingscertificaat",
  "description":"Meer informatie over CRT-bestandsindeling en API's die CRT-bestanden kunnen maken en openen.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een CRT-bestand?

Een bestand met de extensie .crt is een beveiligingscertificaatbestand dat door beveiligde websites wordt gebruikt voor het tot stand brengen van beveiligde verbindingen van de webserver naar een browser. Beveiligde websites maken het mogelijk om gegevensoverdrachten, logins, betaalkaarttransacties te beveiligen en bieden beschermd browsen naar de site. Als u een beveiligde website opent, ziet u een "slot"-pictogram in de adresbalk. Als u erop klikt, kunt u de details van het geïnstalleerde certificaat bekijken. Internationale bedrijven als Verisign en Thawte distribueren deze SSL-certificaten.

## CRT-bestandsindeling

CRT-bestanden zijn in ASCII-indeling en kunnen in elke teksteditor worden geopend om de inhoud van het certificaatbestand te bekijken. Het volgt de X.509-certificeringsnorm die de structuur van het certificaat definieert. Het definieert de gegevensvelden die in het SSL-certificaat moeten worden opgenomen. CRT behoort tot het PEM-formaat van certificaten die Base64 ASCII-gecodeerde bestanden zijn.

### PEM-bestandsstructuur

Een PEM-bestand kan meerdere certificaten hebben. In een dergelijk geval volgt elk certificaat in het PEM-bestand de volgende structuur.

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

### Voorbeeld van CRT-bestandsindeling

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenties ##

* [Openbare sleutels, privésleutels en certificaten](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

