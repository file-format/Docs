{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST-Dateiformat - reStructuredText-Datei",
  "description":"Erfahren Sie mehr über das RST-Dateiformat und APIs, die RST-Dateien erstellen und öffnen können.",
  "linktitle" :"RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Was ist eine RST-Datei?

Eine RST-Datei ist ein Dateiformat für technische Dokumentation, das hauptsächlich in der Python-Programmiergemeinschaft verwendet wird. Es handelt sich um eine Textdatei, die in der Markup-Sprache reStructuredText geschrieben ist und Stile und Formatierungen auf reine Textdokumente anwendet, um eine Dokumentation zu erstellen. RST-Dateien verwenden die Kommentare und andere Informationen im Python-Programmcode, um eine technische Dokumentation der Anwendung zu erstellen. Diese können aber auch Text enthalten, der sich in einfache Webseiten und [eBooks](/de/ebook/) umwandeln lässt. Texteditoren wie Github Atom, GNU Emacs (plattformübergreifend), Microsoft Notepad (Windows), Apple TextEdit (Mac) und Vim (Linux) können zum Öffnen von RST-Dateien verwendet werden.

## RST-Dateiformat

RST-Dateien enthalten Code, der in der Auszeichnungssprache reStructuredText geschrieben ist. Es ist Teil des Docutils-Projekts von Python Doc-SIG (Documentation Special Interest Group), das eine Reihe von Tools für Python bereitstellt, die Javadoc für Java ähneln. Der Parser für das RST-Dateiformat ist in die Docutils eingebettet und kann Informationen aus Python-Programmen extrahieren, um sie in die Programmdokumentation zu formatieren.

### reStructuredText RST-Beispiel

Nehmen wir einen im RST-Dateiformat geschriebenen Beispieltext wie folgt.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Wenn dieser Text in einen rST-Prozessor wie Docutils eingegeben wird, sieht die Ausgabe wie folgt aus.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Bezug ##

* [reStructuredText - von Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

