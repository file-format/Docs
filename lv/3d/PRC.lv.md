---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC faila veidlapaat
linktitle: PRC
description: Lnopelniet par ĶTR faila formātu un API, kas var izveidot un atvērt ĶTR failus.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## ĶTR failu formāti
Paplašinājumus .prc MobiPocket izmanto produktu reprezentācijas kompaktā 3D faila formātā un e-grāmatas faila formātā.

## Kas ir Product Representation Compact (PRC) fails?

PRC (Product Representation Compact) ir 3D faila formāts, kas ir optimizēts 3D datu glabāšanai, ielādei un attēlošanai, jo īpaši no CAD (Computer-Aided Design) sistēmām. Tas ir secīgs binārs fails, kas rakstīts pārnēsājamā veidā. ĶTR var izmantot, lai iegultu 3D datus PDF failā. ĶTR atbalsta lielāko daļu CAD galveno konstrukciju, piemēram, mezglus un daļas, 3D entītiju kokus, precīzu ģeometrijas attēlojumu, trīsstūrveida attēlojumu un iezīmēšanu. ĶTR izmanto paplašinājumu .prc, un izmantotais interneta multivides veids ir *modelis/prc*.

ĶTR ir daudzfunkcionāls faila formāts, kuru, pamatojoties uz tā lietojumu, var saglabāt, izmantojot parasto saspiešanu, lai tieši attēlotu CAD datus, vai arī saglabāt, izmantojot augstu saspiešanu, lai samazinātu faila lielumu. 3D dati, kas saglabāti PDF failā, izmantojot PRC formātu, ir sadarbspējīgi ar CAM un CAE lietojumprogrammām.

### Product Representation Compact (PRC) faila formāta specifikācija

ĶTR failam ir viena galvenā galvenes sadaļa, kam seko viena vai vairākas failu struktūras, kam beigās ir viens modeļa fails. Faila struktūrai ir viena galvene, kam seko šādas datu sadaļas:

- **Globālie**: tajā ir ietvertas atsauces failu struktūras un krāsas, līniju stili un koordinātu sistēmas katrai faila struktūras koka entītijai.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tesselācija**: tajā ir visi mozaīkas (trīsstūrveida) dati koka lapu entītijās (reprezentācijas vienumi un atzīmes).
- **Ģeometrija**: tajā ir visi precīzi ģeometrijas un topoloģijas dati par koka lapu entītijām (reprezentācijas vienumi).
- **Papildu ģeometrija**: tajā ir ģeometrijas kopsavilkuma dati. Tas ļauj daļēji ielādēt failu, neielādējot visu ģeometriju.

Tālāk ir sniegta tipiska ĶTR faila struktūra.

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
## Kas ir MobiPocket e-grāmatas fails ar ĶTR paplašinājumu
E-grāmatas faila formāts, ko ieviesis franču uzņēmums **Mobipocket**, arī izmanto paplašinājumu .prc. Sākotnēji Mobipocket palaida bezmaksas lietojumprogrammu vairākām viedierīcēm, piemēram, planšetdatoriem, plaukstdatoriem un viedtālruņiem. Paplašinājums .prc faktiski ir identisks .mobi, taču to īpaši izmanto plaukstdatoriem, kas atbalsta tikai **.prc** vai **.pdb** paplašinājumus.

### Mobipocket PRC faila formāta specifikācijas
MobiPocket PRC faila formāts ir balstīts uz Open eBook standartu, izmantojot XHTML, kā arī tas var ietvert JavaScript un rāmjus. Ir pieejams arī atbalsts vietējiem SQL vaicājumiem, kas izmantojami ar iegultām datu bāzēm.

Mobipocket Reader ir mājas lapas bibliotēka. Lasītāji var ievietot tukšas lapas jebkurā grāmatas daļā un pievienot mainīgus zīmējumus. Tādus objektus kā anotācijas, grāmatzīmes, labojumus, piezīmes un zīmējumus var pārvaldīt no vienas vietas. Attēli tiek pārveidoti GIF formātā, un to maksimālais izmērs ir 64 K, kas ir pietiekami mobilajiem tālruņiem ar maziem ekrāniem. Mobipocket Reader ir elektroniskās grāmatzīmes un iebūvēta vārdnīca.

Lasītājam ir pilnekrāna režīms lasīšanai un daudzu PDA, komunikatoru un viedtālruņu atbalstam. Mobipocket produkti atbalsta lielāko daļu Palm operētājsistēmu, Windows, Symbian, BlackBerry, bet ne Android. Lasītājs darbojas operētājsistēmā Linux vai Mac OS X, izmantojot WINE.

## Atsauces

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

