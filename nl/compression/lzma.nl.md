{
  "date" : "2021-04-08",
  "keywords" :[ "lzma-bestand", "lzma-bestandsindeling", "wat is een lzma-bestand", "bestand", "lzma-voorbeeld", "lzma-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA gecomprimeerd bestandsformaat",
  "description":"Wat is een LZMA-bestand en API's die LZMA-bestanden kunnen maken en openen.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Wat is een LZMA-bestand?

Een bestand met de extensie .lzma is een gecomprimeerd archiefbestand dat is gemaakt met behulp van de LZMA-compressiemethode (Lempel-Ziv-Markov chain Algorithm). Deze worden voornamelijk gevonden/gebruikt op het Unix-besturingssysteem en zijn vergelijkbaar met andere compressie-algoritmen zoals [ZIP](/nl/compression/zip/) voor het minimaliseren van de bestandsgrootte. LZMA is een oud bestandsformaat dat wordt of is vervangen door het .xz-formaat. Het MIME-type van het .lzma-formaat is \`application/x-lzma'. Dit bestandsformaat is ontworpen door Igor Pavlov voor gebruik in LZMA SDK.

## LZMA-bestandsindeling

Het LZMA-bestand bestaat uit twee hoofdonderdelen:

1. Koptekst
1. Gecomprimeerde gegevens


### LZMA-koptekst

De LZMA-bestanden hebben een header van 13 bytes die wordt gevolgd door de gecomprimeerde LZMA-gegevens. De LZMA-header bestaat uit:

* Eigendommen
* Woordenboekgrootte
* Niet-gecomprimeerde grootte

#### Eigenschappen LZMA-koptekst

Het veld Eigenschappen bevat drie eigenschappen. Tussen haakjes staat een afkorting, gevolgd door het waardebereik van de eigenschap. Het veld bestaat uit:

1) het aantal letterlijke contextbits (lc, [0, 8]);
2) het aantal letterlijke positiebits (lp, [0, 4]); en
3) het aantal positiebits (pb, [0, 4]).

#### LZMA-woordenboekgrootte

Dit wordt opgeslagen als een niet-ondertekend 32-bits little endian integer met waarden variërend van 2^n en 2^n + 2^(n-1). LZMA Utils kan bestanden met elke willekeurige woordenboekgrootte decomprimeren.

#### Niet-gecomprimeerde grootte
De niet-gecomprimeerde grootte wordt opgeslagen als een 64-bits little endian integer zonder teken. Een speciale waarde van 0xFFFF_FFFF_FFFF_FFFF geeft aan dat de niet-gecomprimeerde grootte onbekend is. De waarde wordt weergegeven door End of Payload Marker (\*) als en alleen als de niet-gecomprimeerde grootte onbekend is.

## Referenties

* [Lempel-Ziv-Markov-ketenalgoritme](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
