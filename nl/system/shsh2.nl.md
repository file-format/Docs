{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2-bestand - iOS SHSH Blob-bestandsformaat",
  "description":"Meer informatie over wat een SHSH2-bestand is.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Wat is een SHSH2-bestand?

Een SHSH2-bestand, ook bekend als een SHSH-blob of ECID SHSH, is een digitale handtekening die door Apple wordt gebruikt om firmware-updates voor iOS-apparaten zoals iPhones, iPads en iPods te authenticeren en verifiëren. Het bevat een unieke identificatie voor het apparaat dat bekend staat als ECID (Exclusive Chip ID). Het bevat ook informatie over de firmwareversie die op het apparaat is geïnstalleerd.

## SHSH2-bestandsindeling - Meer informatie

SHSH2-bestanden worden in binair bestandsformaat op schijf opgeslagen en de interne bestandsstructuurdetails van dit bestandsformaat zijn niet openbaar beschikbaar.

Wanneer een nieuwe versie van iOS wordt geïnstalleerd op een Apple-apparaat zoals iPhone, iPad of Mac, wordt een SHSH2-bestand gegenereerd. Dit SHSH2-bestand wordt naar Apple-servers gestuurd, die dit digitale handtekeningbestand lezen en verifiëren. Op basis van deze informatie staat de server de installatie toe of verhindert deze.

Hetzelfde gebeurt wanneer er om een update wordt gevraagd. Wanneer een gebruiker via iTunes of andere software een update of herstel van zijn apparaat aanvraagt, controleren de servers van Apple of het SHSH2-bestand overeenkomt met de ECID en de firmwareversie van het apparaat voordat de update wordt voortgezet.

## Referenties

* [SHSH Blob - Door Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS-saver](https://tsssaver.1conan.com/v2/)

