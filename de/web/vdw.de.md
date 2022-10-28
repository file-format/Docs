{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","vdw-Datei", "vdw-Dateiformat", "vdw-Dateityp", "Datei", "Typ", "was ist eine vdw-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio Graphics Service-Dateiformat",
  "description":"Erfahren Sie mehr über das VDW-Dateiformat und APIs, die VDW-Dateien erstellen und öffnen können.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}
## Was ist eine VDW-Datei?
VDW ist das Dateiformat des Visio Graphics Service, das die zum Rendern einer Webzeichnung erforderlichen Streams und Speicher angibt. Eine Webzeichnung ist eine Sammlung von Zeichenseiten, Formen, Schriftarten, Bildern, Datenverbindungen und Diagrammaktualisierungsinformationen, die als Vektor- oder Rasterzeichnung gerendert werden können. VDW-Dateien können auch in Microsoft Visio geöffnet werden, werden aber hauptsächlich für die Verwendung im Web gespeichert. Microsoft Visio bietet die Möglichkeit, Visio-Dateien in eine Reihe verschiedener Dateiformate zu konvertieren, darunter [PNG](/de/Image/PNG/), [BMP](/de/Image/BMP/), [PDF](/de/pdf/) und andere.

## **VDW** Dateiformat #

Die technischen Spezifikationen des VDW-Dateiformats sind online von [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) verfügbar und können von Entwicklern zum Erstellen herangezogen werden Anwendungen. Das technische Dokument beschreibt Daten, die in einer zusammengesetzten Datei enthalten sind, die Speicher und Streams enthält. Die Darstellung einer Webzeichnung wird durch einen Stream namens VisioServerData über ein ZIP-Archiv ermöglicht. Ein ShapGraphic-XML-Teil im Archiv beschreibt die grafischen Elemente, die in der Webzeichnung angezeigt werden, und werden in Extensible Application Markup Language (XAML) ausgedrückt. Eine Sammlung von XML-Teilen im ZIP-Archiv beschreibt die Datenverbindung der Webzeichnung, Informationen über ihre Form und die Aktualisierungslogik des Diagramms. Diese Teile werden als XML ausgedrückt. Der DataGraphic-XML-Teil beschreibt neu berechnete Eigenschaften, die ausgewertet werden sollen, nachdem die Daten in der Webzeichnung aus der Datenquelle aktualisiert wurden. Zusätzliche Elemente im ZIP-Archiv enthalten Informationen zu den Schriftarten und Bildern, die in der Webzeichnung verwendet werden.

|![Mögliche Implementierung einer Datei](/de/web/vdw.png "Mögliche Implementierung einer Datei")

## Verweise ##

* [[MS-VGSFF]: Dateiformat des Visio-Grafikdiensts (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

