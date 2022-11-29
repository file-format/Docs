---
date: 2019-10-11
keywords: prc, .prc, prc-filformat, hur man öppnar prc-filer, .prc-tillägg, prc-tillägg
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC filformat
linktitle: PRC
description: "Lär dig om PRC-filformat och API:er som kan skapa och öppna PRC-filer."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC-filformaten
Tilläggen ".prc" används för produktrepresentation Compact 3D-filformat och ett e-boksfilformat av MobiPocket.

## Vad är en Product Representation Compact-fil (PRC)?

PRC (Product Representation Compact) är ett 3D-filformat som är optimerat för att lagra, ladda och visa 3D-data, speciellt från CAD-system (Computer-Aided Design). Det är en sekventiell binär fil, skriven på ett portabelt sätt. PRC kan användas för att bädda in 3D-data i en PDF-fil. PRC stöder de flesta huvudkonstruktionerna av CAD, såsom sammansättningar och delar, träd av 3D-enheter, exakt geometrirepresentation, triangulerad representation och markering. PRC använder tillägget .prc och den typ av internetmedia som används är *model/prc*.

PRC är ett mångsidigt filformat som baserat på dess användning antingen kan lagras med vanlig komprimering för att direkt representera CAD-data eller lagras med hög komprimering för att minska filstorleken. 3D-data som lagras i en PDF med PRC-format är interoperabel med CAM- och CAE-applikationer.

### Produktrepresentation Compact (PRC) filformatspecifikation

En PRC-fil har en huvudhuvudsektion följt av en eller flera filstrukturer följt av en modellfil i slutet. En filstruktur har en rubrik följt av följande datasektioner:

- **Globals**: Den innehåller refererade filstrukturer och färger, linjestilar och koordinatsystem för varje trädentitet i filstrukturen.
- **Träd**: Den innehåller en beskrivning av trädet med objekt som produktförekomster, deldefinitioner, representationsartiklar och uppmärkning.
- **Tessellation**: Den innehåller alla tessellerade (triangulerade) data i trädets lövenheter (representationsobjekt och markeringar).
- **Geometri**: Den innehåller all exakt geometri och topologidata för trädets lövenheter (representationsobjekt).
- **Extra geometri**: Den innehåller sammanfattande data för geometrin. Detta gör att filen kan laddas delvis utan att ladda hela geometrin.

Följande är strukturen för en typisk PRC-fil.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Vad är en MobiPocket e-boksfil med PRC-tillägg
Ett e-boksfilformat som introduceras av ett franskt företag som heter **Mobipocket** använder också tillägget ".prc". Inledningsvis lanserade Mobipocket en gratis applikation för flera smarta enheter som surfplattor, handdatorer och smartphones. Tillägget ".prc" är faktiskt identiskt med .mobi men används särskilt för handdatorer som endast stöder tilläggen **.prc** eller **.pdb**.

### Mobipocket PRC filformatspecifikationer
MobiPocket PRC-filformatet är baserat på Open eBook-standarden med XHTML och det kan även inkludera JavaScript och ramar. Det finns också stöd för inbyggda SQL-frågor som ska användas med inbäddade databaser.

Mobipocket Reader har ett hemsidebibliotek. Läsare kan infoga tomma sidor i valfri del av en bok och lägga till variabla ritningar. Objekten som anteckningar, bokmärken, korrigeringar, anteckningar och ritningar kan hanteras från en enda plats. Bilder konverteras till GIF-format och har en maximal storlek på 64K vilket räcker för mobiltelefoner med små skärmar. Mobipocket Reader har elektroniska bokmärken och en inbyggd ordbok.

Läsaren har ett helskärmsläge för läsning och stöd för många handdatorer, kommunikatörer och smartphones. Mobipocket-produkterna stöder de flesta Palm-operativsystem, Windows, Symbian, BlackBerry, men inte Android. Läsaren fungerar under Linux eller Mac OS X med WINE.

## Referenser

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(filformat))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Jämförelse av e-boksformat - Av Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

