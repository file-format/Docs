{
  "date" : "2020-03-16",
  "keywords" :[ "IGES-Datei", "Dateiformat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das IGES-Dateiformat und APIs, die IGES-Dateien erstellen und öffnen können.",
  "title" :"IGES-Dateiformat",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Was ist eine IGES-Datei?

Eine Datei mit der Erweiterung .iges wird verwendet, um Designinformationen zwischen CAD-Anwendungen (Computer Aided Design) auszutauschen. IGES steht für Initial Graphics Exchange Specifications. Informationen, die mit IGES ausgetauscht werden, umfassen Schaltplan-, Drahtmodell-, Freiformflächen- oder Volumenmodelldarstellungen. IGES findet seine Anwendungen in traditionellen Konstruktionszeichnungen, Modellanalysen und Fertigungsfunktionen. Das Format kann sowohl 2D- als auch 3D-Konstruktionsinformationen zwischen CAD-Programmen austauschen. IGES-Dateien können mit mehreren CAD-Anwendungen wie Autodesk und CADSoftTools ABViewer geöffnet werden. Es stehen auch mehrere APIs zum programmatischen Öffnen und Konvertieren von IGES-Dateien zur Verfügung.

## IGES-Dateiformat

IGES-Dateien sind im ASCII-Textformat und können in jedem Texteditor geöffnet werden, um den Inhalt der Datei anzuzeigen. Textinformationen in einer IGES-Datei werden im "Hollerith"-Format dargestellt. Eine gewöhnliche IGES-Datei kann Tausende von Zeilen enthalten, um die 2D- oder 3D-Informationen darzustellen, die gemäß diesem Format ausgetauscht werden können. Eine IGES-Datei ist in fünf Abschnitte unterteilt, die durch den jeweiligen Großbuchstaben in der 73. Spalte gekennzeichnet sind. Diese Abschnitte sind die Abschnitte „Start“ (S), „Global“ (G), „Dateneingabe“ (D), „Parameterdaten“ (P) und „Beenden“ (T). Die Abschnitte Data Entry und Parameter Data werden allgemein mit DE bzw. PD abgekürzt.

### Kopfzeile der IGES-Datei

Die Abschnitte Start und Global enthalten grundlegende Informationen über:
* Name der Datei und ihrer Quelle
* Trennzeichen für den Parameterdatenabschnitt
* Autor der Datei und andere allgemeine Informationen.

Die Abschnitte „Start“ und „Global“ aus dem Beispieldokument auf Wikipedia lauten wie folgt.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Wie zu sehen ist, enthält das Startfeld menschenlesbare Beschreibungen der Datei, und es können beliebige Zeichen in den Spalten 1–72 vorhanden sein, wobei die Zeile mit dem Abschnittskopf und der Abschnittszeilennummer endet. Es muss mindestens 1 Zeile des Abschnitts Start vorhanden sein. Der globale Abschnitt enthält Präprozessordaten. Es muss auch in der Datei vorhanden sein und mit dem Format G000000# enden.

### Abschnitt Dateneingabe (DE) und Parameterdaten (PD).

#### Abschnitt zur Dateneingabe
Eine IGES-Datei besteht aus mehreren Entitäten, die die Informationen zu den Grunddaten des IGES-Dateiformats enthalten. Eine Entität enthält Informationen über verschiedene Elemente eines IGES-Datenformats und wird zum Zeichnen verwendet. Zu den häufiger verwendeten Entitäten gehören:
* Kreisbogen
* Zusammengesetzte Kurve
* Kegelbogen
* Ebene
* Linie

Dies sind nur einige wenige und es gibt rund 150 verschiedene Entitäten in IGES. Jede Entität wird durch eine Typennummer identifiziert, wie z. B.:
* KREISBOGEN (Typ 100)
* LINIE (Typ 110)

##### Entitätseigenschaften

Jede deklarierte Entität hat die folgenden Eigenschaften.

|Feldname|Beschreibung|
---|---|
|Entitätstyp |Dies ist der Typ der beschriebenen Entität. Beispielsweise beschreibt 116 eine Point-Entität.|
|PD-Zeiger |Dies gibt den Ort für diese Entitätsdaten im Parameterdatenabschnitt an. Diese Position ist einfach die Zeilennummer innerhalb des PD-Abschnitts, der die erste Zeile dieser Entitätsdaten enthält.|
|Struktur |Null oder Zeiger auf Definitionsentität. Gilt nicht für die meisten Unternehmen|
|Linienschriftmuster| Nummer oder Zeiger auf Linienschriftmusterentität. Zahl bedeutet: * 0 Kein Muster angegeben (Standard) * 1 Fest * 2 Gestrichelt * 3 Phantom * 4 Mittellinie * 5 Gepunktet|
|Ebene| Gibt Ebenen an, die dieser Entität zugeordnet werden sollen. Ermöglicht das Erscheinen einer Entität auf mehr als einer Ebene|
|Ansicht| Gibt Anzeigeoptionen an. Diese sind: 0 Zeigt gleiche Sichtbarkeit und Eigenschaften in allen Ansichten an. Standardzeiger auf die Ansichtsentität (Typ 410), von der aus es angezeigt werden kann. Verweis auf eine Ansichtssichtbare Assoziativitätsentität (Typ 402, Form 3)
|Transformationsmatrixzeiger| Verweist auf eine Transformationsmatrixentität (Typ 124) oder ist standardmäßig null (keine Transformation)|
|Beschriftungsanzeige-Assoziativität| Verweist auf eine Beschriftungsanzeigeassoziativität (Typ 402, Form 5), die definiert, wie die Entitätsbeschriftung angezeigt wird.|
|Statusnummer| Enthält vier Abschnitte mit zwei Zahlen. 1-2: Leerstatus. Entweder 00 für normal oder 01 für ausgeblendet. 3-4: Untergeordneter Einheitsschalter: ist 00 für unabhängig, 01 für physisch abhängig, 02 für logisch abhängig und 03 für beide. 5-6: Entity Use Flag: ist entweder 00 für Geometrie, 01 für Anmerkung, 02 für Definition, 03 für Sonstiges, 04 für Logisch, 05 für 2D-Parametrik und 06 für Konstruktionsgeometrie. Schließlich ist 7-8 die Hierarchie, wobei 00 global von oben nach unten angibt (Eigenschaften dieser Entität verwenden), 01 global zurückstellen (Eigenschaften dieser Entität nicht verwenden) und 02 Hierarchieeigenschaft verwenden (Hierarchieentität verwenden (Typ 406, Form 10) Merkmale der hierarchischen Gruppierung zu bestimmen).|
|Sequenznummer| Angegeben durch D#, wobei # die Zeilennummer für diesen Abschnitt ist (nicht vom Anfang der Datei). Dies wird auch verwendet, um auf diese Dateneingabeeinheit zu verweisen.|
|Entitätstyp| es wird zweimal pro Entitätsliste angegeben|
|Linienstärkennummer| Gibt die Dicke beim Anzeigen von Objekten an. Kleinste ist 1, 0 ist Standard|
|Farbnummer| Gibt die Objektfarbe an. Zulässige ganzzahlige Werte sind: 0 Keine Farbe (Standard) 1 Schwarz 2 Rot 3 Grün 4 Blau 5 Gelb 6 Magenta 7 Cyan 8 Weiß|
|Anzahl der Parameterzeilen| Gibt die Anzahl der Zeilen an, die diese Entität im Parameterdatenabschnitt einnimmt|
|Formularnummer| Gibt die Form oder die Darstellung dieser Entität an. Ändert die Interpretation der Parameterdaten. Standard ist 0|
|Reserviertes Feld| Nicht verwendet|
|Reserviertes Feld| Nicht verwendet|
|Entitätsbezeichnung| Von der Anwendung angegebener Bezeichner - rechtsbündig |
|Subskriptionsnummer| Numerischer Qualifizierer für die Entitätsbezeichnung. Beide zusammen bilden eine eindeutige Kennung für die Entität|
|Sequenznummer Siehe oben. |Dies wird D#+1 sein, da jede Entität in zwei Zeilen angegeben wird.|

#### Abschnitt Parameterdaten
Auf den Abschnitt „Dateneinträge“ folgt der Abschnitt „Parameterdaten“. Es listet die Daten für jeden jeweiligen Eintrag auf und listet Parameter für die Entität auf, basierend auf den Trennzeichen, die im globalen Abschnitt angegeben sind (normalerweise Kommas, um Parameter zu trennen, und ein Semikolon, um die Auflistung zu beenden).


## Verweise
* [IGES von WikiPedia](https://en.wikipedia.org/wiki/IGES)

