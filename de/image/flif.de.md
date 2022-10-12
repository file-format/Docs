---
date: 2020-08-12
keywords: "flif, .flif, flif-Dateiformat, wie man flif-Dateien öffnet, .flif-Erweiterung, flif-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "FLIF-Dateiformat"
linktitle: "FLIF"
description: "Erfahren Sie mehr über das FLIF-Dateiformat und APIs, die FLIF-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Was ist eine FLIF-Datei? ##

FLIF (Free Lossless Image Format) ist ein verlustfreies Bildformat, das die Erweiterung .flif für seine Dateien verwendet. FLIF behauptet, [PNG](/de/image/png/), verlustfreies [WebP](/de/image/webp/), verlustfreies BPG und verlustfreies JPEG 2000 in Bezug auf das Komprimierungsverhältnis zu übertreffen. FLIF verwendet progressives Interlacing, wodurch jeder teilweise Download des Bildes als verlustbehaftete Codierung für das gesamte Bild verwendet werden kann.

## Kurze Geschichte ##

FLIF wurde im September 2015 angekündigt und die Alpha-Version wurde im Oktober 2015 veröffentlicht. Im September 2016 wurde die erste stabile Version von FLIF veröffentlicht.

## FLIF-Design ##

FLIF verwendet eine Variante von CABAC (kontextadaptive binäre arithmetische Codierung), MANIAC (metaadaptive Near-Zero Integer Arithmetic Coding) zur Komprimierung. MANIAC ist ein Entropiecodierungsalgorithmus, der von Jon Sneyers und Pieter Wuille entwickelt wurde. Bei MANIAC sind die Kontexte Knoten von Entscheidungsbäumen, die zum Zeitpunkt der Codierung dynamisch gelernt werden. Dadurch wird das Kontextmodell bildspezifischer und führt zu einer besseren Komprimierung. FLIF hat die folgenden Funktionen:

- Unterstützt verlustfreie Komprimierung
- Unterstützt verlustbehaftete Komprimierung mit Encoder-Vorverarbeitung
- Unterstützt Graustufen, RGB und RGBA
- Unterstützt eine Farbtiefe von 1 bis 16 Bit pro Kanal
- Unterstützt Interlaced- und Non-Interlaced-Dateien
- Unterstützt die progressive Dekodierung von teilweise heruntergeladenen Dateien
- Unterstützt Animationen
- Unterstützt eingebettete ICC-Farbprofile, Exif- und XMP-Metadaten
- Hat eingeschränkte Unterstützung für die Komprimierung von Camera Raw-Dateien (RGGB)

## FLIF-Dateiformat ##

Eine FLIF-Datei besteht aus den folgenden vier Teilen:

## Hauptkopfzeile ##

Der Hauptheader enthält die wichtigsten Metadaten, einschließlich Breite, Höhe, Farbtiefe, Anzahl der Frames.

|Typ|Wert|Beschreibung|
|---|---|---|
|4 Bytes|"FLIF"|Magie|
|4 Bits|3 = ni immer noch; 4 = ich noch; 5 = ni anim; 6 = i anim|Interlacing, Animation|
|4 Bits|1 = Graustufen; 3 = RGB; 4 = RGBA|Anzahl der Kanäle (nb_channels)|
|1 Byte|'0','1','2' ('0'=benutzerdefiniert)|Bytes pro Kanal (Bpc)|
|Variante|Breite-1|Breite|
|Variante|Höhe-1|Höhe|
|variante|nb_frames-2 (nur bei Animation)|Anzahl Frames (nb_frames)|

## Metadatenblöcke ##

Dieser Teil enthält Nicht-Pixel wie Exif/XMP-Metadaten, ICC-Farbprofil usw., die mit DEFLATE-Komprimierung codiert sind. Diese Chunks sind ähnlich wie PNG-Chunks definiert, mit dem Unterschied, dass die Chuck-Größe mit einer variablen Anzahl von Bytes codiert wird. Chunk-Namen können aus 4 Buchstaben (4 Byte) oder einem Wert unter 32 bestehen, der einen nicht optionalen Chunk anzeigt.

Nachfolgend ein Beispiel für optionale Spannfutter:

|Chunk-Name|Beschreibung|Inhalt (nach DEFLATE-Dekomprimierung)|
|---|---|---|
|iCCP|ICC-Farbprofil|rohe ICC-Farbprofildaten|
|eXif|Exif-Metadaten|"Exif\0\0"-Header, gefolgt von einem TIFF-Header und den EXIF-Daten|
|eXmp|XMP-Metadaten|XMP in einem schreibgeschützten xpacket ohne Padding enthalten|

### Namenskonvention ###

- **Anfangsbuchstabe**: Großbuchstaben werden für kritische und Kleinbuchstaben für nicht kritische Blöcke verwendet.
- **Second Letter**: Großbuchstaben werden für öffentliche und Kleinbuchstaben für private Chunks verwendet
- **Dritter Buchstabe**: Großbuchstaben werden für Chucks verwendet, die zur korrekten Anzeige des Bildes benötigt werden, und Kleinbuchstaben sind für die Anzeige des Bildes nicht wichtig.
- **Vierter Buchstabe**: Großbuchstaben werden für Spannfutter verwendet, die sicher blind kopiert werden können. Kleinbuchstaben sind abhängig von den Bilddaten.

## Zweite Kopfzeile ##

Diese enthält die Information über die tatsächliche Codierung der Pixel.

|Typ|Beschreibung|Bedingung|Standardwert|
|---|---|---|---|
|1 Byte|NUL-Byte (0x00), Chunk-Name eines FLIF16-Bitstroms||
|uni_int(1,16)|Bits pro Pixel der Kanäle|Bpc == '0': repeat(nb_channels)|8 wenn Bpc == '1', 16 wenn Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Anzahl Schleifen|nb_frames > 1||
|uni_int(0,60_000)|Rahmenverzögerung in ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flag: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|Alpha-Teiler|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Flag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|Variable|Transformationen (siehe unten)|||
|uni_int(1) = 0|Indikatorbit: fertig mit Transformationen|||
|uni_int(0,2)|Vorhersage für unsichtbare Pixel|alpha_zero && Interlaced && Alpha-Bereich umfasst Null||

**Kanäle**

|Kanalnummer|Beschreibung|
|---|----|
|0|Rot oder Grau|
|1|Grün|
|2|Blau|
|3|Alpha|

**Transformationen**

|Typ|Beschreibung|
|---|---|
|uni_int(1) = 1|Indikatorbit: noch nicht fertig|
|uni_int(0,13)|Umwandlungskennzeichen|
|Variable|Transformationsdaten (abhängig von der Transformation)|

Transformation wird verwendet, um Pixeldaten für eine bessere Komprimierung zu modifizieren und tatsächlich auftretende Pixelwerte zu verfolgen.

## Pixeldaten ##

Dieser Teil enthält die tatsächlichen Pixeldaten, die unter Verwendung der MANIAC-Entropiecodierung codiert sind. Die Pixel können unter Verwendung von Zeilensprung- oder Nicht-Zeilensprung-Codierung codiert werden.

### Interlaced-Methode ###

Bei dieser Methode werden Zoomstufen definiert. Zoomlevel 0 wird für das Vollbild verwendet, Zoomlevel 1 wird für alle geradzahligen Zeilen verwendet, Zoomlevel 2 wird für alle geradzahligen Spalten von Zoomlevel 1 verwendet. Mit anderen Worten, jeder geradzahlige Zoomlevel 2k ist eine heruntergesampelte Version des Bild im Maßstab 1:2^k. Zoomstufen werden vom höchsten zum niedrigsten kodiert.

### Methode ohne Zeilensprung ###

Bei diesem Verfahren beginnt die Codierung der MANIAC-Bäume unmittelbar gefolgt von der Codierung der Pixel.

## Verweise ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

