{
  "date" : "2019-10-11",
  "keywords" :[ "bz2-bestand", "bz2-bestandsindeling", "wat is een bz2-bestand", "bestand", "bz2-voorbeeld", "bz2-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Gecomprimeerd bestandsformaat",
  "description":"Leer te weten wat een BZ2-bestand is en wat API's zijn die BZ2-bestanden kunnen maken en openen.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Wat is een BZ2-bestand?

BZ2 zijn gecomprimeerde bestanden die zijn gegenereerd met behulp van de [BZIP2](http://www.bzip.org/) open source compressiemethode, meestal op UNIX- of Linux-systemen. Het wordt gebruikt voor het comprimeren van een enkel bestand en is niet bedoeld voor het archiveren van meerdere bestanden. Dit in tegenstelling tot het TAR-bestandsformaat op dezelfde platforms dat meerdere bestanden in één bestand archiveert, maar zonder compressie. Bestanden die zijn gecomprimeerd als BZ2 kunnen worden gedecomprimeerd met toepassingen zoals [WinZip](https://www.winzip.com/win/en/). BZIP2 gebruikt Run-Length Encoding (RLE) of [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) compressie-algoritme om hoge compressieniveaus te bereiken.

## BZ2-bestandsindeling

Er zijn geen formele specificaties beschikbaar voor dit bestandsformaat. Een onofficiële [reverse engineered specificaties](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) laat echter zien dat een .bz2-stream bestaat uit een 4-byte header die wordt gevolgd door nul of meer gecomprimeerde blokken. Het wordt onmiddellijk gevolgd door een end-of-stream-markering die een 32-bits CRC bevat voor de hele stroom in platte tekst die wordt verwerkt. Er is geen opvulling tussen de gecomprimeerde blokken en alle blokken zijn bit-uitgelijnd.

## BZ2-bestand uitpakken/uitpakken

U kunt een BZ2-bestand op Windows en Mac OS uitpakken met software zoals WinZip. Op linux, de volgende opdracht in terminal.

```
bzip2 -d filename.bz2
```

## Referenties

* [BZIP2-formaatspecificaties](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

