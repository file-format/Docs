{
  "date" : "2021-05-25",
  "keywords" :[ "DML","DML-Datei", "DML-Dateiformat", "DML-Dateityp", "Datei", "Typ", "Was ist eine DML-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - DynaScript-HTML-Datei",
  "description":"Erfahren Sie mehr über das DML-Dateiformat und APIs, die DML-Dateien erstellen und öffnen können.",
  "linktitle" :"DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Was ist eine DML-Datei?

Eine Datei mit der Erweiterung .dml ist eine mit DyanScript erstellte Webskript-Seitencodedatei. DynaScript ist eine dynamische [HTML](/de/web/html/)-Skriptsprache, die mit ECMAScript kompatibel ist und die meisten der gleichen Funktionen wie andere Skriptsprachen bietet. Es ähnelt ColdFusion-Code und Microsoft Active Server Pages (ASP)-Code. DML-Dateien können ähnlich wie andere HTML-Seiten in Standard-Webbrowsern geöffnet und angezeigt werden.

## DML-Dateiformat

DML-Dateien werden im Nur-Text-Dateiformat erstellt und können mit einem Texteditor geöffnet werden, um den Code anzuzeigen. Das Schreiben von Code unter Verwendung der DML-Skriptsprache kann verwendet werden, um HTML auf serverseitig gehosteten DML-Seiten dynamisch zu generieren. DynaScripts werden aus den folgenden Sprachelementen aufgebaut:


* SCRIPT-Tag - Diese werden als HTML-Kommentare in Dokumente eingebettet. Ein HTML-Kommentar wird durch ein \ gekennzeichnet <!-- tag.
* Literale - Dies sind feste Werte in DynaScript-Dateien. Beispiele hierfür sind Ganzzahlen wie s 123 , 0x3F , 0123, Fließkommazahlen wie 456.789 , 3.2e-8, boolesche Werte wie true oder false und Zeichenfolgen wie „Der Regen in Spanien“.
* Variablen - DynaScript-Variablen müssen nicht definiert oder einem festen Datentyp zugewiesen werden. Eine Variable muss einen Wert haben, bevor Sie sie in einem Ausdruck verwenden; andernfalls wird eine Laufzeitwarnung generiert.
* Ausdrücke - Dies sind Kombinationen von Variablen, Literalwerten, Operatoren und anderen Ausdrücken. Die rechte Seite einer Zuweisungsanweisung ist ein Ausdruck.
* Operatoren - Diese operieren auf einem oder mehreren Ausdrücken, die als Operanden bezeichnet werden. Diese können entweder ternär, binär oder unär sein: Ternäre Operatoren wirken auf drei Ausdrücke, binäre Operatoren auf zwei Ausdrücke und unäre Operatoren auf einen.
* Anweisungen - Diese steuern den Skriptfluss, manipulieren Objekte und die allgemeine Programmierung. Im Allgemeinen folgen diese Anweisungen der Standard-C- und Java-Syntax. Beispiele sind if-else, do-while loops, switch, break, Continue usw. wie jede andere Skriptsprache.
* Funktionen - Funktionen ermöglichen Ihnen wie jede andere Skriptsprache, eine Reihe von Anweisungen einmal in einem Dokument als Funktion zu kapseln und sie dann mehrmals im gesamten Dokument zu verwenden (durch Aufrufen der Funktion). DynaScript unterstützt auch Funktionen.
* Objekte - DynaScript ist objektorientiert und unterstützt "Objekte" und die grundlegenden objektorientierten Konzepte von Kapselung, Polymorphismus und Vererbung.

