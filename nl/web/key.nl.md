{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over KEY-bestandsindeling en API's die KEY-bestanden kunnen maken en openen.",
  "title" :"KEY File Format - Privacy-Enhanced Mail Private Key File",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Wat is een KEY-bestand?

Een KEY-bestand is het privégedeelte van een beveiligingsmechanisme dat op schijf wordt opgeslagen in het PEM-bestandsformaat (Privacy-Enhanced Mal). Het wordt gebruikt om informatie te decoderen die wordt uitgewisseld tussen een webbrowser en de webserver die de browseverzoeken bedient. Een KEY-bestand bevat gecodeerde strings die nutteloos zijn voor het menselijk oog, maar die de essentie zijn van het coderen/decoderen van informatie-uitwisseling als onderdeel van een SSL-certificaat op webservers. KEY-bestanden worden automatisch gegenereerd en aan de clientzijde geïnstalleerd.

U kunt **KEY**-bestanden openen met elke teksteditor, zoals Microsoft Notepad (Windows), Apple TextEdit (Mac) of GitHub Atom (platformoverschrijdend). KEY-bestanden zijn vergelijkbaar met de bestandsindelingen [CRT](/nl/web/crt/) en [CER](/nl/web/cer/).

## KEY-bestandsindeling - Meer informatie

KEY-bestanden worden op schijf opgeslagen als platte tekstbestanden, maar zijn gecodeerde tekenreeksen die niet mensvriendelijk zijn om te lezen. In de praktijk hebben gebruikers geen begrip van de tekenreeksen wanneer ze in een teksteditor worden geopend. Het private key-certificaat is vertrouwelijk en mag met niemand worden gedeeld. Het volledige proces van het beveiligen van informatie-uitwisseling via internet omvat een:

* **Openbare sleutel** - gebruikt om gebruikersinformatie te coderen voor de uitwisseling van gegevens tussen de browser en de webservers
* **Privésleutel** - gebruikt om de informatie te decoderen zoals deze wordt ontvangen door de webserver

De SSL-certificaten, ook wel X.509-certificaten genoemd, zijn uniek voor elke website. KEY-bestanden met de volgende syntaxis:

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

### KEY-bestand Voorbeeld

Hieronder volgt een voorbeeld van een privésleutelbestand.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenties

* [Openbare sleutels, privésleutels en certificaten](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

