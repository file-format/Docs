---
date: 2019-12-09
keywords: "arj, .arj, arj-Dateiformat, wie man arj-Dateien öffnet, .arj-Erweiterung, arj-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "ARJ-Dateiformat"
linktitle: "ARJ"
description: "Erfahren Sie mehr über das ARJ-Dateiformat und APIs, die ARJ-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Was ist eine ARJ-Datei? ##

ARJ (Archived by Robert Jung) ist eine hocheffiziente komprimierte Archivdatei, die von Robert K. Jung entwickelt wurde. ARJ wurde Anfang der 1990er Jahre für DOS und frühe Windows-Versionen entwickelt. ARJ-Dateien sind nützlich, um eine große Anzahl von Dateien zu sichern oder freizugeben, da Sie nicht alle diese Dateien im Auge behalten müssen und nur eine einzige Datei zu handhaben ist. Die Erweiterung .arj wird für die ARJ-Archivdateien verwendet.

## ARJ-Dateiformat ##

Eine ARJ-Datei enthält zwei Arten von Headern:

- Hauptkopf: Am Anfang des Archivs befindet sich ein Hauptkopf.
- Lokale Header: Lokale Header sind vor jeder Datei vorhanden.

|Offset|Typ|Anzahl|Beschreibung|
|---|---|---|---|
|0000h|Wort|1|ID=0EA60h|
|0002h|word|1|grundlegende Headergröße|
|0004h|Byte|1|Größe des Headers|
|0005h|byte|1|Archiver-Versionsnummer|
|0006h|byte|1|Mindestversionsnummer erforderlich|
|0007h|byte|1|Host-Betriebssystem:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (System xx)</br> 5 - OS/2</br> 6 - APFEL GS</br> 7 - ATARI ST</br> 8 - Weiter</br> 9 - VAX VMS|
|0008h|byte|1|Interne Flags, Bitmap:</br> 0 - kein Passwort / Passwort</br> 1 - reserviert</br> 2 - Datei wird auf der nächsten Platte fortgesetzt</br> 3 - Dateistartpositionsfeld ist verfügbar</br> 4 - Pfadübersetzung ( "\" nach "/" )|
|0009h|byte|1|Komprimierungsmethode:</br> 0 - gespeichert</br> 1 - am meisten komprimiert</br> 2 - komprimiert</br> 3 - schneller komprimiert</br> 4 - am schnellsten komprimiert|
|000Ah|Byte|1|Dateityp:</br> 0 - binär</br> 1 - 7-Bit-Text</br> 2 - Kommentarkopfzeile</br> 3 - Verzeichnis</br> 4 - Datenträgerbezeichnung|
|000Bh|byte|1|reserviert|
|000Ch|dword|1|Datum/Uhrzeit der Originaldatei im MS-DOS-Format|
|0010h|dword|1|Größe der komprimierten Datei|
|0014h|dword|1|Größe der Originaldatei"|
|0018h|dword|1|CRC-32 der Originaldatei|
|001Ah|word|1|Position der Dateispezifikation im Dateinamen|
|001Ch|word|1|Dateiattribute|
|001Eh|word|1|Hostdaten|
|?|dword|1|Startposition der erweiterten Datei|
|????h|dword|1|CRC-32 des grundlegenden Headers|
|????h|word|1|Größe des ersten erweiterten Headers|
|????h+"SIZ"+2|dword|1|CRC-32 des erweiterten Headers|
|????h+"SIZ"+6|Byte|?|Komprimierte Datei|

## Verweise ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

