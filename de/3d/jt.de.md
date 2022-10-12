{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "Datei", "Erweiterung", "Format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das JT-Dateiformat und APIs, die JT-Dateien erstellen und öffnen können.",
  "title" :"JT - Jupiter-Tessellationsdateiformat",
  "linktitle" :"JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine JT-Datei?

**JT** (Jupiter Tessellation) ist ein effizientes, branchenorientiertes und flexibles ISO-standardisiertes 3D-Datenformat, das von Siemens PLM Software entwickelt wurde. Mechanische CAD-Bereiche der Luft- und Raumfahrt, der Automobilindustrie und der Schwermaschinenbau verwenden JT als ihr führendes 3D-Visualisierungsformat.

Das JT-Format ist ein Szenendiagramm, das die CAD-spezifischen Attribute und Knoten unterstützt. Hochentwickelte Komprimierungstechniken werden verwendet, um Facettendaten (Dreiecke) zu speichern. Dieses Format ist so strukturiert, dass es visuelle Attribute, Produkt- und Herstellungsinformationen (PMI) und Metadaten unterstützt. Es gibt eine gute Unterstützung für das asynchrone Streamen von Inhalten. In der Schwermaschinenindustrie verwenden Fachleute JT-Dateien in ihren CAD-Lösungen und Softwareprogrammen für das Produktlebenszyklusmanagement (PLM), um die Geometrie komplizierter Güter zu untersuchen.

Da JT fast alle wichtigen 3D-CAD-Formate unterstützt, kann seine Baugruppe mit einer Vielzahl von Kombinationen umgehen, die als "Multi-CAD" bekannt sind. Diese Multi-CAD-Baugruppe ist immer gut verwaltet und auf dem neuesten Stand, da die Synchronisation zwischen den nativen CAD-Produktbeschreibungsdateien mit den zugehörigen JT-Dateien automatisch erfolgt. JT-Dateien sind ursprünglich leichtgewichtig und gelten daher als geeignet für die Zusammenarbeit im Internet. Unternehmen arbeiten viel einfacher zusammen, indem sie 3D-Visualisierungen über die Medien senden, verglichen mit „schweren“ Original-CAD-Dateien. Darüber hinaus gewährleisten JT-Dateien viele Sicherheitsfunktionen, die den Austausch von geistigem Eigentum sicherer machen.

## Geschichte

Engineering Animation, Inc. und Hewlett Packard waren die ursprünglichen Designer von JT, die dieses Format als Direct Model Toolkit entwickelt haben. Nach der Übernahme von EAI durch UGS Corp. wurde JT Teil der UGS-Suite. Anfang 2007 kündigte UGS JT als ihr Master-3D-Format an. Im selben Jahr erwarb die Siemens AG UGS und entpuppte sich als Siemens PLM Software. Siemens verwendet JT als gemeinsames Interoperabilitätsformat und Datenarchivierungsformat. Im Jahr 2009 akzeptierte die ISO die JT-Spezifikation zur Veröffentlichung als ISO Publicly Available Specification (PAS). Mitte 2010 gab ProSTEP iViP bekannt, dass auf industrieller Ebene JT und STEP AP 242 XML zusammen verwendet werden können, um den maximalen Datenvorteil zu erzielen Austauschszenarien. 2012 wurde JT offiziell zum ISO-standardisierten (ISO 14306:2012 (ISO JT V1)) 3D-Visualisierungsformat erklärt.

## JT-Dateiformat ##

Alle Objekte im JT-Format werden durch eine Objektkennung dargestellt, und Verweise zwischen Objekten werden durch die Kennung des referenzierten Objekts gehandhabt. Die Integrität dieser Objektreferenzen kann durch Umstellen/Umstellen von Zeigern aufrechterhalten werden.

Eine JT-Datei ist als eine Reihe von Blöcken angeordnet und der Header-Block ist immer der erste Datenblock in der Datei. Eine Reihe von Datensegmenten und ein TOC-Segment folgen unmittelbar auf den Kopfblock. Das eine Datensegment (6 LSG Segment) besitzt immer eine referenzkonforme JT-Datei. Das TOC-Segment enthält die Standortinformationen aller anderen Datensegmente dieser Datei.

{{< figure src="../JT-1.png" alt="JT-Dateiformat" >}}

### Dateikopf ###

Der Dateikopf ist der erste Block in der Datenhierarchie der JT-Datei. Versionsinformationen und Informationen zum Standort des Inhaltsverzeichnisses sind im Header eingeschlossen, was Ladern das Lesen von Dateien erleichtert. Die Dateikopfinhalte sind wie folgt angeordnet.

### Inhaltsverzeichnissegment ###

Das TOC-Segment muss in einer Datei vorhanden sein und enthält Identifikations- und Positionsinformationen aller anderen Datensegmente. Die tatsächliche Position des TOC-Segments wird durch das TOC-Offset-Feld des Dateiheaders angegeben. Jedes einzeln adressierbare Datensegment wird durch einen TOC-Eintrag in einem TOC-Segment dargestellt.

### Datensegment ###

Die JT-Datei definiert alle gespeicherten Daten innerhalb eines Datensegments. Einige Datensegmente können alle Datenbytes an Informationen komprimieren, die innerhalb des Segments verbleiben. Datensegmente haben folgende Struktur:

![alt text](../JT-2.png "JT Data Segment")


Die folgende Tabelle beschreibt verschiedene Arten von Datensegmenten:

|Name|Beschreibung
---|---|
|LSG-Segment|Umfasst eine Sammlung von Objekten, die durch gerichtete Verweise verbunden sind, um LSG (gerichtete azyklische Graphenstruktur) zu bilden
|Form-LOD-Segment|enthält die definierenden Daten für die geometrischen Formen (z. B. Scheitelpunkte, Normalen, Polygone usw.)
|JT B-Rep Segment|Mit einem Element für die Daten, um die genaue geometrische Grenze für einen einzelnen Abschnitt im JT B-Rep-Format darzustellen.
|XT B-Rep-Segment|Element für die Daten aufweisend, um die genaue geometrische Grenze für einen einzelnen Abschnitt im Grenzdarstellungsformat darzustellen
|Drahtgittersegment|Die Daten stellen ein präzises 3D-Drahtgitter für einen bestimmten Teil dar, der durch ein in diesem Segment enthaltenes Element definiert wird.
|Metadatensegment|Ermöglicht das Speichern von Metadaten in verschiedenen adressierbaren Segmenten.
|JT-ULP-Segment|mit einem Element für die Daten zur Darstellung der halbgenauen geometrischen Grenze für einen einzelnen Abschnitt im JT-ULP-Format.
|JT LWPA-Segment|Enthält ein Element, das analytische Daten für ein bestimmtes Teil definiert. LWPA schließt die analytische Oberflächensammlung in die b-rep-Definition des Teils ein.

## Kompression ##

Übertragungs- und Speicheranforderungen von 3D-Modellen sind anspruchsvoller, daher können JT-Dateien die Vorteile der Komprimierung nutzen. Ein JT-Datenmodell kann aus verschiedenen Dateien bestehen, die unterschiedliche Komprimierungstechniken verwenden, aber der Komprimierungsprozess ist für JT-Datenbenutzer transparent.

Bisher sind JT Open Toolkit (als Standard) und erweiterte Komprimierung zwei Komprimierungstechniken, die von JT-Dateien verwendet werden. JT Open Toolkit verwendet einen einfachen, verlustfreien Komprimierungsalgorithmus, während die erweiterte Komprimierung eine verfeinerte, domänenspezifische Komprimierungstechnik verwendet, die zu einer verlustbehafteten Geometriekomprimierung führt. Clientanwendungen bevorzugen die erweiterte Komprimierung gegenüber der Verwendung der Standardkomprimierung, da die erweiterte Komprimierung ziemlich hohe Komprimierungsverhältnisse ergibt. Die Abwärtskompatibilität mit gewöhnlichen Anwendungen zur Anzeige von JT-Dateien wird durch die Bereitstellung einer Standardkomprimierung aufrechterhalten. Das Komprimierungsformular muss mit der Version des JT-Dateiformats kompatibel sein, die angezeigt wird, wenn eine JT-Datei mit einem Texteditor geöffnet und in ASCII-Header-Informationen eingeschlossen wird.

## Verweise ##

* [JT File Format Reference](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (Visualisierungsformat)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

