{
  "date" : "2020-01-10",
  "keywords" :[ "otg-Datei", "otg-Dateiformat", "was ist eine otg-Datei", "Datei", "otg-Beispiel", "otg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Dateiformat für OpenDocument-Zeichnungsvorlagen",
  "description":"Erfahren Sie mehr über das OTG-Dateiformat und APIs, die OTG-Dateien erstellen und öffnen können.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Was ist eine OTG-Datei?

Eine OTG-Datei ist eine Zeichnungsvorlage, die mit dem OpenDocument-Standard erstellt wird, der der OASIS Office Applications [1.0-Spezifikation](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf) folgt. Es stellt die Standardorganisation von Zeichnungselementen für ein Vektorbild dar, das verwendet werden kann, um den Inhalt der Datei weiter zu verbessern. OTF-Dateien sind wie alle anderen auf dem OpenDocument-Format basierenden Dateien, die auf dem XML-Format basieren, um den Inhalt des Dokuments darzustellen. OTF-Dateien können angezeigt werden, indem Sie sie in einem beliebigen Text- oder Standard-XML-Editor öffnen.

## OTG-Dateiformatspezifikationen ##

Das OTG-Dateiformat basiert auf dem OpenDocument-XML-Format, das über ein etabliertes Schema verfügt. Die Struktur jeder Komponente eines OpenDocument-Formats wird durch ein Element dargestellt, das zugeordnete Attribute hat und für alle Dokumenttypen wie Textdokumente, Tabellenkalkulationen oder Zeichnungsdateien gleich ist. OTG, das eine Zeichnungsvorlage ist, nutzt umfassend die Grafikinhaltsspezifikationen, die Folgendes umfassen:

* Verbesserte Seitenfunktionen für grafische Anwendungen
* Formen zeichnen
* Rahmen
* 3D-Formen
* Benutzerdefinierte Form
* Präsentationsformen
* Präsentationsanimationen
* SMIL-Präsentationsanimationen
* Präsentationsveranstaltungen
* Textfelder präsentieren
* Inhalt des Präsentationsdokuments

### Erweiterte Seitenfunktionen für grafische Anwendungen ###
#### Handout-Meister ####

Das Handout-Master-Element ist eine Vorlage zum automatischen Generieren der Handout-Seiten für Anwendungen, die das Drucken solcher Seiten unterstützen.
Die Attribute, die dem zugeordnet werden können `<style:handout-master>` Element sind:

|Layout|Attribut|Beschreibung
---|---|---|
|Layout der Präsentationsseite|presentation:name-des-präsentationsseitenlayouts|Links zu `<style:presentation-page-layout>` Attribut
|Seitenlayout|`style:page-layout-name` | Gibt ein Seitenlayout an, das die Größen, den Rahmen und die Ausrichtung der Handzettel-Musterseite enthält.
|Seitenstil|`draw:style-name`|Weist einer Handout-Musterseite zusätzliche Formatierungsattribute zu, indem ein Zeichenseitenstil zugewiesen wird.|
|Kopfdeklaration| `presentation:use-header-name`| Gibt den Namen der Kopfzeilenfelddeklaration an, die für alle Kopfzeilenfelder verwendet wird, die auf der Handzettel-Musterseite angezeigt werden.
|Fußerklärung| presentation:use-footer-name|Gibt den Namen der Fußzeilenfelddeklaration an, die für alle Fußzeilenfelder verwendet wird, die auf der Handout-Musterseite angezeigt werden.
|Datums- und Uhrzeitdeklaration|use-date-time-name|Gibt den Namen der Datums-/Uhrzeit-Felddeklaration an, die für alle Datums-/Uhrzeitfelder verwendet wird, die auf der Handout-Musterseite angezeigt werden.

### Formen zeichnen ###
Das OpenDocument-Format unterstützt mehrere Zeichnungsformen, die von jedem Dokumenttyp verwendet werden können.

|Form|Verknüpfte Attribute| Elemente
---|---|---|
Rechteck - `<draw:rect>` |Position, Größe, Stil, Ebene, Z-Index, ID, Beschriftungs-ID, Textanker, Tabellenhintergrund, Endposition des Zeichnens, runde Ecken|Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text
Zeile `<draw:line>` |Stil, Ebene, Z-Index, ID, Beschriftungs-ID und Transformation, Textanker, Tabellenhintergrund, Endposition des Zeichnens, Startpunkt, Endpunkt|Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text
Polylinie `<draw:polyline> `| Position, Größe, Ansichtsfeld, Stil, Ebene, Z-Index, ID, Beschriftungs-ID und Transformation, Textanker, Tabellenhintergrund, Endposition des Zeichnens, Punkte| Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text
Vieleck `<draw:polygon> `|Position, Größe, Ansichtsfeld, Stil, Ebene, Z-Index, ID, Beschriftungs-ID und Transformation, Textanker, Tabellenhintergrund, Endposition des Zeichnens, Punkte|Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text
|Reguläres Polygon `<draw:regular-polygon> `|Position, Größe, Stil, Ebene, Z-Index, ID, Beschriftungs-ID und Transformation, Textanker, Tabellenhintergrund, Endposition des Zeichnens, Konkav, Ecken, Schärfe|Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text
|Paht `<draw:path> `|Position, Größe, Ansichtsfeld, Stil, Ebene, Z-Index, ID, Beschriftungs-ID und Transformation, Textanker, Tabellenhintergrund, Zeichenendposition, Pfaddaten| Titel, lange Beschreibung, Ereignis-Listener, Klebepunkte, Text

### Rahmen ###
Ein Rahmen in einem Zeichnungsdokument ist ein rechteckiger Behälter, der Textfelder, Bilder oder Objekte enthält. Rahmen unterstützen zusätzliche Funktionen wie Konturen, Bildkarten und Hyperlinks. Ein Frame kann sowohl ein Objekt als auch ein Bild enthalten, wodurch mehrere Wiedergaben eines Objekts möglich sind. Die Anwendungen rendern das jeweilige Element basierend auf der besten Unterstützung.

Frames können enthalten:
* Textfelder
* Objekte, die entweder im OpenDocument-Format oder in einem objektspezifischen Binärformat dargestellt werden
* Bilder
* Applets
* Plugins
* Schwebende Rahmen

Ein Rahmen ist in einem Dokument enthalten, wie unten gezeigt.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Verweise ##
* [OASIS Open Document Format für Office-Anwendungen](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument-Format – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

