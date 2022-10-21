---
date: 2019-12-09
keywords: "arc, .arc, arc-Dateiformat, wie man arc-Dateien öffnet, .arc-Erweiterung, arc-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "ARC-Dateiformat"
linktitle: "BOGEN"
description: "Erfahren Sie mehr über das ARC-Dateiformat und APIs, die ARC-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Was ist eine ARC-Datei?

ARC ist ein verlustfreies Datenkomprimierungs- und Archivierungsformat, das von System Enhancement Associates (SEA) entwickelt wurde. Das Dateiformat und die Anwendung, die es erstellt, heißen beide ARC. ARC war in den frühen Tagen des DFÜ-BBS sehr beliebt, da es die Funktionen der Komprimierung und Archivierung mehrerer Dateien in derselben Datei kombinierte. ARC wurde später durch [ZIP](/de/compression/zip/) ersetzt, das bessere Komprimierungsverhältnisse bot.

Die .arc-Dateierweiterung wird von mehreren anderen nicht verwandten Archivdateitypen verwendet, wie dem ARC-Format, das vom Internet Archive zum Speichern mehrerer Webressourcen verwendet wird, einem anderen ARC-Format, das vom FreeArc-Archiver verwendet wird, einem anderen Format, das von Nintendo für Ressourcen verwendet wird, usw .

## Kurze Geschichte des ARC-Dateiformats

Das ARC-Programm wurde 1985 von Thom Henderson von System Enhancement Associates geschrieben. Dieses Programm gruppierte Dateien in einer einzigen Archivdatei und komprimierte sie auch. Die vom ARC-Programm generierten Dateien verwendeten die Erweiterung .arc. SEA veröffentlichte 1986 den Quellcode für ARC und ARC wurde 1987 von Howard Chu auf Unix und Atari ST portiert.

Phil Katz hat PKARC und PKXARC zum Archivieren und Extrahieren von Dateien entwickelt. Die Dateien funktionierten mit dem ARC-Dateiformat und waren deutlich schneller. Im Gegensatz zu ARC teilte Katz die Komprimierungs- und Archivierungsfunktionen auf zwei verschiedene Dateien auf, was den Speicherbedarf für deren Ausführung reduzierte.

Nach dem Rechtsstreit zwischen SEA und Katz zog sich SEA aus dem Shareware-Markt zurück und entwickelte ARC+Plus mit einer Vollbild-Benutzeroberfläche. Das ARC-Format ist auf dem PC nicht mehr üblich.

## ARC-Dateiformat

Die ARC-Datei besteht aus einer Folge von Dateiheader und Datei, gefolgt von der Archivende-Markierung, wie unten gezeigt.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC-Datei-Header ###

|Offset|Label|Typ|Wert|Beschreibung|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Methode|
|02|ARCFNT|DS|12|Dateiname|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Komprimierte Größe|
|13|ARCDAT|DW|0000|Dateidatum (MSDOS)|
|15|ARCTIM|DW|0000|Dateizeit (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Unkomprimierte Größe|
|1D|ARCFIL|DS|ARCNSZ| |

### Komprimierungsmethoden ###

Das Komprimierungsverfahren-Byte gibt das verwendete Komprimierungsverfahren an. Im Folgenden sind die für die ARC-Datei verwendeten Komprimierungsmethoden aufgeführt.

|Methode|Name|Beschreibung|
|---|---|---|
|0|Gespeichert|Keine Komprimierung verwendet|
|1|Gepackt|Wiederholte Lauflängencodierung (RLE)|
|2|Squeezed|Huffman-Kodierung|
|3|Crunched|LZW mit 4K-Puffer, 12-Bit-Codes|
|4|Crunched|Erst packen, dann LZW 4K Buffer mit 12 Bit|
|5|Crunched|Packing, LZW, 4K-Puffer, variable Länge (9-12 Bit)|
|6|Squashed|LZW, 8K-Puffer, variable Länge (9-13 Bit)|
|7|Crushed|Packen, dann LZW 8K Buffer, 2-13 Bit (PAK 1.0)|
|8|Destillieren|Dynamischer Huffman mit 8K-Puffer (PAK 2.0)|

## Verweise

- [ARC (Dateiformat) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(Dateiformat))

