{
  "date" : "2019-10-11",
  "keywords" :[ "gbr-Datei", "gbr-Dateiformat", "was ist eine gbr-Datei", "Datei", "gbr-Beispiel", "gbr-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR-Dateiformat - Gerber-Dateiformat für PCB",
  "description":"Erfahren Sie mehr über das GBR-Dateiformat und APIs, die GBR-Dateien erstellen und öffnen können.",
  "linktitle" :"GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GBR-Datei?

Eine Datei mit der Erweiterung .gbr ist ein Gerber-Bilddateiformat für den Austausch von Designdaten für Leiterplatten (PCB). Es wurde von Ucamco entwickelt. PCB-Designdaten sind die Hauptkomponente, die von der Fertigungsindustrie für die Handhabung benötigt werden. Eine GRB-Datei enthält PCB-Daten wie Kupferschichten, Lötmasken, Legenden sowie Bohr- und Leitungsdaten. Es kann verwendet werden, um Daten wie PCB-Fertigungsmerkmale, einschließlich Dicke oder Oberflächenbeschaffenheit, in einem standardisierten Format zu übertragen. Alle PCB-Designsysteme geben Gerber-Dateien aus, die von PCB-Fertigungssystemen verarbeitet werden können. GBR-Dateien sind inzwischen zum De-facto-Standard für die Datenübertragung von Leiterplattendesigns (PCB) geworden. Ucamco hat einen [kostenlosen Online-Viewer] (https://gerber-viewer.ucamco.com/) bereitgestellt, um GBR-Dateiformate zu öffnen und anzuzeigen.

## GBR-Dateiformat

GBR ist ein menschenlesbares UTF-8-Format, das aus nur 27 Befehlen besteht. Aufgrund dieser kurzen Befehlsliste und seiner Kompaktheit ist GBR einfach zu debuggen. Gerber ist im Kern ein offenes Vektorformat für binäre 2D-Bilder. Über Attribute werden Meta-Informationen mit den Bildern übertragen. Eine einzelne GRB-Datei gibt ein einzelnes Bild an und erfordert keine Interpretation begleitender Dateien oder externer Parameter. Ein Bild benötigt nur eine Datei. Es verwendet 7-Bit-ASCII-Zeichen für alle Befehle und Namen, die in der Spezifikation definiert und druckbar sind. Dies deckt die vollständige Bilderzeugung vollständig ab.

### GBR-Beispieldatei

Es folgt eine Beispiel-Gerber-Datei, die einen Kreis mit 1,5 mm Durchmesser erstellt, der auf dem Ursprung zentriert ist. Es gibt einen Befehl pro Zeile.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Verweise

* [Gerber-Format](https://www.ucamco.com/en/gerber)

