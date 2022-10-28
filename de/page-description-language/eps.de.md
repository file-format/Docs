{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "Datei", "Erweiterung", "Dateiformat", "Seitenlayout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das EPS-Dateiformat und APIs, die EPS-Dateien erstellen und öffnen können.",
  "title" :"EPS-Dateiformat - Encapsulated PostScript-Datei",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine EPS-Datei?

Eine .eps-Datei ist eine Bilddatei, die im Encapsulated Postscript-Dateiformat auf einer Disc gespeichert wird. Es kann eine beliebige Kombination aus Text, Grafiken und Bildern enthalten. EPS-Dateien können auch ein eingekapseltes Bitmap-Vorschaubild enthalten, das von Anwendungen angezeigt werden kann, die solche Dateien öffnen können.

## Kurze Geschichte des EPS-Dateiformats

Ein kurzer Blick auf das EPS-Dateiformat aus der Verlaufsperspektive zeigt die folgenden Informationen:

* Die erste Version von EPS wurde irgendwann zwischen 1985 und 1988 von Adobe veröffentlicht
* Version 2.0 der EPS-Spezifikation wurde im Januar 1989 veröffentlicht
* Die Spezifikation für Version 3.0 von EPS wurde 1992 als separates Dokument veröffentlicht; Dies ist die neueste veröffentlichte Version.

EPS bildete in Kombination mit dem Erweiterungsmechanismus Open Structuring Conventions, der in Abschnitt 9 der Spezifikation der PostScript Language Document Structuring Conventions von Adobe beschrieben ist, die Grundlage früher Versionen des Adobe Illustrator Artwork-Dateiformats.

## EPS-Dateiformat

EPS ist ein proprietäres, aber öffentlich dokumentiertes Format, und die Spezifikationen des EPS-Dateiformats sind öffentlich als Referenz für Entwickler verfügbar. EPS ist ein [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) konformes Dateiformat und hält sich an alle von der DSC aufgestellten Regeln. Das DSC ist ein spezielles Dateiformat für PostScript-Dokumente von Adobe. Jede Anwendung, die behauptet, EPS-Dateien lesen zu können, sollte DSC-kompatibel sein.

Eine EPS-Datei besteht aus zwei Hauptabschnitten, wie unten erläutert.

### Vorschaubild ###

Eine typische EPS-Datei enthält ein Vorschaubild in einem Format, das zur bequemen Verwendung in einem Arbeitsablauf vorgesehen ist, an dem mehrere Systeme oder Anwendungen beteiligt sind. Die Absicht einer Vorschau besteht darin, ein Bild in einem Format zu haben, das die meisten Grafikanwendungen rendern können; eine Vorschau hat normalerweise eine niedrigere Auflösung, in Pixelabmessungen und/oder in Bittiefe. Die Vorschaudatei kann in einem von mehreren Formaten vorliegen. Die Spezifikation für EPS_3 listet drei "gerätespezifische" Vorschauformate auf:

* für den Apple Macintosh ein PICT-Bild, wie es von der QuickDraw-Anwendung verwendet wird
* für DOS-Computer eine TIFF-Bitmap
* Windows-Metadatei.

PICT und Windows Metafile können sowohl Bitmap-Daten als auch Vektorgrafiken enthalten. Darüber hinaus definiert die Spezifikation eine sehr einfache geräteunabhängige Darstellung für ein eingebettetes Bitmap-Vorschaubild. Diese Darstellung ist als Encapsulated PostScript Interchange Format (EPSI) bekannt.

Eine EPSI-Vorschau ist eine als ASCII-Hexadezimal dargestellte Bitmap, die zur Identifizierung zwischen einige PostScript-Kommentare gewickelt ist und einfach und leicht zu transportieren ist. Um EPS-Dateien mit unterschiedlichen Vorschauformaten zu unterscheiden, wurden in der EPS-Spezifikation unterschiedliche DOS-Dateierweiterungen und Macintosh-Dateitypen empfohlen.

### PostScript-Code

Das EPS-Dateiformat muss mindestens Folgendes enthalten:

* ein Header-Kommentar, %!PS-Adobe-3.0 EPSF-3.0
* und einen Begrenzungsrahmenkommentar, %%BoundingBox: llx lly urx ury, der die Grenzen der Illustration beschreibt. Diese vier Argumente entsprechen den unteren linken (llx, lly) und oberen rechten (urx, ury) Ecken des Begrenzungsrahmens.

Eine EPS-Datei kann keinen der folgenden Operatoren verwenden:

* Bandgerät,
* cleardictstack
* Kopierseite
* Löschseite
* Ausgangsserver
* Rahmengerät
* grestoreall
* initclip
* Initgrafiken
* Initmatrix
* Verlassen
* Renderbänder
* setglobal
* setpagedevice
* Satz geteilt
* Startjob.

## Konvertierung von EPS in andere Dateiformate

EPS-Dateien können in Standardbildformate wie [JPG](/de/image/jpeg/), [PNG](/de/image/png/), [TIFF](/de/image/tiff/) und [PDF](/de/pdf /) mit verschiedenen Anwendungen, zB Adobe Illustrator, Photoshop und PaintShop Pro.

Aufgrund einer [Sicherheitslücke](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) in EPS-Dateien haben Office 2016, Office 2013, Office 2010 und Office 365 die Möglichkeit zum Einfügen von EPS-Dateien in Office-Dokumente deaktiviert.

## Verweise

* [Encapsulated PostScript – von Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

