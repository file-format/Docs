---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ fil formularat
linktitle: ARJ
description: Ltjene om ARJ filformat og API'er, der kan oprette og åbne ARJ fils.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Hvad er en ARJ fil? ##

ARJ (Arkiveret af Robert Jung) er en højeffektiv komprimeret arkivfil udviklet af Robert K. Jung. ARJ blev udviklet til DOS og tidlige versioner af Windows i begyndelsen af 1990'erne. ARJ-filer er nyttige til at sikkerhedskopiere eller dele et stort antal filer, da du ikke behøver at holde styr på alle disse filer, og der kun er en enkelt fil at håndtere. .arj-udvidelsen bruges til ARJ-arkivfilerne.

## ARJ filformat ##

En ARJ-fil indeholder to typer overskrifter:

- Hovedhoved: Der er én hovedhoved i starten af arkivet.
- Lokale overskrifter: Lokale overskrifter er til stede før hver fil.

|Offset|Type|Optælling|Beskrivelse|
|---|---|---|---|
|0000h|ord|1|ID=0EA60h|
|0002h|ord|1|grundlæggende overskriftstørrelse|
|0004h|byte|1|Størrelse på overskrift|
|0005h|byte|1|Arkiverversionsnummer|
|0006h|byte|1|Minimum påkrævet versionsnummer|
|0007h|byte|1|Host OS:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (System xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - Næste</br> 9 - VAX VMS|
|0008h|byte|1|Interne flag, bitmappet:</br> 0 - ingen adgangskode / adgangskode</br> 1 - reserveret</br> 2 - filen fortsætter på næste disk</br> 3 - fil startpositionsfelt er tilgængeligt</br> 4 - stioversættelse (\ til /)|
|0009h|byte|1|Kompressionsmetode:</br> 0 - gemt</br> 1 - komprimeret mest</br> 2 - komprimeret</br> 3 - komprimeret hurtigere</br> 4 - komprimeret hurtigst|
|000Ah|byte|1|Filtype:</br> 0 - binær</br> 1 - 7-bit tekst</br> 2 - kommentarhoved</br> 3 - bibliotek</br> 4 - volumen etiket|
|000Bh|byte|1|reserveret|
|000Ch|dword|1|Dato/klokkeslæt for den originale fil i MS-DOS-format|
|0010h|dword|1|Størrelsen af den komprimerede fil|
|0014h|dword|1|Størrelse på den originale fil|
|0018h|dword|1|CRC-32 af den originale fil|
|001Ah|word|1|Filspecifik position i filnavn|
|001Ch|word|1|Filattributter|
|001Eh|word|1|Værtsdata|
|?|dword|1|Udvidet fil startposition|
|????h|dword|1|CRC-32 i den grundlæggende overskrift|
|????h|word|1|Størrelse af den første udvidede overskrift|
|????h+SIZ+2|dword|1|CRC-32 af den udvidede overskrift|
|????h+SIZ+6|byte|?|Komprimeret fil|

## Referencer ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

