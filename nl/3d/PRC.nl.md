---
date: 2019-10-11
keywords: prc, .prc, prc-bestandsindeling, hoe prc-bestanden te openen, .prc-extensie, prc-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC-bestandsindeling
linktitle: PRC
description: "Meer informatie over de PRC-bestandsindeling en API's die PRC-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## De PRC-bestandsindelingen
De ".prc" extensies worden gebruikt voor Product Representation Compact 3D bestandsformaat en een e-book bestandsformaat door MobiPocket.

## Wat is een Product Representation Compact-bestand (PRC)?

PRC (Product Representation Compact) is een 3D-bestandsindeling die is geoptimaliseerd voor het opslaan, laden en weergeven van 3D-gegevens, met name afkomstig van CAD-systemen (Computer-Aided Design). Het is een sequentieel binair bestand, geschreven op een draagbare manier. PRC kan worden gebruikt om 3D-gegevens in een PDF-bestand in te sluiten. PRC ondersteunt de meeste hoofdconstructies van CAD, zoals assemblages en onderdelen, bomen van 3D-entiteiten, exacte geometrieweergave, driehoekige weergave en opmaak. PRC gebruikt de extensie .prc en het gebruikte internetmediatype is *model/prc*.

PRC is een multifunctioneel bestandsformaat dat op basis van het gebruik ervan kan worden opgeslagen met reguliere compressie om CAD-gegevens direct weer te geven, of kan worden opgeslagen met hoge compressie om de bestandsgrootte te verkleinen. De 3D-gegevens die zijn opgeslagen in een PDF met PRC-indeling, zijn compatibel met CAM- en CAE-toepassingen.

### Product Representation Compact (PRC) bestandsformaatspecificatie

Een PRC-bestand heeft één hoofdkopgedeelte gevolgd door een of meer bestandsstructuren gevolgd door één modelbestand aan het einde. Een bestandsstructuur heeft één kop, gevolgd door de volgende gegevenssecties:

- **Globals**: het bevat de bestandsstructuren en kleuren waarnaar wordt verwezen, lijnstijlen en coördinatensystemen voor elke boomentiteit van de bestandsstructuur.
- **Boom**: het bevat een beschrijving van de boomstructuur van items, zoals productvoorkomens, onderdeeldefinities, representatie-items en opmaak.
- **Tessellation**: het bevat alle mozaïekachtige (driehoekige) gegevens in de bladentiteiten van de boom (representatie-items en markeringen).
- **Geometrie**: het bevat alle exacte geometrie- en topologiegegevens van de bladentiteiten van de boom (representatie-items).
- **Extra geometrie**: het bevat de samenvattende gegevens van de geometrie. Hierdoor kan het bestand gedeeltelijk worden geladen zonder de gehele geometrie te laden.

Het volgende is de structuur van een typisch PRC-bestand.

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
## Wat is een MobiPocket e-bookbestand met PRC-extensie?
Een e-book bestandsformaat dat is geïntroduceerd door een Frans bedrijf genaamd **Mobipocket** gebruikt ook de extensie ".prc". In eerste instantie lanceerde Mobipocket een gratis applicatie voor meerdere slimme apparaten zoals tablet-pc's, PDA's en smartphones. De extensie ".prc" is eigenlijk identiek aan .mobi, maar wordt vooral gebruikt voor PDA's die alleen de extensie **.prc** of **.pdb** ondersteunen.

### Mobipocket PRC bestandsformaat specificaties
Het MobiPocket PRC-bestandsformaat is gebaseerd op de Open eBook-standaard die XHTML gebruikt en kan ook JavaScript en frames bevatten. Ondersteuning voor native SQL-query's voor gebruik met ingesloten databases is ook beschikbaar.

De Mobipocket Reader heeft een home page bibliotheek. Lezers kunnen blanco pagina's invoegen in elk deel van een boek en variabele tekeningen toevoegen. De objecten zoals Annotaties, bladwijzers, correcties, notities en tekeningen zijn beheersbaar vanaf één locatie. Afbeeldingen worden geconverteerd naar GIF-formaat en hebben een maximale grootte van 64K, wat voldoende is voor mobiele telefoons met kleine schermen. Mobipocket Reader heeft de elektronische bladwijzers en een ingebouwd woordenboek.

De reader heeft een full screen modus voor lezen en ondersteuning voor veel PDA's, Communicators en Smartphones. De Mobipocket-producten ondersteunen de meeste Palm-besturingssystemen, Windows, Symbian, BlackBerry, maar niet Android. De reader werkt onder Linux of Mac OS X met WINE.

## Referenties

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC-formaatspecificatie](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Vergelijking van e-bookformaten - Door Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

