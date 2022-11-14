---
date: 2020-08-12
keywords: flif, .flif, flif-bestandsindeling, hoe u flif-bestanden opent, .flif-extensie, flif-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF-bestandsindeling
linktitle: FLIF
description: "Meer informatie over de FLIF-bestandsindeling en API's die FLIF-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Wat is een FLIF-bestand? ##

FLIF (Free Lossless Image Format) is een lossless beeldformaat dat de .flif-extensie voor zijn bestanden gebruikt. FLIF claimt beter te presteren dan [PNG](/nl/image/png/), lossless [WebP](/nl/image/webp/), lossless BPG en lossless JPEG 2000 in termen van compressieverhouding. FLIF maakt gebruik van progressieve interliniëring, waardoor elke gedeeltelijke download van de afbeelding kan worden gebruikt als codering met verlies voor de gehele afbeelding.

## Korte geschiedenis ##

FLIF werd aangekondigd in september 2015 en de alfaversie werd uitgebracht in oktober 2015. In september 2016 werd de eerste stabiele versie van FLIF uitgebracht.

## FLIF-ontwerp ##

FLIF gebruikt een variant van CABAC (Context-adaptive binary arithmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) voor compressie. MANIAC is een entropiecoderingsalgoritme ontwikkeld door Jon Sneyers en Pieter Wuille. In MANIAC zijn de contexten knooppunten van beslissingsbomen die dynamisch worden geleerd tijdens het coderen. Dit maakt het contextmodel meer beeldspecifiek en resulteert in een betere compressie. FLIF heeft de volgende kenmerken:

- Ondersteunt lossless compressie
- Ondersteunt compressie met verlies met voorverwerking van de encoder
- Ondersteunt grijstinten, RGB en RGBA
- Ondersteunt kleurdiepte van 1 tot 16 bits per kanaal
- Ondersteunt geïnterlinieerde en niet-geïnterlinieerde bestanden
- Ondersteunt progressieve decodering van gedeeltelijk gedownloade bestanden
- Ondersteunt animaties
- Ondersteunt ingebouwde ICC-kleurprofielen, Exif- en XMP-metadata
- Heeft beperkte ondersteuning voor het comprimeren van Camera Raw-bestanden (RGGB)

## FLIF-bestandsindeling ##

Een FLIF-bestand bestaat uit de volgende vier delen:

## Hoofdkop ##

De hoofdkop bevat de belangrijkste metadata inclusief de breedte, hoogte, kleurdiepte, aantal frames.

|Type|Waarde|Beschrijving|
|---|---|---|
|4 bytes|"FLIF"|Magie|
|4 bits|3 = ni nog steeds; 4 = ik nog steeds; 5 = geen animatie; 6 = ik anime|Interliniëring, animatie|
|4 bits|1 = grijswaarden; 3 = RGB; 4 = RGBA|Aantal kanalen (nb_channels)|
|1 byte|'0','1','2' ('0'=custom)|Bytes per kanaal (Bpc)|
|varint|breedte-1|Breedte|
|varint|hoogte-1|Hoogte|
|varint|nb_frames-2 (alleen als animatie)|Aantal frames (nb_frames)|

## Metadata-brokken ##

Dit deel bevat niet-pixelachtige Exif/XMP-metadata, ICC-kleurprofielen, enz. die zijn gecodeerd met DEFLATE-compressie. Deze chunks worden op dezelfde manier gedefinieerd als PNG-chunks, met het verschil dat de chuck-grootte is gecodeerd met een variabel aantal bytes. De namen van Chunks kunnen 4 letters (4 bytes) of een waarde lager dan 32 zijn, wat wijst op een niet-optioneel blok.

Het volgende is een voorbeeld van optionele klauwplaten:

|Baknaam|Beschrijving|Inhoud (na DEFLATE-decompressie)|
|---|---|---|
|iCCP|ICC-kleurprofiel|ruwe ICC-kleurprofielgegevens|
|eXif|Exif-metadata|"Exif\0\0"-header gevolgd door een TIFF-header en de EXIF-gegevens|
|eXmp|XMP-metadata|XMP in een alleen-lezen xpacket zonder opvulling|

### Naamgeving ###

- **Eerste letter**: hoofdletters worden gebruikt voor kritieke en kleine letters voor niet-kritieke brokken.
- **Tweede letter**: hoofdletters worden gebruikt voor openbare en kleine letters voor privé-chunks
- **Derde letter**: hoofdletters worden gebruikt voor klauwplaten die nodig zijn om de afbeelding correct weer te geven en kleine letters zijn niet belangrijk om de afbeelding weer te geven.
- **Vierde letter**: hoofdletters worden gebruikt voor klauwplaten die veilig blindelings kunnen worden gekopieerd. Kleine klauwplaten zijn afhankelijk van de afbeeldingsgegevens.

## Tweede kop ##

Hierin staat de informatie over de daadwerkelijke codering van de pixels.

|Type|Beschrijving|Voorwaarde|Standaardwaarde|
|---|---|---|---|
|1 byte|NUL byte (0x00), chunknaam van een FLIF16 bitstream||
|uni_int(1,16)|Bits per pixel van de kanalen|Bpc == '0': repeat(nb_channels)|8 if Bpc == '1', 16 if Bpc == '2'|
|uni_int(0,1)|Vlag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Aantal lussen|nb_frames > 1||
|uni_int(0,60_000)|Framevertraging in ms|nb_frames > 1: herhaal(nb_frames)|
|uni_int(0,1)|Vlag: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alfa deler|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Vlag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variabele|Transformaties (zie hieronder)|||
|uni_int(1) = 0|Indicatorbit: gedaan met transformaties|||
|uni_int(0,2)|Onzichtbare pixelvoorspeller|alpha_zero && interlaced && alpha-bereik omvat nul||

**Kanalen**

|Kanaalnummer|Beschrijving|
|---|----|
|0|Rood of grijs|
|1|Groen|
|2|Blauw|
|3|Alfa|

**Transformaties**

|Type|Beschrijving|
|---|---|
|uni_int(1) = 1|Indicatorbit: nog niet klaar|
|uni_int(0,13)|Transformatie-ID|
|variabele|Transformatiegegevens (afhankelijk van transformatie)|

Transformatie wordt gebruikt om pixelgegevens aan te passen voor een betere compressie en om daadwerkelijk optredende pixelwaarden bij te houden.

## Pixelgegevens ##

Dit deel bevat de feitelijke pixelgegevens die zijn gecodeerd met behulp van MANIAC-entropiecodering. De pixels kunnen worden gecodeerd met behulp van interlaced of niet-interlaced codering.

### Interlaced methode ###

Bij deze methode worden zoomniveaus gedefinieerd. Zoomlevel 0 wordt gebruikt voor het volledige beeld, zoomlevel 1 wordt gebruikt voor alle even genummerde rijen, zoomlevel 2 wordt gebruikt voor alle even genummerde kolommen van zoomlevel 1. Met andere woorden, elk even genummerd zoomlevel 2k is een gedownsamplede versie van de afbeelding, op schaal 1:2^k. Zoomniveaus zijn gecodeerd van de hoogste naar de laagste.

### Niet-geïnterlinieerde methode ###

Bij deze methode begint de codering van de MANIAC-bomen onmiddellijk gevolgd door de codering van de pixels.

## Referenties ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

