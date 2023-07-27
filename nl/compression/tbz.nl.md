{
  "date" : "2019-10-11",
  "keywords" :[ "tbz-bestand", "tbz-bestandsformaat", "wat is een tbz-bestand", "bestand", "tbz-voorbeeld", "tbz-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip gecomprimeerd teerarchief",
  "description":"Meer informatie over TBZ-bestandsindelingen en API's die TBZ-bestanden kunnen maken en openen.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Wat is een TBZ-bestand?

Een bestand met de extensie .tbz is een gecomprimeerd archief dat BZIP-compressie gebruikt om de inhoud van de inhoudsbestanden te verkleinen. De TBZ-bestanden zijn in feite UNIX [TAR](/nl/compression/tar/) gearchiveerde bestanden die vervolgens met BZIP zijn gecomprimeerd. De meest recente compressie op het tweede niveau is [BZIP2](/nl/compression/bz2/) die BZIP heeft vervangen. Het TBZ-bestandsformaat is geschikt voor het overbrengen van grote bestanden. TBZ-bestanden kunnen worden geopend/uitgepakt met softwaretoepassingen zoals 7-Zip, PeaZip en jZip. Linux- en macOS-gebruikers kunnen ook een TBZ openen met de BZIP2-opdracht vanuit een terminalvenster.

## TBZ-bestandsindeling

TBZ-bestanden zijn eigenlijk gecomprimeerde archieven die zijn gemaakt met BZIP/[BZIP2](/nl/compression/bz2/)-compressie. Er zijn geen formele specificaties beschikbaar voor dit bestandsformaat. Een onofficiële [reverse engineered specificaties](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) laat echter zien dat een .bz2-stream bestaat uit een 4-byte header die wordt gevolgd door nul of meer gecomprimeerde blokken.

## Referenties ##

* [BZIP2-formaatspecificaties](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

