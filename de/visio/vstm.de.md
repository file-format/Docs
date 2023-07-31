{
  "date" : "2019-10-11",
  "keywords" :[ "vstm-Datei", "vstm-Dateiformat", "was ist eine vstm-Datei", "Datei", "vstm-Beispiel", "vstm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio-Vorlagendateiformat",
  "description":"Erfahren Sie mehr über das VSTM-Dateiformat und APIs, die VSTM-Dateien erstellen und öffnen können.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
"identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine VSTM-Datei?

Dateien mit der Dateiendung VSTM sind mit Microsoft Visio erstellte Vorlagendateien, die Makros unterstützen. Im Gegensatz zu VSDX-Dateien können aus VSTM-Vorlagen erstellte Dateien Makros ausführen, die in VBA-Code (Visual Basic for Applications) entwickelt wurden. Eine Vorlagendatei kann erstellt werden, um grundlegende Einstellungen des Dokuments bereitzustellen, die verwendet werden können, um weitere Dokumente mit diesen Einstellungen zu erzeugen. Visio-Dateien werden zum Erstellen von Zeichnungen verwendet, die visuelle Objekte, Flussdiagramme, UML-Diagramme, Informationsflüsse, Organigramme, Softwarediagramme, Netzwerklayouts, Datenbankmodelle, Objektzuordnungen und andere ähnliche Informationen enthalten. Mit Visio generierte Dateien können auch in verschiedene Dateiformate wie PNG, BMP, PDF und andere exportiert werden.

## Datei Format ##

VSTM-Dateien basieren auf den Open Packaging Conventions und XML, und Entwickler können von diesem Format profitieren, indem sie lernen, wie sie programmgesteuert mit diesen Dateien arbeiten. Das Format erbt viele der gleichen XML-Strukturen wie seine Teile aus dem Visio-XML-Zeichnungsdateiformat (.vdx). Die Interoperabilität mit Visio-Dateien wird erheblich verbessert, da Software von Drittanbietern Visio-Dateien auf Dateiformatebene manipulieren kann.

Jede Visio-Datei wird als Paket bezeichnet, das andere Dateien oder Teile enthält. Ein Paketteil kann eine XML-Datei, ein Bild oder sogar eine VBA-Lösung sein. Die Teile innerhalb des Pakets können in „Dokument“- und „Beziehungs“-Teile unterteilt werden.

### Dokumentieren ###

Die Dokumentteile enthalten den eigentlichen Inhalt und die Metadaten der Visio-Datei, wie den Namen der Datei, die erste Seite und alle darin enthaltenen Shapes und sogar die Datenverbindungen für die Shapes. Bilder und Textdateien innerhalb des Pakets werden als Dokumentteile betrachtet.

### Beziehungen ###

Die Beziehungsteile einer Visio-Datei werden im Ordner „_rels“ gespeichert und beschreiben, wie die Teile innerhalb des Pakets miteinander in Beziehung stehen. Es stellt auch die Struktur der Datei bereit. Ein eigenständiges XML-Dokument verwendet die Eltern/Kind-Beziehung von Elementen, um die Beziehung von Entitäten zueinander zu bestimmen. Ein gültiges Visio 2013-Dateiformat enthält den richtigen Satz von Teilen, und das Paket enthält die Beziehungen zwischen den Teilen.

Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen innerhalb des Pakets beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einer angegebenen Quelle (definiert durch den Namen und Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beispielsweise werden Beziehungsteile verwendet, um zu beschreiben, welche Formvorlagen mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander zusammenhängen oder wie Bilder und Objekte mit einer bestimmten Seite zusammenhängen.

## Verweise ##

* [Einführung in das Visio-Dateiformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

