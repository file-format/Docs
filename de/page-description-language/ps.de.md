{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS-Dateiformat",
  "description":"Erfahren Sie mehr über das PS-Dateiformat und APIs, die PS-Dateien erstellen und öffnen können.",
  "linktitle" :"PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine .PS-Datei? ##

PostScript (PS) ist eine universelle Seitenbeschreibungssprache, die im Desktop- und Electronic-Publishing-Geschäft verwendet wird. Das Hauptaugenmerk von PostScript (PS) liegt auf der Erleichterung des zweidimensionalen Grafikdesigns. Die meisten Sprachen erfordern eine bestimmte Kompilierungsphase vor der Codeausführung, während das Post Script (PS)-Format eine direkte Interpretation zur Laufzeit unterstützt. Seine frühe Version definiert die grafischen Formen, verschiedene Texterscheinungen und modellierte Bilder auf gedruckten Seiten oder angezeigten Seiten, wobei die Regeln des Adobe-Bildgebungsmodells befolgt werden. Ein PS-Programm ist in der Lage, eine Dokumentbeschreibung zwischen einem Kompositions- und einem Drucksystem zu kommunizieren, wobei das Gerät unabhängig und auf hohem Niveau gehalten wird. Darüber hinaus ist dieses Programm auch in der Lage, das Erscheinungsbild von Text und Grafiken auf einem Display zu steuern.

Die PostScript-Seitenbeschreibung kann mit Hilfe des PostScript-Interpreters des Geräts gerendert und auf Druckern und anderen Ausgabegeräten angezeigt werden. Da die Befehle zum Drucken von Zeichen, grafischen Formen und Bildern von einem Interpreter ausgeführt werden, wird für dieses spezielle Gerät die High-Level-PostScript-Beschreibung in das Low-Level-Rasterdatenformat konvertiert. Im Allgemeinen werden verschiedene Anwendungen wie Illustratoren, Dokumentenerstellungssysteme und computergestütztes Design (CAD) automatisiert, um PostScript-Seitenbeschreibungen zu erzeugen. Im Allgemeinen müssen Programmierer zum Zeitpunkt der Erstellung neuer Anwendungen PostScript-Programme schreiben. Ein Programmierer kann jedoch die Fähigkeiten der PostScript-Sprache nutzen, auf die in keiner Anwendung zugegriffen werden kann, indem er ein PS-Programm für diese spezielle Situation schreibt.

## Kurze Geschichte ##

Das Konzept der PostScript-Sprache wurde zuerst von John Warnock eingeführt. 1966 arbeitete er an einem Projekt des Hafens von New York. Er versuchte, einen Interpreter für große dreidimensionale Grafiken für die Datenbank dieses Projekts zu entwickeln. Für die Verarbeitung dieser Grafiken konzipierte John Warnock die Design System-Sprache. In der Zwischenzeit suchte Xerox PARC nach einem Standardmittel zum Definieren von Seitenbildern für seinen ersten Laserdrucker. Obwohl Bob Sproull und William Newman 1975-76 das Press-Format (Datenformat) entwickelten, um Laserdrucker anzusteuern, wurde eine Sprache für mehr Flexibilität benötigt. 1978 schloss sich Warnock Martin Newell bei Xerox PARC an und schrieb die Interpretationssprache JaM neu, die später erweitert und in die Interpress-Sprache erweitert wurde. Warnock gründete Adobe Systems im Dezember 1982 mit Chuck Geschke, Doug Brotz, Ed Taft und Bill Paxton. Sie begannen, an einer einfacheren Sprache namens PostScript zu arbeiten, ähnlich wie Interpress, die 1984 kommerziell auf den Markt kam. Steve Jobs von Apple besuchte sie und riet ihnen, PostScript für Laserdrucker anzupassen.

Im März 1985 war Apples LaserWriter der erste Drucker mit einem eingebetteten PostScript-Interpreter, der das Desktop-Publishing (DTP) revolutionierte. Die technische Solidität und weit verbreitete Verfügbarkeit machten PostScript zu einer Sprache der Wahl für Desktop- und elektronische Veröffentlichungen. 1990 war ein Interpreter für die PostScript-Sprache ein wesentlicher Bestandteil der Laserdrucker.

## Haupteigenschaften ##

Die Fähigkeiten der PostScript-Sprache zum Umgang mit interaktiven Grafiken und Seitenbeschreibungen besitzen die folgenden Merkmale:

**Formen:** Willkürlicher Natur, kann aus geraden Linien, Kurven, Quadraten und kubischen Kurven bestehen, die sowohl selbstdurchquerend als auch getrennt sein können (in Abschnitten und Löchern).

**Maloperatoren:** erlauben den Umriss der Form mit beliebiger Dicke, Farbe, Füllung oder erlauben das Zeichnen der Form als Ausschnitt, um das Zuschneiden anderer Grafiken zu ermöglichen.

**Farben:** haben die Vielfalt wie Graustufen, RGB, CMYK und CIE. Spezielle Arten von Farben werden als unterschiedliche Merkmale modelliert: Sonderfarben, Farbzuordnung, gleichmäßige Schattierung und sich wiederholende Muster.

**Text:** voll integriert mit Grafiken. Darüber hinaus ermöglicht das Adobe-Bildgebungsmodell, dass Textzeichen als grafische Formen angezeigt werden, die von jedem normalen Grafikoperator bedient werden können.

**Beispielbilder**: Aus Originalquellen (gescannte Fotos) extrahiert oder synthetisch hergestellt. Die PostScript-Sprache bietet vielfältige Mittel, um Bilder in jeder Auflösung und gemäß unterschiedlichen Farbmodellen auf einem Ausgabegerät zu regenerieren.

Eine Allzweck-Programmiersprache kann die Grafikfähigkeiten der PostScript-Sprache nutzen, indem sie Ps in ihr Gerüst einbettet. Die primitiven Datentypen wie Zahlen, Zeichen, Arrays und Strings; Steuerprimitive wie Schleifen, Prozeduren und Bedingungen; und einige unkonventionelle Funktionen, wie z. B. Wörterbücher, sind in der Sprache angegeben. Diese Merkmale erleichtern Programmierern das Schreiben von Befehlen zum Aufrufen von Operationen auf höherer Ebene. Diese High-Level-Operationen erfüllen die Anforderungen komplexer Anwendungen. Eine solche Praxis ist kompakter und effizienter als die Verwendung eines festen Satzes von Grundoperationen.

In PostScript geschriebene Programme können in Form von ASCII-Quelltext erstellt, kommuniziert und interpretiert werden. Die gesamte Sprache kann in Form von druckbaren Zeichen und Leerzeichen definiert werden. Diese Darstellung unterstützt Programmierer dabei, die Sprache einfach zu erstellen, zu manipulieren und zu verstehen. Darüber hinaus bleibt die Dateispeicherung und -übertragung zwischen verschiedenen Computern und Betriebssystemen durch die Maschinenunabhängigkeit komfortabel.

Binär codierte Formen der Sprache sind möglich, wenn dem Programm ein vollständig transparenter Kommunikationsweg zum PostScript-Interpreter garantiert wird. Strikte Übereinstimmung mit der ASCII-Darstellung von PS-Programmen wird von Adobe für den Dokumentenaustausch oder die Archivierung empfohlen.

## Versionen ##

PS(.ps) ist die Dateierweiterung für ein PostScript-Dokument. Das britische Nationalarchiv kategorisiert fünf chronologische Versionen der PostScript-Datei, die in der DSC-Version definiert sind: Versionen 1.0, 2.0, 2.1, 3.0, 3.1. Jede Version definiert wichtige Strukturierungskommentare. Encapsulated PostScript File (EPS) ist ein spezieller Untertyp der PostScript-Datei, die die Sprache verwendet, um eine rechteckige Grafik anzugeben. Das PostScript Language Reference Manual beschreibt ein EPS wie folgt: "Eine gekapselte PostScript-Datei (EPS) ist ein PostScript-Programm, das höchstens eine einzelne Seite in einer Form beschreibt, die von anderen Anwendungen importiert werden kann, um sie in ein enthaltendes Dokument einzubetten." Eine PostScript-Dokumentdatei kann eine EPS-Datei darin einkapseln. Eine zusätzliche Verwendung von PostScript wird als Display PostScript (DPS) erwähnt. DPS generiert Bildschirmgrafiken über eine Grafik-Engine, die das Bildgebungsmodell und die Sprache von PostScript verwendet.

## Verweise ##

* [PostScript-Formatfamilie](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

