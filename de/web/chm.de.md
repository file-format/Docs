{
  "date" : "2019-10-11",
  "keywords" :[ "chm","chm-Datei", "chm-Dateiformat", "chm-Dateityp", "Datei", "Typ", "was ist eine chm-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Kompiliertes HTML-Hilfedateiformat",
  "description" :"Erfahren Sie, was eine CHM-Datei und APIs sind, die sie erstellen und öffnen können.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine CHM-Datei?

Das CHM-Dateiformat stellt die Microsoft **[HTML](/de/web/html/)**-Hilfedatei dar, die aus einer Sammlung von HTML-Seiten besteht. Es bietet einen Index für den schnellen Zugriff auf die Themen und die Navigation zu verschiedenen Teilen des Hilfedokuments. Die CHM-Datei kann über die bereitgestellte Suchoption nach Inhalten durchsucht werden. CHM ist ein Microsoft-eigenes Online-Hilfedateiformat, das häufig für die Softwaredokumentation verwendet wird. Darüber hinaus wird es in mehreren anderen Anwendungen wie Schulungshandbüchern, interaktiven Büchern und elektronischen Newslettern verwendet. Die meisten modernen Microsoft-Entwicklungsumgebungen unterstützen das Generieren von CHM-Dokumentation aus Informationen, die in der Anwendung verfügbar sind.

Die einzigartige Fähigkeit des CHM-Dateiformats, ein kombiniertes Inhaltsverzeichnis und einen Index zu implementieren, unterscheidet es von anderen Standard-HTML-Seiten. Die generierte CHM-Datei ist relativ klein und kann daher problemlos mit Softwarepaketen verteilt werden. Das Hilfe-Entwicklungstool HTML Help Workshop bietet ein benutzerfreundliches System zum Erstellen und Verwalten von Hilfeprojekten und zugehörigen Dateien. CHM-Dateien können Text, Bilder und Hyperlinks enthalten; sichtbar in einem Webbrowser; Wird von Windows und anderen Programmen als Online-Hilfelösung verwendet.

## CHM-Dateiformat

Die endgültige Form der generierten CHM-Datei hängt davon ab, wie das Hilfesystem gestaltet ist und ob es für eine Anwendung oder eine Website bestimmt ist. Eine CHM-Datei unterstützt die Datenkomprimierung mit LZX-Komprimierung, um die komprimierten HTML-Dateien zu generieren. Es verfügt über eine integrierte Suchmaschine zum schnellen Durchsuchen von Inhalten sowie die Möglichkeit, mehrere .CHM-Dateien zusammenzuführen. Eine CHM-Datei besteht aus einer Reihe von HTML-Dateien, einem verknüpften Inhaltsverzeichnis und einer Indexdatei.

### HTML-Dateien

Unabhängig davon, ob Sie Hilfethemen für die Verteilung mit einem Programm oder im Internet erstellen, die von Ihnen verfassten Dokumente werden mit einer speziellen Formatierungssprache erstellt, die als Hypertext Markup Language (HTML) bezeichnet wird. HTML-Themendateien haben die Dateinamenerweiterung .htm oder .html.

Obwohl jedes Hilfethema oder jede Webseite, die Sie erstellen, wie ein Dokument mit Text, Grafiken oder animierten Bildern aussieht, sind .htm-Dateien eigentlich Textdokumente mit speziellen HTML-Formatierungscodes. Diese Codes, Tags genannt, teilen einem Browser mit, wie jede Seite angezeigt werden soll. Nur der Text, der in einem Thema oder einer Webseite erscheint, befindet sich tatsächlich in der .htm-Datei. Alle Grafiken, Sounds, animierten Bilder oder andere Elemente, die angezeigt werden, sind separate Dateien, auf die Ihre HTML-Datei verweist. Der Browser kopiert oder lädt die Grafiken, Sounds oder andere Elemente herunter, wenn er die Tags sieht, die ihn dazu auffordern.

### Inhaltsverzeichnis (TOC)
Die Inhaltsverzeichnisdatei (.hhc) der Hilfe ist eine HTML-Datei, die die Thementitel für Ihr Inhaltsverzeichnis enthält. Wenn ein Benutzer das Inhaltsverzeichnis in einer kompilierten Hilfedatei (oder auf einer Webseite) öffnet und auf einen Thementitel klickt, wird die diesem Titel zugeordnete HTML-Datei geöffnet.

### Indexdatei
Die Indexdatei (.hhk) ist eine HTML-Datei, die die Indexeinträge (Schlüsselwörter) für Ihren Index enthält. Wenn ein Benutzer den Index in einer kompilierten Hilfedatei oder auf einer Webseite öffnet und auf ein Schlüsselwort klickt, wird die mit dem Schlüsselwort verknüpfte HTML-Datei geöffnet.

## HTML-Hilfekomponenten

Die HTML-Hilfe besteht aus mehreren Komponenten. Dazu gehören die folgenden:

* „HTML Help Workshop“: ein Hilfe-Entwicklungstool mit einer einfach zu bedienenden grafischen Oberfläche zum Erstellen von Projektdateien, HTML-Themendateien, Inhaltsdateien, Indexdateien und allem, was Sie sonst noch brauchen, um ein Online-Hilfesystem oder eine Website zusammenzustellen .
* `HTML Help ActiveX control`: ein kleines, modulares Programm, das verwendet wird, um Hilfe-Navigation und Sekundärfenster-Funktionalität in eine HTML-Datei einzufügen.
* `The HTML Help Viewer`: ein voll funktionsfähiges und anpassbares dreiteiliges Fenster, in dem Online-Hilfethemen erscheinen können.
* „Microsoft HTML Help Image Editor“: ein Online-Grafiktool zum Erstellen von Screenshots; und zum Konvertieren, Bearbeiten und Anzeigen von Bilddateien.
* `The HTML Help Java Applet`: ein kleines Java-basiertes Programm, das anstelle eines ActiveX-Steuerelements verwendet werden kann, um eine Hilfe-Navigation in eine HTML-Datei einzufügen.
* „Das ausführbare HTML-Hilfeprogramm“: Das Programm, das die Hilfe anzeigt und ausführt, wenn Sie auf eine kompilierte Hilfedatei klicken.
* „Der HTML-Hilfe-Compiler“: Das Programm, das Projekt-, Inhalts-, Index-, Themen- und andere Dateien in eine kompilierte Hilfedatei kompiliert.
* `The HTML Help Authoring Guide`: ein Online-Leitfaden, der entwickelt wurde, um Hilfeautoren bei der Verwendung von HTML Help zum Entwerfen eines Hilfesystems zu unterstützen. Das Handbuch enthält außerdem eine vollständige HTML-Hilfereferenz für Entwickler und eine HTML-Tag-Referenz für Autoren.

## Verweise

* [Microsoft HTML-Hilfe](https://docs.microsoft.com/en-us/ previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

