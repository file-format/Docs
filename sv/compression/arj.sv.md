---
date: 2019-12-09
keywords: arj, .arj, arj-filformat, hur man öppnar arj-filer, .arj-tillägg, arj-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ filformat
linktitle: ARJ
description: "Lär dig mer om ARJ-filformat och API:er som kan skapa och öppna ARJ-filer." 
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Vad är en ARJ fil? ##

ARJ (Arkiverad av Robert Jung) är en högeffektiv komprimerad arkivfil utvecklad av Robert K. Jung. ARJ utvecklades för DOS och tidiga versioner av Windows i början av 1990-talet. ARJ-filer är användbara för att säkerhetskopiera eller dela ett stort antal filer eftersom du inte behöver hålla reda på alla dessa filer och det finns bara en enda fil att hantera. Tillägget .arj används för ARJ-arkivfilerna.

## ARJ-filformat ##

En ARJ-fil innehåller två typer av rubriker:

- Huvudhuvud: Det finns en huvudhuvud i början av arkivet.
- Lokala rubriker: Lokala rubriker finns före varje fil.

|Offset|Typ|Antal|Beskrivning|
|---|---|---|---|
|0000h|ord|1|ID=0EA60h|
|0002h|ord|1|grundläggande rubrikstorlek|
|0004h|byte|1|Storlek på rubrik|
|0005h|byte|1|Arkiverens versionsnummer|
|0006h|byte|1|Minsta versionsnummer behövs|
|0007h|byte|1|Värd OS:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (System xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - NÄSTA</br> 9 - VAX VMS|
|0008h|byte|1|Interna flaggor, bitmappade:</br> 0 - inget lösenord / lösenord</br> 1 - reserverad</br> 2 - filen fortsätter på nästa disk</br> 3 - fil startpositionsfält är tillgängligt</br> 4 - sökvägsöversättning ( "\" till "/" )|
|0009h|byte|1|Kompressionsmetod:</br> 0 - lagras</br> 1 - komprimerad mest</br> 2 - komprimerad</br> 3 - komprimeras snabbare</br> 4 - komprimerad snabbast|
|000Ah|byte|1|Filtyp:</br> 0 - binär</br> 1 - 7-bitars text</br> 2 - kommentarshuvud</br> 3 - katalog</br> 4 - volymetikett|
|000Bh|byte|1|reserverad|
|000Ch|dword|1|Datum/tid för originalfilen i MS-DOS-format|
|0010h|dword|1|Storleken på den komprimerade filen|
|0014h|dword|1|Storlek på originalfilen"|
|0018h|dword|1|CRC-32 för originalfilen|
|001Ah|ord|1|Filspecifik position i filnamn|
|001Ch|word|1|Filattribut|
|001Eh|word|1|Värddata|
|?|dword|1|Utökad fil startposition|
|????h|dword|1|CRC-32 i grundhuvudet|
|????h|word|1|Storlek på den första utökade rubriken|
|????h+"SIZ"+2|dword|1|CRC-32 för den utökade rubriken|
|????h+"SIZ"+6|byte|?|Komprimerad fil|

## Referenser ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

