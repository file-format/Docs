{
  "date" : "2019-10-11",
  "keywords" :[ "vsdm-Datei", "vsdm-Dateiformat", "was ist eine vsdm-Datei", "Datei", "vsdm-Beispiel", "vsdm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio-Zeichnungsdateiformat",
  "description":"Erfahren Sie mehr über das VSDM-Dateiformat und APIs, die VSDM-Dateien erstellen und öffnen können.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
"identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine VSDM-Datei?

Dateien mit der Erweiterung .vsdm sind Zeichnungsdateien, die mit der Microsoft Visio-Anwendung erstellt wurden, die Makros unterstützt. VSDM-Dateien sind OPC/XML-Zeichnungen, die VSDX ähneln, aber auch die Möglichkeit bieten, Makros auszuführen, wenn die Datei geöffnet wird. Makros sind benutzerdefinierte Aktionen/Schritte, die in Visual Basic for Applications (VBA) entwickelt wurden und zur Ausführung sich wiederholender Aufgaben verwendet werden können. Das VSDM-Dateiformat wurde mit der Einführung von Microsoft Visio 2013 eingeführt. Visio-Dateien werden verwendet, um Zeichnungen zu erstellen, die visuelle Objekte, Flussdiagramme, UML-Diagramme, Informationsflüsse, Organigramme, Softwarediagramme, Netzwerklayouts, Datenbankmodelle, Objektzuordnungen und andere enthalten ähnliche Informationen. Mit Visio generierte Dateien können auch in verschiedene Dateiformate wie [PNG](/de/image/png/), [BMP](/de/image/bmp/), [PDF](/de/pdf/) und andere exportiert werden.

## VSDM-Dateiformat

VSDM-Dateien basieren auf den Open Packaging Conventions und XML, und Entwickler können von diesem Format profitieren, indem sie lernen, wie sie programmgesteuert mit diesen Dateien arbeiten. Das Format erbt viele der gleichen XML-Strukturen wie seine Teile aus dem Visio-XML-Zeichnungsdateiformat (.vdx). Die Interoperabilität mit Visio-Dateien wird erheblich verbessert, da Software von Drittanbietern Visio-Dateien auf Dateiformatebene manipulieren kann.

Jede Visio-Datei wird als Paket bezeichnet, das andere Dateien oder Teile enthält. Ein Paketteil kann eine XML-Datei, ein Bild oder sogar eine VBA-Lösung sein. Die Teile innerhalb des Pakets können in „Dokument“- und „Beziehungs“-Teile unterteilt werden.

### Dokumentieren ###

Die Dokumentteile enthalten den eigentlichen Inhalt und die Metadaten der Visio-Datei, wie den Namen der Datei, die erste Seite und alle darin enthaltenen Shapes und sogar die Datenverbindungen für die Shapes. Bilder und Textdateien innerhalb des Pakets werden als Dokumentteile betrachtet.

### Beziehungen ###

Die Beziehungsteile einer Visio-Datei werden im Ordner „\_rels“ gespeichert und beschreiben, wie die Teile innerhalb des Pakets miteinander in Beziehung stehen. Es stellt auch die Struktur der Datei bereit. Ein eigenständiges XML-Dokument verwendet die Eltern/Kind-Beziehung von Elementen, um die Beziehung von Entitäten zueinander zu bestimmen. Ein gültiges Visio 2013-Dateiformat enthält den richtigen Satz von Teilen, und das Paket enthält die Beziehungen zwischen den Teilen.

Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen innerhalb des Pakets beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einer angegebenen Quelle (definiert durch den Namen und Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beispielsweise werden Beziehungsteile verwendet, um zu beschreiben, welche Formmaster mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander in Beziehung stehen oder wie Bilder und Objekte mit einer bestimmten Seite in Beziehung stehen.

## Verweise ##

* [Einführung in das Visio-Dateiformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

