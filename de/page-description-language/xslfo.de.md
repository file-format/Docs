{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "XSL-Formatierungsobjekte", "Datei", "Erweiterung", "Dateiformat", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Erfahren Sie mehr über das XSLFO-Dateiformat und APIs, die XSLFO-Dateien erstellen und öffnen können.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine XSL-FO-Datei? ##

XSL-FO (XSL Formatting Objects) ist eine leistungsstarke Stylesheet-Sprache zum Formatieren von XML-Dokumenten. Die Semantik der gebundenen Form von Papier und Druck wird durch XSL-FO ausgedrückt, wenn die Dimensionen festgelegt sind. Im Gegensatz zu HTML, das die Semantik der unbegrenzten Form eines Browserfensters mit variablen Abmessungen darstellt. Die von XSL-FO formatierten XML-Dokumente werden meist zur Generierung von PDF-Dateien verwendet. XSL (Extensible Stylesheet Language) ist eine Reihe von W3C-Technologien mit vollständigen Funktionen, die für die Formatierung und den Austausch von XML-Dokumenten und XSL-FO-Teil dieser Sprache konzipiert sind. XSLT und XPath sind auch andere Teile von XSL.

Es wird vorgeschlagen, XML-Dokumente zuerst in XSL-FO umzuwandeln, PDF ist ein Beispiel für dieses Kriterium. In PDF werden die Ergebnisse zuerst mit XSLT und dann mit dem XSL-FO-Formatierer gerendert. Auf diese Weise können XML-Dokumente beliebig formatiert werden. Obwohl XSL-FO den Vorteil nutzt, Cascading Style Sheet (CSS)-Eigenschaften zu verwenden und sie zu erweitern, wo immer es für das reale Format erforderlich ist, enthält es die Bereitstellung von Seitenvorlagen, die in der Terminologie von XSL-FO als Seitenmaster bezeichnet werden. XSL-FO bietet auch Formatierung für ziemlich komplexe Dokumente und unterstützt die Indexerstellung.

## Geschichte und grundlegende Konzepte ##

Im Januar 2012 wurde der Working Draft von XSL-FO letztmalig aktualisiert, und im November 2013 wurde seine Working Group geschlossen. Ein XSL-Stylesheet spezifiziert die Präsentation einer Klasse von XML-Dokumenten, indem es beschreibt, wie eine Instanz der Klasse in ein XML-Dokument transformiert wird, das das Formatierungsvokabular verwendet. XSL-FO ist eine integrierte Präsentationssprache und hat keine semantischen Auszeichnungen, die in HTML verwendet werden. Darüber hinaus speichert diese Sprache alle Daten des Dokuments in sich selbst, im Gegensatz zu CSS, das die Standardeinstellungen eines externen HTML- oder XML-Dokuments ändert.

Das allgemeine Kriterium für die Verwendung von XSL-FO ist, dass der Benutzer ein Dokument in einer XML-Sprache schreibt, anstatt in FO zu schreiben. Danach erfolgt eine XSLT-Transformation. Diese XSLT-Transformation ist für die Konvertierung von XML in XSL-FO verantwortlich. Sobald das XSL-FO-Dokument erstellt ist, wird es an eine Anwendung namens FO-Prozessor übergeben. FO-Prozessoren sind dafür verantwortlich, dieses Dokument in ein lesbares sowie ein druckbares Dokument umzuwandeln. PDF-Dateien oder PS sind Beispiele für die häufigste Ausgabe von XSL-FO. Dies bedeutet jedoch nicht, dass der FO-Prozessor nur diese beiden Formattypen als Ausgabe erzeugen kann. Einige FO-Prozessoren können in den RTF-Dateien ausgeben oder sogar ein Fenster kann in der GUI des Benutzers erscheinen, dieses Fenster zeigt die Seitenfolge und ihren Inhalt an.

Ein XSL-FO-Dokument unterscheidet sich von einem PDF oder einem PS in dem Sinne, dass es letztendlich nicht das Textlayout auf verschiedenen Seiten definiert. Vielleicht gestaltet es die Seiten und bestimmt die Orte, an denen der Inhalt angezeigt wird. Darüber hinaus organisiert ein FO-Prozessor den Text innerhalb der durch das FO-Dokument spezifizierten Grenzen. Diese Spezifikation erlaubt es sogar, dass sich verschiedene FO-Prozessoren entsprechend den resultierenden erzeugten Seiten verhalten. Ein Beispiel für ein solches Verhalten ist die Silbentrennung. Nur wenige FO-Prozessoren können Wörter trennen, um Platz zu sparen, wenn eine Zeile umbricht, während einige Prozessoren diese Option nicht auswählen. Es hängt von den Prozessoren ab, unterschiedliche Silbentrennungsalgorithmen zu wählen, die ihren Anforderungen entsprechen. Diese Silbentrennungsalgorithmen können sehr einfach oder auch komplexer sein. In manchen Situationen sanktioniert die XSL-FO-Spezifikation explizit FO-Prozessoren, ein gewisses Maß an Auswahl im Zusammenhang mit dem Layout.

Diese Variation unter den FO-Prozessoren erzeugt unterschiedliche Ergebnisse, über die die Prozessoren oft nicht besorgt sind. Weil der allgemeine Fokus von XSL-FO auf der Erstellung von Seiten/gedruckten Dokumenten liegt. XSL-FO-Dokumente selbst fungieren normalerweise als Vermittler, ihre Hauptfunktion besteht darin, entweder PDF-Dateien oder ein Dokument zu generieren, das als zu verteilende Ausgabe gedruckt werden kann. In HTML/CSS oder XSL-FO zeigt die Verteilung des PDF als Endergebnis anstelle der Eingabe der Formatierungssprache an, dass die Empfänger von der resultierenden Vielseitigkeit unberührt bleiben, die aufgrund von Unterschieden zwischen den Interpretern der Formatierungssprache erzeugt wird. Andererseits ist es offensichtlich, dass es keinen einfachen Weg gibt, dass ein Dokument die unterschiedlichen Bedürfnisse der Empfänger erfüllen kann, z. B. variable Seitengröße oder gewünschte Schriftgröße oder Anpassung für Seite oder Druck.

## XSLFO-Dateiformat ##

SL-FO-Dokumente sind grundsätzlich XML-Dokumente, folgen aber keinem Schema. Stattdessen folgen SL-FO-Dokumente der Syntax, die in der Spezifikation ihrer eigenen Sprache definiert ist. In jedem XSL-FO-Dokument sind zwei Abschnitte erforderlich:

1. Ein Abschnitt, der eine Liste mit beschrifteten Seitenlayouts angibt.
1. Ein Abschnitt mit allen Details von Dokumentdaten, mit Markup, das die Anzeige von Inhalten auf verschiedenen Seiten durch verschiedene Seitenlayouts bestimmt.

Eigenschaften der Seite werden in den Seitenlayouts erwähnt, die die Organisation für den Text definieren können, um den Konventionen für die spezifische Sprache zu entsprechen. Darüber hinaus werden auch die Seitengröße, deren Seitenränder und Seitenfolgen (die unterschiedliche Eigenschaften für die ungeraden und geraden Seiten vorsehen) durch die Seitenlayouts definiert.

Der Datenteil des Dokuments ist in eine Reihe von Flüssen unterteilt, wobei jeder Fluss mit einem Seitenlayout verbunden ist. Die Flows schließen eine Liste von Blöcken ein. Diese Liste von Blöcken kann Inline-Markup-Features oder eine Liste von Textdaten oder vielleicht beides gleichzeitig enthalten. An den Rändern des Dokuments können auch die Seitenzahlen oder Kapitelüberschriften angezeigt werden. Die Funktionalität sowohl von Blöcken als auch von Inline-Elementen bleibt die gleiche wie in CSS, jedoch unterscheiden sich einige Füll- und Randregeln zwischen FO und CSS.

Die Richtung der Seitenausrichtung ist vollständig für die Erweiterung von Blöcken und Zeilen angegeben, wodurch FO-Dokumente unter anderen Sprachen als Englisch funktionieren. Die Sprache der FO-Spezifikation verwendet die Wörter start und end anstelle von left und right zur Wegbeschreibung. Das grundlegende Inhalts-Markup und die Kaskadierungsregeln von XSL-FO stammen von CSS. Die Sprache von XSL-FO stimmt mit den folgenden Spezifikationen überein.

## Mehrere Spalten ##

Eine Seite kann mehrere Spalten und Blöcke haben und sich standardmäßig von einer Spalte zur anderen erstrecken. Mehrere Seiten dürfen unterschiedliche Breiten und Spaltenzahlen haben. Alle FO-Merkmale folgen den Grenzen einer mehrspaltigen Seite.

### Listen ###

Eine XSL-FO-Liste wird durch zwei Sätze von Blöcken erstellt, die Seite an Seite angeordnet sind. Konzeptionell zeigt ein Block auf der linken Seite in einer Liste eine Zahl, ein Aufzählungszeichen oder eine Textfolge an, während der Block auf der rechten Seite wie erwartet funktionieren kann. Die Nummerierung von XSL-FO-Listen wird normalerweise von XSLT vorgenommen.

### Tabellen ###

Eine FO-Tabelle ähnelt einer HTML/CSS-Tabelle. Der Benutzer kann die Datenzeilen, Gestaltungsinformationen und Hintergrundfarbe für jede einzelne Zelle auswählen. Unter Verwendung eindeutiger Gestaltungsinformationen hat der Benutzer das Recht, die erste Zeile als Tabellenkopfzeile auszuwählen. Der FO-Prozessor kann explizit über die Platzangabe jeder Spalte informiert werden oder den Text automatisch in die Tabelle einpassen.

### Indizierung ###

XSL-FO 1.1 verfügt über Funktionen, die dabei helfen, einen Index zu generieren, indem auf korrekt gekennzeichnete Elemente verwiesen wird.

### Vorteile ###

* Geeignet für inhaltsbasierte Veröffentlichungen
* Benutzerfreundlichkeit
* Kostengünstig

## Verweise ##

* [Was ist XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL-Formatierungsobjekte](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

