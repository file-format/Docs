{
  "date" : "2022-01-23",
  "keywords" :[ "xz-bestand", "bestandsindeling", "wat is een xz-bestand", "bestand", "xz-voorbeeld", "xz-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ-bestand - XZ-gecomprimeerd archief",
  "description":"Meer informatie over XZ-bestandsindeling en API's die XZ-bestanden kunnen maken en openen.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Wat is een XZ-bestand?

XZ is een gecomprimeerde bestandsindeling die gebruikmaakt van het LZMA2-compressiealgoritme. Het is ontworpen als vervanging voor de populaire gzip- en bzip2-formaten en biedt een aantal voordelen ten opzichte van deze oudere standaarden. XZ-bestanden worden goed ondersteund op veel platforms en kunnen snel en gemakkelijk worden gedecomprimeerd. Hoewel ze niet zo gewoon zijn als [ZIP](/nl/compression/zip/)- of [RAR](/nl/compression/rar/)-bestanden, kunnen XZ-archieven worden gebruikt om grote hoeveelheden gegevens op te slaan zonder concessies te doen aan de compressiekwaliteit. Als u grote bestanden moet comprimeren of decomprimeren, is de XZ-bestandsextensie het overwegen waard.

## XZ-bestandsindeling

XZ-bestand worden gegenereerd en opgeslagen als binaire bestanden op schijf. Het gebruikt het LZMA-algoritme om gegevens te comprimeren en kan een compressieverhouding tot 50% bereiken. XZ-bestanden worden meestal gebruikt voor softwaredistributies en back-uparchieven. Ze kunnen worden gedecomprimeerd met behulp van het XZ-hulpprogramma, dat bij de meeste Linux-distributies is inbegrepen.

## Unzip XZ-bestanden op Linux/Unix

Om XZ-bestanden uit te pakken, installeer eerst het pakket `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Gebruik de opdracht `unxz` om .xz-bestanden uit te pakken:
```
$ unxz compressed_xz_file.xz
```

of gebruiken met --decompress optie van XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referenties

* [XZ-hulpprogramma's](https://en.wikipedia.org/wiki/XZ_Utils)

