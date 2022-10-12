{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX-Dateiformat",
  "description":"Erfahren Sie mehr über das TEX-Dateiformat und APIs, die TEX-Dateien erstellen und öffnen können.",
  "linktitle" :"TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine TEX-Datei? ##

**TeX** ist eine Sprache, die sowohl Programmier- als auch Markup-Funktionen umfasst, die zum Setzen von Dokumenten verwendet werden. Donald Knuth von der Stanford University ist der Schöpfer dieses einfallsreichen Satzsystems. Auf der ganzen Welt ist TeX die ultimative Wahl für Autoren und Verleger, um qualitativ hochwertige technische Dokumente zu erstellen. TeX leistet hervorragende Arbeit bei der Formatierung komplexer mathematischer Ausdrücke. In Verbindung mit einem hochwertigen Fotosatzgerät konkurriert TeX mit den Ergebnissen der besten traditionellen Satzsysteme. Daher gelten sie als die edelsten digitalen typografischen Systeme.

TeX-Eingabedateien basieren auf ASCII-Code und ermöglichen so den Austausch von Manuskripten zwischen Autoren, Verlagsleitern und Kritikern. Eine Vielzahl von Computerumgebungen, fast jede moderne Plattform und viele ältere Plattformen unterstützen TeX. Darüber hinaus ist TeX eine kostenlose Software, die einer breiten Palette von Verbrauchern zur Verfügung steht. Viele UNIX-Installationen verwenden sowohl UNIX troff als auch TeX als ihr Formatierungssystem für verschiedene Zwecke. Andere Satzaufgaben werden in Form von LaTeX, ConTeXt und anderen Makropaketen hervorragend ausgeführt.

## Kurze Geschichte ##

TeX wurde 1978 von Donald Knuth entworfen und geschrieben. Guy Steele vom Massachusetts Institute of Technology überarbeitete die Ein-/Ausgabe von TeX, damit es unter inkompatiblen Betriebssystemen wie Timesharing System (ITS) lauffähig wurde. Die erste Version von TeX wurde unter dem WAITS-Betriebssystem von Stanford in der Programmiersprache (SAIL) entwickelt und für die Ausführung auf einem PDP-10 getestet. Knuth führte die Idee der literarischen Programmierung für Vorabversionen ein. Die literarische Programmierung ist eine Möglichkeit, kompilierbaren Quellcode und Satz (in TeX) für eine vernetzte Dokumentation unter Verwendung der Originaldatei zu generieren. Die zur Entwicklung dieser fortgeschrittenen Versionen von TeX verwendete Sprache heißt WEB, eine Mischung aus DEC PDP-10 Pascal-Programmen, um die Portabilität zu gewährleisten.

Eine überarbeitete neue Version von TeX wurde 1982 veröffentlicht und hieß TeX82. Die wichtigste Änderung ist der Ersatz des ursprünglichen Silbentrennungsalgorithmus durch den neu geschriebenen Algorithmus von Frank Liang. Um die Portabilität über verschiedene Plattformen hinweg zu gewährleisten, verwendet TeX82 anstelle von Gleitkommazahlen Festkommaarithmetik zusammen mit einer echten, turing-vollständigen Programmiersprache. 1989 wurde eine neue Version von TeX und Metafont veröffentlicht. So ermöglicht die Version 3.0 von TeX 8-Bit-Eingaben und erlaubt 256 verschiedene Zeichen im Text. Nach Version 3 werden Aktualisierungen durch Hinzufügen einer zusätzlichen Ziffer am Ende der Dezimalstelle gekennzeichnet, z. B. wird die aktuelle Version von TeX als 3.14159265 angezeigt. Diese Version wurde zuletzt am 1.12.2014 aktualisiert.

## TeX-Eingabe ##

Eine Eingabedatei für TEX kann mit einem Texteditor unter Verwendung von gewöhnlichem Text erstellt werden. Im Gegensatz zu einem typischen Textverarbeitungsprogramm lässt diese Eingabedatei keine unsichtbaren Steuerzeichen zu. Eine Datei kann in eine andere Datei eingebettet werden, die Makrodefinitionen und Hilfsdefinitionen enthält, die die Fähigkeiten von TeX erweitern. Wenn eine TeX-Installation Makrodateien enthält, demonstrieren die lokalen Informationen über TeX die Verwendung von Makrodateien. Die Standardform von TeX integriert eine Kombination aus Makros und anderen Definitionen, die als einfaches TEX bekannt sind.

Auf Basis der genauen Kenntnis der Größen aller Zeichen und Symbole errechnet es die optimale Anordnung von Buchstaben pro Zeile und Zeilen pro Seite. Bei der Dokumentenverarbeitung wird eine .dvi-Datei erzeugt, wobei „dvi“ für „geräteunabhängig“ steht. Gerätetreiberprogramme sind zum Drucken oder Anzeigen einer Vorschau des Dokuments mit einer DVI-Erweiterung erforderlich. Heutzutage wird die dvi-Erzeugung durch ein allgemein verwendetes pdf-TeX umgangen. Innerhalb der TeX-Installation sind keine Vorkenntnisse über Schriftarten verfügbar, daher werden externe Schriftartdateien verwendet, die Teil der lokalen TeX-Umgebung sind, um Informationen für das Dokument zu erhalten.

## Satzsystem ##

Etwa 300 Primitive (Befehle) können vom Basis-TeX-System verstanden werden. Primitive sind Befehle auf niedriger Ebene, daher werden sie von einem gewöhnlichen Benutzer selten direkt verwendet und die meisten Funktionen werden von Formatdateien ausgeführt. Diese Formatdateien sind vorgeladene Speicherabbilder von TeX, denen das Laden großer Makrosammlungen folgt. Das ursprüngliche Standardformat der Sprache, dh einfaches TeX, fügt etwa 600 Befehle hinzu.

Ein mit geschweiften Klammern gruppierter umgekehrter Schrägstrich kennzeichnet den Anfang von TeX-Befehlen. Da TeX eine auf Makros und Token basierende Sprache ist, können fast alle syntaktischen Eigenschaften von TeX zur Laufzeit geändert werden, einschließlich benutzerdefinierter, mit Ausnahme von nicht erweiterbaren Token, die dann ausgeführt werden. Die Expansion selbst ist praktisch problemlos. Einige Befehle müssen nach Argumenten kommen, die dabei helfen, die Funktion eines Befehls zu erklären. Beispielsweise weist der Befehl \vskip TEX an, die Seite nach unten/oben zu überspringen, gefolgt von einem Argument, das bestimmt, wie viel Platz übersprungen werden soll.

## Versionen ##

LaTeX ist das am häufigsten verwendete Format, das ursprünglich von Leslie Lamport entwickelt wurde. LaTeX integriert verschiedene Dokumentstile für Dateien, Briefe, Bücher und Folien und bietet Verweise und automatische Nummerierung für verschiedene Abschnitte und mathematische Ausdrücke. AMS-TeX ist ein weiteres beliebtes Format, das von der American Mathematical Society entwickelt wurde.

AMS-TeX bietet viel benutzerfreundlichere Befehle, die von Zeitschriften neu definiert werden können, um sie an ihren lokalen Stil anzupassen. LaTeX kann die Vorteile von AMS-TeX nutzen, indem es die AMS-"Pakete" verwendet, die dann als AMS-LaTeX bezeichnet werden. ConTeXt ist ein weiteres Format, das von Hans Hagen geschrieben wurde und hauptsächlich für Desktop-Publishing verwendet wird.

Die TeX-Software bietet mehrere Funktionen, die zum Zeitpunkt ihrer Erstellung in anderen Satzsystemen nicht verfügbar oder von geringerer Qualität waren. Einige der innovativen Features dieser Sprache basieren auf interessanten Algorithmen, die aus den Thesen von Knuths Studenten abgeleitet wurden. Während andere Schriftsatzprogramme jetzt nützliche Funktionen von TeX in ihre Programme integrieren.

## Verweise ##

* [TeX-Schriftsatzsystem](https://en.wikipedia.org/wiki/TeX)

