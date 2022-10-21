{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "htm-Datei", "htm-Dateiformat", "htm-Dateityp", "Datei", "Typ", "was ist eine htm-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTM-Dateiformat",
  "description" :"Ihr Dateiformat-Leitfaden, um zu erfahren, was eine HTM-Datei und APIs sind, die sie erstellen und öffnen können.",
  "linktitle" :"HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine HTM-Datei?

Dateien mit der Erweiterung **.htm** stellen Hypertext Markup Language zum Erstellen von Webseiten zur Anzeige in Webbrowsern wie Google Chrome, Internet Explorer, Firefox und einigen anderen dar. Es definiert die Markups zum Erstellen statischer Seiten, die im World Wide Web (WWW) für den Zugriff durch andere veröffentlicht werden sollen. Diese Markups teilen den Browsern mit, wie der Inhalt einer Webseite angezeigt werden soll. Solche Seiten können reinen Text, Bilder, Hyperlinks zu anderen Seiten, Videos und andere Medieninformationen enthalten. Wenn eine Webseite veröffentlicht wird, können Sie sich den Markup-Code dahinter ansehen, indem Sie die Seitenquelle anzeigen. Moderne Browser ermöglichen es, jeden Abschnitt einer Webseite zu inspizieren, wo jede Unterteilung oder jedes Markup-Element in der HTM-Quelle ausgearbeitet ist.

## Kurze Geschichte von HTM

Seit ihrer Einführung und ersten Einführung werden die HTML-Spezifikationen seit 1996 vom World Wide Web Consortium (W3C) gepflegt. Im Jahr 2000 wurden sie auch zu einem internationalen Standard (ISO/IEC 15445:2000). 1999 wurde HTML 4.01 veröffentlicht. Im Jahr 2004 begann die Web Hypertext Application Technology Working Group (WHATWG) mit der Arbeit an der HTML5-Version, die 2008 zu einem gemeinsamen Ergebnis mit dem W3C wurde. Sie wurde am 28. Oktober 2014 fertiggestellt und standardisiert.

## HTML-Dateiformat

Ein HTML 4-Dokument besteht aus drei Teilen:

1. eine Zeile mit Informationen zur HTML-Version
1. einen deklarativen Header-Abschnitt
1. einen Körper, der den eigentlichen Inhalt des Dokuments enthält. Der Körper kann durch das BODY-Element oder das FRAMESET-Element implementiert werden, um den Körper in Rahmen einzuschließen

Jedem Abschnitt können Leerzeichen, Zeilenumbrüche, Tabulatoren und Kommentare vorangehen oder folgen. Ein Beispiel für ein einfaches HTML-Dokument sieht wie folgt aus:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versionsinformation

Die erste Codezeile,<!DOCTYPE html> , wird als Doctype-Deklaration bezeichnet und teilt dem Browser mit, in welcher HTML-Version die Seite geschrieben ist. Abhängig von der HTML-Version gibt es eine Reihe verschiedener Doctype-Deklarationen, die die für das Dokument verwendete Dokumenttypdefinition (DTD) benennen. Jede DTD unterscheidet sich von anderen in den Elementen, die sie unterstützt, und unterscheidet sich wie folgt:

* HTML 4.01 Strict – enthält alle Elemente und Attribute, die nicht [veraltet](https://www.w3.org/TR/html401/conform.html#deprecated) wurden oder nicht in Frameset-Dokumenten erscheinen
* HTML 4.01 Transitional - enthält alles in der strikten DTD sowie veraltete Elemente und Attribute (von denen die meisten die visuelle Darstellung betreffen
* HTML 4.01 Frameset - enthält alles in der Übergangs-DTD sowie Frames

Für **HTML5** sind die Versionsinformationen einfach wie unten angegeben.

```
<!DOCTYPE html>
```

### Header-Informationen

Der Header eines HTML-Dokuments kann eine Reihe von HTML-Elementen enthalten, die nicht vom Browser gerendert werden. Solche Elemente sind entweder Metadaten, die Informationen über die Seite beschreiben, oder enthalten Abschnitte, die zum Abrufen von Informationen aus externen Ressourcen wie CSS-Stylesheets oder JavaScript-Dateien verwendet werden. Die Kopfzeile einer Seite wird durch \ dargestellt<head> tag und endet mit \</head> Schild.

<html>Zum Festlegen des Seitentitels ist das \<title> -Element ist das einzige, das innerhalb der \<head>-Tags erforderlich ist. Dasselbe wird von Suchmaschinen verwendet, um den Titel einer Seite zu identifizieren. </html>

### Körperinformationen

Dies ist der Hauptabschnitt in der Datei, der alle Inhalte der Datei enthält, die von Browsern gerendert werden. Der HTML-Text kann Markups enthalten, die auf verschiedene Bausteine in Form von Tags verweisen können. Es kann verschiedene Arten von Informationen wie Text, Bilder, Farben, Grafiken usw. enthalten. Darüber hinaus können auch Audio- und Videoelemente in den HTML-Körper eingebettet werden, um von Browsern gerendert zu werden. In Gegenwart moderner Stylesheet-Anwendungen zur visuellen Darstellung wurden die Präsentationsattribute von BODY wie Hintergrundfarbe, Linkfarbe, Textfarbe usw. als veraltet markiert. Daher können die gleichen Effekte mit Stylesheets wie unten gezeigt erzielt werden:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Inline-Stylesheets lassen sich einfach einbetten, und für schnelle Anwendungen auf die visuellen Effekte erleichtern externe Stylesheets die einmalige Bereitstellung und den Zugriff an vielen Stellen.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML-Elemente

Wie bereits erwähnt, werden Inhalte im HTML-Body durch Tags dargestellt, die auch als HTML-Elemente bezeichnet werden. Jedes Tag kann zusätzliche Informationen in Form von Attributen haben, die geschrieben werden als
```
<tag attribute1#"value1" attribute2#"value2">
```
obwohl es nicht notwendig ist, Attribute mit jedem Tag zu haben. Wenn Attribute nicht genannt werden, werden jeweils Standardwerte verwendet. Im Folgenden sind einige Beispiele für Elemente aufgeführt:

#### Header

```
<head>
  <title>The Title</title>
</head>
```

#### Überschriften

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Absätze

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Verweise

* [Die globale Struktur des HTML-Dokuments](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

