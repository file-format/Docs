{
  "date" : "2021-04-08",
  "keywords" :[ "mst-bestand", "mst-bestandsindeling", "wat is een mst-bestand", "bestand", "mst-voorbeeld", "mst-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU-bibliotheekarchiefbestandsindeling",
  "description":"Meer informatie over LBR-bestandsindeling en API's die LBR-bestanden kunnen maken en openen.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Wat is een LBR-bestand?

Een bestand met de extensie .lbr is een archiefbestand gemaakt met het LU-programma en gebruikt op CP/M- en DOS-besturingssystemen in de jaren 80. Het wordt niet meer gebruikt en is vervangen door moderne bestandsindelingen voor archivering. Het formaat comprimeert de ledenbestanden niet en fungeert hiervoor als containerarchief. De archiveringsfunctie werd meestal gebruikt voor de overdracht van gearchiveerde bestanden via internet. Omdat LBR geen compressie bood, werden andere hulpprogramma's zoals SQ of CRUNCH gebruikt om de ledenbestanden voor het archiveren of het resulterende archiefbestand na het archiveren te comprimeren om de grootte te verkleinen.

## LBR-bestandsindeling

Het LBR-bestandsformaat is ontworpen door Gary P. Novosielski en heeft geen technische details die publiekelijk beschikbaar zijn. LBR-bestanden beginnen met een 0x00 byte, gevolgd door 11 spaties (0x20), dan twee 0x00 bytes en vervolgens twee bytes die niet beide 0x00 zijn. Omdat het een containerbestandsformaat is, kan het worden uitgepakt met behulp van de LU.COM en NULU.COM.

## Referenties

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

