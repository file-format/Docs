{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RST-filformat- reStructuredText-fil",
  "description": "Lær om RST-filformat og API'er, der kan oprette og åbne RST-filer.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-dat"
}
},
  "lastmod": "2022-04-11"
}

## Hvad er en RST fil?

En RST-fil er et teknisk dokumentationsfilformat, der primært bruges i Python-programmeringsfællesskabet. Det er en tekstfil skrevet i reStructuredText markup-sproget, der anvender stilarter og formatering på almindelige tekstdokumenter til generering af dokumentation. RST-filer bruger kommentarerne og andre oplysninger i Python-programmernes kode til at oprette teknisk dokumentation for applikationen. Disse kan dog også indeholde tekst, der kan konverteres til simple websider og [eBooks](/ebook/). Teksteditorer som Github Atom, GNU Emacs (cross-platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) og Vim (Linux) kan bruges til at åbne RST-filer.

## RST filformat

RST-filer indeholder kode, der er skrevet i reStructuredText markup-sprog. Det er en del af Docutils-projektet af Python Doc-SIG (Documentation Special Interest Group), der giver et sæt værktøjer til Python, der ligner Javadoc til Java. Parseren til RST-filformatet er indlejret i Docutils og kan udtrække information fra Python-programmer for at formatere dem til programdokumentation.

### reStructuredText RST Eksempel

Lad os tage et eksempel på tekst skrevet i RST-filformat som følger.

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

Når denne tekst indlæses til en rST-processor, såsom Docutils, er outputtet som følger.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Reference ##

* [reStructuredText - af Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)


