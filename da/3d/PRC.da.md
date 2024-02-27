---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC fil formularat
linktitle: PRC
description: Ltjene om PRC filformat og API'er, der kan oprette og åbne PRC fils.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC-filformaterne
.prc-udvidelserne bruges til produktrepræsentation Compact 3D-filformat og et e-bogs-filformat af MobiPocket.

## Hvad er en Product Representation Compact (PRC) fil?

PRC (Product Representation Compact) er et 3D-filformat, der er optimeret til at gemme, indlæse og vise 3D-data, der især kommer fra CAD-systemer (Computer-Aided Design). Det er en sekventiel binær fil, skrevet på en bærbar måde. PRC kan bruges til at indlejre 3D-data i en PDF-fil. PRC understøtter de fleste hovedkonstruktioner af CAD, såsom samlinger og dele, træer af 3D-enheder, nøjagtig geometrirepræsentation, trianguleret repræsentation og markup. PRC bruger .prc-udvidelsen, og den anvendte internetmedietype er *model/prc*.

PRC er et multifunktionelt filformat, der baseret på dets brug enten kan lagres ved hjælp af almindelig komprimering til direkte at repræsentere CAD-data eller gemmes ved hjælp af høj komprimering for at reducere filstørrelsen. 3D-dataene, der er gemt i en PDF ved hjælp af PRC-format, er interoperable med CAM- og CAE-applikationer.

### Produktrepræsentation Compact (PRC) filformatspecifikation

En PRC-fil har en hovedhovedsektion efterfulgt af en eller flere filstrukturer efterfulgt af en modelfil i slutningen. En filstruktur har én overskrift efterfulgt af følgende datasektioner:

- **Globals**: Den indeholder de refererede filstrukturer og farver, linjestile og koordinatsystemer for hver træenhed i filstrukturen.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tessellation**: Den indeholder alle tessellerede (triangulerede) data i træets bladenheder (repræsentationselementer og markeringer).
- **Geometri**: Den indeholder alle nøjagtige geometri- og topologidata for træets bladenheder (repræsentationselementer).
- **Ekstra geometri**: Den indeholder oversigtsdata for geometrien. Dette gør det muligt at indlæse filen delvist uden at indlæse hele geometrien.

Det følgende er strukturen af en typisk PRC-fil.

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
## Hvad er en MobiPocket e-bogsfil med PRC-udvidelse
Et e-bogs filformat, som er introduceret af et fransk firma kaldet **Mobipocket**, bruger også udvidelsen .prc. I første omgang lancerede Mobipocket en gratis applikation til flere smarte enheder som tablet pc'er, PDA'er og smartphones. .prc-udvidelsen er faktisk identisk med .mobi, men bruges især til PDA'er, som kun understøtter **.prc** eller **.pdb** udvidelser.

### Mobipocket PRC filformatspecifikationer
MobiPocket PRC-filformatet er baseret på Open eBook-standarden ved hjælp af XHTML, og det kan også inkludere JavaScript og rammer. Understøttelse af native SQL-forespørgsler, der skal bruges med indlejrede databaser, er også tilgængelig.

Mobipocket Reader har et hjemmesidebibliotek. Læsere kan indsætte tomme sider i enhver del af en bog og tilføje variable tegninger. Objekter som anmærkninger, bogmærker, rettelser, noter og tegninger kan håndteres fra et enkelt sted. Billeder konverteres til GIF-format og har en maksimal størrelse på 64K, hvilket er tilstrækkeligt til mobiltelefoner med små skærme. Mobipocket Reader har de elektroniske bogmærker og en indbygget ordbog.

Læseren har en fuldskærmstilstand til læsning og understøttelse af mange PDA'er, kommunikatører og smartphones. Mobipocket-produkterne understøtter de fleste Palm-operativsystemer, Windows, Symbian, BlackBerry, men ikke Android. Læseren fungerer under Linux eller Mac OS X ved hjælp af WINE.

## Referencer

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

