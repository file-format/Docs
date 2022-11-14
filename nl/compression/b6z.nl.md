{
  "date" : "2019-10-11",
  "keywords" :[ "b6z-bestand", "b6z-bestandsindeling", "wat is een b6z-bestand", "bestand", "b6z-voorbeeld", "b6z-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP-archiefbestandsindeling",
  "description":"Meer informatie over B6Z-bestandsindeling en API's die B6Z-bestanden kunnen maken en openen.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Wat is een B6Z-bestand?

Een bestand met de extensie .b6z is een gecomprimeerd archiefbestand gemaakt door macOS-softwaretoepassing [B6Zip](http://b6zip.com) die wordt gebruikt om bestanden te comprimeren en te decomprimeren. Het is een relatief nieuw archiefformaat dat een hogere compressieverhouding mogelijk maakt. B6Z heeft een open architectuur en ondersteunt bestandsgroottes tot 900000 PB. Het ondersteunt gegevenscompressie, foutherstel en bestandsoverspanning. De B6Zip-hulpprogrammasoftware is gratis beschikbaar op MacOS om verschillende soorten gecomprimeerde bestanden te openen, waaronder B6Z.

## B6Z-bestandsindeling

Het B6Z-bestandsformaat is gebaseerd op een open architectuur en biedt solide compressie met AES-256-coderingsalgoritme. Het gebruikt LZMA2 als standaard compressiemethode, maar ondersteunt als volgt ook andere compressiemethoden.

|Methode|Beschrijving|
---|---|
|LZMA |Geoptimaliseerde versie van LZ77-algoritme|
|LZMA2| Verbeterde versie van LZMA|
|Laat leeglopen| Regulier LZ77-algoritme|
|BZip2| Standaard BWT-algoritme|
|PPMD| Dmitry Shkarin's PPMdH|

Het hulpprogramma B6Zip ondersteunt al deze compressiestandaarden en is sterk geoptimaliseerd, wat resulteert in hoge snelheid. Het ondersteunt het werken met [ZIP](/nl/compression/zip/), [TAR](/nl/compression/tar/) en [RAR](/nl/compression/rar/) bestandsformaten. B6Z-bestanden hebben MIME-type application/x-b6z-gecomprimeerd.

## Referenties

* [B6Zip](http://b6zip.com)

