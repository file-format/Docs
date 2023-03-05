{
  "date" : "2021-01-21",
  "keywords" :[ "ai-Datei", "ai-Dateiformat", "was ist eine ai-Datei", "Datei", "ai-Beispiel", "ai-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator-Artwork-Datei",
  "description":"Erfahren Sie mehr über das AI-Dateiformat und APIs, die AI-Dateien erstellen und öffnen können.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Was ist eine AI-Datei?

Eine Datei mit der Erweiterung .ai ist eine Adobe Illustrator-Artwork-Datei, die Vektorgrafiken auf einer einzelnen Seite enthält. Es verwendet Punkte, um Pfade für die Anzeige der Bilddaten zu erstellen, und schützt so vor einem Verlust der Bildqualität, wenn es vergrößert wird. Das AI-Dateiformat basiert auf dem PGF-Dateiformat, das AI-Dateien ähnelt. Das AI-Format wird hauptsächlich für Logos und Printmedien verwendet, und seine anfänglichen Versionen wurden als ähnlich denen von [EPS](/de/image/eps/)-Dateien angesehen. AI-Dateien können mit den Grafikwerkzeugen Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro und CorelDraw geöffnet werden.

## AI-Dateiformat

AI ist das proprietäre Dateiformat von Adobe Illustrator und verwendet den dualen Pfadansatz ähnlich wie PGF zum Speichern von EPS-kompatiblen Dateien. Die [Adobe Illustrator-Dateiformatspezifikationen](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) enthalten detaillierte Informationen Entwickler-Referenz für interne Details dieses Dateiformats. Alle von Adobe Illustrator erstellten Dokumente (Dateien) sind Dokumente in PostScript-Sprache und bestehen aus zwei Hauptteilen, die den Dokumentstrukturierungskonventionen entsprechen: einem „Prolog“ und einem „Skript“.

### Prolog

Der Prolog-Abschnitt kapselt Informationen ein, die für die Interpretation der Datei erforderlich sind. Ein Beispiel wäre der Begrenzungsrahmen, der alle Markierungen auf der Seite enthält. Es enthält auch Ressourceninformationen wie Schriftarten und Prozedurdefinitionen. Diese Ressourcen sind logisch in Gruppen gruppiert, die Procsets genannt werden, und enthalten explizite Methoden zum Initialisieren und Beenden ihrer Prozeduren.

### Skript

Grafische Elemente auf der Seite werden durch das Skript beschrieben. Ein Skript enthält Verweise auf die Operatoren und Prozeduren im Prolog zusammen mit Operanden und Daten. Die drei logischen Abschnitte eines Skripts umfassen:

* Setup-Sequenz - die die im Prolog definierten Ressourcen initialisiert und aktiviert
* Folge beschreibender Operatoren
* Trailer, der Ressourcen deaktiviert

Operatoren im Skript sind Sequenzen von grafischen Elementen, die in der Sprache geschrieben sind, die durch procsets im Prolog definiert ist. Diese Sequenzen bestehen aus Sammlungen von Datenelementen, Grafikattributdefinitionen und Aufrufen der in den Procsets definierten Prozeduren.

### Objekt-Tags

Objekt-Tags werden verwendet, um benutzerdefinierte Informationen an ein Adobe Illustrator-Kunstobjekt anzuhängen. Tags bestehen aus:

* Tag-Kennung
* Tag-Typ
* Daten

## Verweise
* [Adobe Illustrator-Dateiformatspezifikationen](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI-Dateiformat von PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

