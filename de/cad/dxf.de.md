{
  "date" : "2020-03-16",
  "keywords" :[ "DXF-Datei", "Dateiformat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DXF-Dateiformat und APIs, die DXF-Dateien erstellen und öffnen können.",
  "title" :"DXF-Dateiformat",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DXF-Datei?

DXF, Drawing Interchange Format oder Drawing Exchange Format, ist eine getaggte Datendarstellung der AutoCAD-Zeichnungsdatei. Jedes Element in der Datei hat eine Präfix-Ganzzahl, die als Gruppencode bezeichnet wird. Dieser Gruppencode stellt tatsächlich das folgende Element dar und gibt die Bedeutung eines Datenelements für einen bestimmten Objekttyp an. DXF ermöglicht es, nahezu alle benutzerspezifischen Informationen in einer Zeichnungsdatei darzustellen.

Das DXF-Dateiformat wurde von Autodesk als CAD-Datendateiformat für die Dateninteroperabilität zwischen AutoCAD und anderen Anwendungen entwickelt. Somit können Daten gemäß den Interoperabilitätsspezifikationen für DXF-Dateiformate aus anderen Formaten in DXF in AutoCAD importiert werden.

## Kurze Geschichte ##


Die Geschichte des DXF-Dateiformats reicht bis ins Jahr 1982 zurück, als es als Teil von AutoCAD 1.0 eingeführt wurde. Erste Versionen von AutoCAD unterstützen nur das ASCII-Dateiformat DXF. Mit der Version 10 von AutoCAD (und höher) im Jahr 1988 wurde in AutoCAD die Unterstützung sowohl für das ASCII- als auch für das binäre DXF-Dateiformat eingeführt. In den früheren Stadien teilte Autodesk keine Dateiformatspezifikationen mit und aus diesem Grund war der korrekte Import von DXF-Dateien nicht einfach. Allerdings veröffentlicht Autodesk jetzt die DXF-Spezifikationen und steht der Öffentlichkeit zur Verfügung.

## Dateiformatspezifikationen ##

Das DXF-Dateiformat verwendet den Gruppencode und die Wertepaare, um den Inhalt in Abschnitte einzuteilen. Jeder Abschnitt besteht aus Datensätzen, wobei jeder Datensatz aus einem Gruppencode und einem Datenelement besteht. Jeder Gruppencode und -wert befindet sich in einer eigenen Zeile in der DXF-Datei. Jeder Abschnitt beginnt mit einem Gruppencode 0, gefolgt von der Zeichenfolge ABSCHNITT. Darauf folgt ein Gruppencode 2 und eine Zeichenfolge, die den Namen des Abschnitts angibt (z. B. ABSCHNITT1). Jeder Abschnitt besteht aus Gruppencodes und Werten, die seine Elemente definieren. Ein Abschnitt endet mit einer 0, gefolgt von der Zeichenfolge ENDSEC.

Das DXF-Dateiformat berücksichtigt Objekte, die sich von Entitäten unterscheiden. Objekte haben hier keine grafische Darstellung, aber Entitäten haben sie. Daher werden Einträge in DXF als grafische Objekte bezeichnet, während Objekte als nicht-grafische Objekte bezeichnet werden. Die Abschnitte BLOCK und ENTITIES der DXF-Datei enthalten Entitäten und die Verwendung von Gruppencodes in diesen beiden Abschnitten ist identisch. Das Ende einer Entität wird durch die nächste 0-Gruppe angezeigt, die die nächste Entität beginnt oder das Ende des Abschnitts anzeigt.

### Dateistruktur ###

Abschnitte in einer DXF-Datei sind in der folgenden Reihenfolge angeordnet:

|Abschnitt|Grundlegende Beschreibung
---|---|
|Kopfzeile|Dieser Abschnitt enthält allgemeine Informationen zur Zeichnung. Es ist wie die Einstellungsfunktion in Ihrem Telefon, die die verschiedenen Variablen enthält, die der Zeichnung und den zugehörigen Werten zugeordnet sind. Beispielsweise definiert der Abschnitt Kopfzeile, welche AutoCAD-Version die DXF-Datei verwendet (die Variable $ACADVER) oder die Einheit, die zum Messen von Winkeln in der Datei verwendet wird (die Variable $AUNITS).
|Classes|Der Abschnitt CLASSES enthält die Informationen für anwendungsdefinierte Klassen, deren Instanzen in den Abschnitten BLOCKS, ENTITIES und OBJECTS der Datenbank erscheinen.
|Tabellen|Dieser Abschnitt enthält Definitionen für mehrere verschiedene Tabellen, von denen jede eine Reihe verschiedener Symboleinträge enthält. Zum Beispiel der [Zeilentyp](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) Tabelle (LTYPE) definiert das Muster von Strichen, Punkten, Text und Symbolen in der DXF-Datei und wie sie skaliert werden. Hier ist eine vollständige Liste der Tabellen in diesem Abschnitt:<ul><li> Anwendungs-ID-Tabelle (APPID).</li><li> Blockaufzeichnungstabelle (BLOCK_RECORD).</li><li> Bemaßungsstiltabelle (DIMSTYPE).</li><li> Layer (LAYER)-Tabelle</li><li> Linientyp (LTYPE)-Tabelle</li><li> Textstiltabelle (STYLE).</li><li> Benutzerkoordinatensystem (BKS)-Tabelle</li><li> Tabelle anzeigen (VIEW).</li><li> Viewport-Konfigurationstabelle (VPORT).</li></ul>
|Blöcke|Dieser Abschnitt enthält die grafischen Objekte und Zeichnungselemente, die jede Blockreferenz in der Zeichnung bilden.
|Entitäten|Dieser Abschnitt enthält die eigentlichen Objektdaten und grafischen Entitäten der Zeichnung. Dies können Rohdaten sein – ein Kreiselement wird beispielsweise durch seine Dicke, den Mittelpunkt, seinen Radius und seine Extrusionsrichtung definiert.
|Objekte|Hier finden Sie die nicht-grafischen Teile der Zeichnung. Hier werden beispielsweise AutoCAD-Wörterbücher gespeichert.

## Verweise ##

* [DXF-Dateispezifikationen](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF von Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

