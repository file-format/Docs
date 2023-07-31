{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Berichtsseitenlayout",
  "keywords" :[ "rpl", "Berichtsseitenlayout", "XSD", "SQL Server", "Berichterstellung"],
  "description":"Erfahren Sie mehr über das RPL-Stream-Format, ein internes Binärformat, das von Microsoft SQL Server Reporting Services beim Kontakt mit Viewer-Steuerelementen verwendet wird.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Was ist eine RPL-Datei? ##

Das Stream-Format RPL (Report Page Layout) ist ein internes Binärformat, das von MS SQL Server Reporting Services beim Kontakt mit Viewer-Steuerelementen verwendet wird, um einen Teil der Renderarbeit vom Server zum Client-Viewer-Steuerelement zu reduzieren. Entwickler können mithilfe von RPL benutzerdefinierte Berichtsdesigner erstellen, die RPL generieren, sowie benutzerdefinierte Berichtsrenderer, die die RPL-Datei verarbeiten und anzeigen, um Berichte anzuzeigen.

## RPL-Strukturen

Ein RPL-Stream umfasst Stream-Struktur, Berichtsstruktur, Berichtseigenschaften und Aufzählungen. Jede Struktur umfasst Folgendes:

- Eine Definition der Struktur.

- Die Grammatik der erweiterten Backus-Naur-Form (ABNF) für die Struktur.

- Ein Bitdiagramm der Struktur.

- Definitionen aller in der Struktur enthaltenen Felder.

Hier sind die kurzen Anmerkungen zu einigen der RPL-Strukturen:

### Stream-Struktur
Die Stream-Struktur besteht aus einer Reihe von Datensätzen. Ein Datensatz enthält null oder mehr strukturierte Felder, die das Berichtslayout enthalten.

#### RPL-Stream
Der RPL-Stream darf nur einen Berichtsdatensatz haben und der Stream muss aus einer Reihe von binären Datensätzen bestehen, die die Berichtshierarchie beibehalten.

#### Aufzeichnung
Der Datensatz ist ein grundlegender Baustein, der verwendet wird, um die Informationen zu einem Bericht aufzubewahren. Ein Datensatz besteht aus einer Folge von Bytes unterschiedlicher Länge. Ein Datensatz besteht aus zwei Komponenten:
- Ein Datensatztyp
- Die Datensatzdaten, die für diesen Datensatztyp spezifisch sind.
Der Datensatztyp ist ein Byte, das definiert, welcher Informationstyp durch den Datensatz spezifiziert wird und wie die Struktur der Datensatzdaten bezüglich des Datensatzes geordnet und strukturiert ist. Der Datensatzwert hängt von der Art der Daten ab, die für diesen Datensatz spezifisch sind.

#### Einfache Datentypstrukturen

Die folgende Tabelle definiert die Datentypen in einem RPL-Stream.

|Beschreibung| formatieren|
---|---|
|Char|Repräsentiert einen 16-Bit (2-Byte) numerischen (ordinalen) Wert.|
|Byte|Repräsentiert eine 8-Bit (1-Byte) Ganzzahl ohne Vorzeichen.|
|Int16|Repräsentiert eine vorzeichenbehaftete 16-Bit (2-Byte) Ganzzahl.|
|Single|Repräsentiert einen 32-Bit (4-Byte) Gleitkommawert mit einfacher Genauigkeit.|
|Dezimal|Repräsentiert einen 128-Bit (16-Byte) Datentyp.|
|DateTime|Repräsentiert eine 64-Bit (8-Byte)-Codierung eines Datums- und Uhrzeitwerts.|
|Int64|Repräsentiert eine vorzeichenbehaftete 64-Bit (8-Byte) Ganzzahl.|
|Int32|Repräsentiert eine vorzeichenbehaftete 32-Bit (4-Byte) Ganzzahl.|
|Float|Repräsentiert einen 32-Bit (4-Byte) Gleitkommawert mit einfacher Genauigkeit.|
|Boolean|Repräsentiert einen logischen Wert vom Typ Boolean mit 8 Bit (1 Byte). Die gültigen Werte sind wahr (1) und falsch (0).|
|Long|Repräsentiert eine vorzeichenbehaftete 64-Bit (8-Byte) Ganzzahl.|
|String|Alle String-Werte innerhalb des Protokolls MÜSSEN UNICODE UTF-16 sein. Standardmäßig beginnen alle String-Werte mit einer Ganzzahl, die die Länge des Strings definiert. Zeichenfolgenwerte werden im Protokoll als Array von Bytes dargestellt; die Anzahl der Bytes MUSS gleich der Anzahl der Zeichen im String multipliziert mit zwei sein.|

### Berichtsstrukturen
Die Berichtsstrukturen umfassen die Definitionen und Größen ihrer relevanten Strukturen und Elemente.

Die folgende Liste gibt die Berichtsstrukturen an:

- Bericht
- Ausführung
- Berichtseigenschaften
- Offset-Array-Element
- Seiteninhalt
- Buchseite
- Seiteneigenschaften
- Seitenlayout
- Abschnitt
- Einfacher Abschnitt
- Gemischte Sektion
- Abschnittseigenschaften
- Körperbereichselement
- Seitenkopfelement
- Seitenfußelement
- Körperelement
- Elementeigenschaften
- Gemeinsame Elementeigenschaften
- Gemeinsam genutzte Elementeigenschaften verwenden
- InlineSharedElementProperties
- NonSharedElementProperties
- Stil
- SharedStyleProperties
- NonSharedStyleProperties
- Aktionsinfo
- ActionInfoContent
- Aktion
- ActionImageMapBereiche
- ActionInfoWithMaps
- Dynamische Bilddaten
- ImageConsolidationOffsets
- Artikel melden
- Linie
- Bild
- Bilddateneigenschaften
- UseSharedImageDataProperties
-InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Bilddaten
- ImageMapAreas
- ImageMapArea
- Diagramm
- GaugePanel
- Karte
- Rechteck
- Unterbericht
-RichTextBox
- Absatzinhalt
-TextRun
- Absatz
-RichTextBoxStructure
- Tablix
- TablixInhalt
- TablixStruktur
- TablixMaße
- Spaltenbreiten
- Spalteninfo
- Zeilenhöhen
- Zeileninfo
- TablixRow
- TablixRowCell
- TablixEcke
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMitgliederDef
- TablixMemberDef
- Messungen
- Messung
- BerichtElementEnde

### Eigenschaften
Es folgt die Liste der Eigenschaften, die in einem RPL-Stream verwendet werden können:

- ICH WÜRDE
- Spaltenanzahl
- Spaltenabstand
- Einzigartiger Name
- Name
- Etikett
- Lesezeichen
- QuickInfo
- ToggleItem
- Beschreibung
- Ort
- ConsumeContainerWhiteSpace (RPL 10.6)
- Sprache
- Ausführungszeit
- Autor
- Automatische Aktualisierung
- Berichtsname
- Seitenhöhe
- Seitenbreite
-RandOben
- RandLinks
- Randrechts
- Rand unten
- Säulen
- Seitenname (RPL 10.6)
- Schräg
- Kann wachsen
- CanShrink
- Wert
- ToggleState
- CanSort
- SortState
- Formel
- IsToggleParent
- Typschlüssel
- Originalwert
- Ist einfach
- ContentOffset
- StreamName
- Dimensionierung
- LinkToChild
- AufErsterSeite drucken
- Zwischen Abschnitten drucken (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Bildname
- Breite
- Höhe
- Horizontale Auflösung
- Vertikale Auflösung
- RawFormat
- Hyperlinks
- LesezeichenLink
- Drillthrough-ID
- Drillthrough-URL
- Randfarbe
-RandfarbeLinks
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
-BorderStyleLinks
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Rahmenbreite
- BorderBreiteLinks
-RandbreiteRechts
- BorderWidthTop
- Rahmenbreiteunten
- PolsterungLinks
- PaddingRight
- PolsterungOberseite
- PolsterungBoden
- Schriftstil
- Schriftfamilie
- Schriftgröße
- Schriftstärke
- Format
- TextDekoration
- Textausrichtung
- Vertikal ausrichten
- Farbe
- Zeilenhöhe
- Richtung
- Schreibmodus
- UnicodeBiDi
- Hintergrundbild
- Hintergrundfarbe
- Hintergrund Wiederholung
- NumeraleSprache
- NumeralVariant
- Kalender
- Spaltenkopfzeilen
- Zeilenkopfspalten
- ColsBeforeRowHeader
- LayoutDirection
- Definitionspfad
- Eben
- MemberCellIndex
-CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- Spaltenindex
- Zeilenindex
- Gruppenlabel
- RekursiveToggleLevel
- Listenstil
- Listenebene
- Absatznummer
- Rechter Einzug
- Linker Einzug
- Hängender Einzug
- Leerzeichen davor
- LeerzeichenDanach
- Erste Linie
- Auszeichnung
- InhaltTop
- InhaltLinks
- Inhaltsbreite
- Inhaltshöhe
- Bundesland
- CellItemState
- MemberDefState

### Aufzählungen
Die folgende Liste zeigt die Aufzählungen, die im RPL-Stream verwendet werden können:

- Sortieroptionen
- Größen
- ShapeType
- ImageRawFormat
- Schriftstile
- FontWeights
- TextDekorationen
- Textausrichtungen
- Vertikale Ausrichtungen
- Richtungen
- Schreibmodi
- UnicodeBiDiTypes
- Kalender
- BorderStyles
- BackgroundRepeatTypes
- Listenstile
- MarkupStyles
- Typschlüssel
- Zustandswerte
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize





## Verweise ##

- [Berichtsseitenlayout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

