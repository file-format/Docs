---
date: 2019-10-11
keywords: "prc, .prc, prc-Dateiformat, wie man prc-Dateien öffnet, .prc-Erweiterung, prc-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "PRC-Dateiformat"
linktitle: "PRC"
description: "Erfahren Sie mehr über das PRC-Dateiformat und APIs, die PRC-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Die PRC-Dateiformate
Die „.prc“-Erweiterungen werden für das Product Representation Compact 3D-Dateiformat und ein E-Book-Dateiformat von MobiPocket verwendet.

## Was ist eine Product Representation Compact (PRC)-Datei?

PRC (Product Representation Compact) ist ein 3D-Dateiformat, das zum Speichern, Laden und Anzeigen von 3D-Daten optimiert ist, insbesondere aus CAD-Systemen (Computer-Aided Design). Es ist eine sequentielle Binärdatei, die portabel geschrieben ist. PRC kann verwendet werden, um 3D-Daten in eine PDF-Datei einzubetten. PRC unterstützt die meisten Hauptkonstrukte von CAD wie Baugruppen und Teile, Bäume von 3D-Elementen, exakte Geometriedarstellung, triangulierte Darstellung und Markup. PRC verwendet die Erweiterung .prc und der verwendete Internetmedientyp ist *model/prc*.

PRC ist ein Mehrzweck-Dateiformat, das je nach Verwendung entweder mit normaler Komprimierung gespeichert werden kann, um CAD-Daten direkt darzustellen, oder mit hoher Komprimierung gespeichert werden kann, um die Dateigröße zu reduzieren. Die in einem PDF im PRC-Format gespeicherten 3D-Daten sind mit CAM- und CAE-Anwendungen interoperabel.

### Spezifikation des Dateiformats Product Representation Compact (PRC).

Eine PRC-Datei hat einen Hauptheaderabschnitt, gefolgt von einer oder mehreren Dateistrukturen, gefolgt von einer Modelldatei am Ende. Eine Dateistruktur hat einen Header, gefolgt von den folgenden Datenabschnitten:

- **Globals**: Enthält die referenzierten Dateistrukturen und Farben, Linienstile und Koordinatensysteme für jede Baumeinheit der Dateistruktur.
- **Baum**: Enthält eine Beschreibung des Baums von Elementen wie Produktvorkommen, Teiledefinitionen, Repräsentationselementen und Markup.
- **Tessellation**: Enthält alle tessellierten (triangulierten) Daten in den Blattelementen des Baums (Repräsentationselemente und Markups).
- **Geometrie**: Enthält alle exakten Geometrie- und Topologiedaten der Blattelemente des Baums (Repräsentationselemente).
- **Zusätzliche Geometrie**: Enthält die zusammenfassenden Daten der Geometrie. Dadurch kann die Datei teilweise geladen werden, ohne die gesamte Geometrie zu laden.

Das Folgende ist die Struktur einer typischen PRC-Datei.

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
## Was ist eine MobiPocket-E-Book-Datei mit der Erweiterung PRC
Ein E-Book-Dateiformat, das von einer französischen Firma namens **Mobipocket** eingeführt wird, verwendet ebenfalls die Erweiterung ".prc". Zunächst startete Mobipocket eine kostenlose Anwendung für mehrere intelligente Geräte wie Tablet-PCs, PDAs und Smartphones. Die Erweiterung ".prc" ist eigentlich identisch mit .mobi, wird aber besonders für PDAs verwendet, die nur die Erweiterungen **.prc** oder **.pdb** unterstützen.

### Mobipocket PRC-Dateiformatspezifikationen
Das MobiPocket PRC-Dateiformat basiert auf dem Open eBook-Standard unter Verwendung von XHTML und kann auch JavaScript und Frames enthalten. Unterstützung für native SQL-Abfragen zur Verwendung mit eingebetteten Datenbanken ist ebenfalls verfügbar.

Der Mobipocket Reader hat eine Homepage-Bibliothek. Leser können leere Seiten in jeden Teil eines Buches einfügen und variable Zeichnungen hinzufügen. Die Objekte wie Anmerkungen, Lesezeichen, Korrekturen, Notizen und Zeichnungen können von einem einzigen Ort aus verwaltet werden. Bilder werden in das GIF-Format konvertiert und haben eine maximale Größe von 64 KB, was für Mobiltelefone mit kleinen Bildschirmen ausreichend ist. Mobipocket Reader hat die elektronischen Lesezeichen und ein eingebautes Wörterbuch.

Der Reader verfügt über einen Vollbildmodus zum Lesen und unterstützt viele PDAs, Communicators und Smartphones. Die Mobipocket-Produkte unterstützen die meisten Palm-Betriebssysteme, Windows, Symbian, BlackBerry, aber nicht Android. Der Reader funktioniert unter Linux oder Mac OS X mit WINE.

## Verweise

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC-Formatspezifikation] (https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Vergleich von E-Book-Formaten - Von Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

