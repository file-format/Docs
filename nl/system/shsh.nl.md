{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH-bestand - iPhone/iPod Touch SHSH Blob-bestandsindeling",
  "description":"Meer informatie over wat een SHSH-bestand is.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Wat is een SHSH-bestand?

Een SHSH-bestand, ook wel Signature HaSH genoemd, is een digitale handtekening die door Apple wordt gebruikt om firmware-updates voor iOS-apparaten zoals iPhones, iPads en iPods te authenticeren en verifiëren.

## Verschil tussen SHSH- en SHSH2-bestandsformaten

Net als een SHSH2-bestand bevat het SHSH-bestand een unieke identificatie voor het apparaat, een zogenaamde "ECID" (Exclusive Chip ID), evenals informatie over de firmwareversie die op het apparaat is geïnstalleerd. SHSH-bestanden werden echter gebruikt in oudere versies van iOS (vóór iOS 10) en zijn sindsdien vervangen door SHSH2-bestanden.

## SHSH-bestandsindeling - Meer informatie

SHSH-bestanden worden op schijf opgeslagen in binair bestandsformaat. De details van de interne bestandsstructuur van dit bestandsformaat zijn niet openbaar beschikbaar.

SHSH-bestanden zijn belangrijk voor gebruikers die de firmware van hun apparaat willen downgraden naar een eerdere versie die niet langer door Apple wordt ondertekend. Door de SHSH-bestanden voor een specifieke firmwareversie op te slaan terwijl deze nog door Apple wordt ondertekend, kunnen gebruikers deze later gebruiken om de handtekeningverificatie van Apple te omzeilen en die firmwareversie op hun apparaat te installeren. Dit proces wordt ook wel 'jailbreaken' genoemd.

## Referenties

* [SHSH Blob - Door Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS-saver](https://tsssaver.1conan.com/v2/)

