{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST-filformat - reStructuredText File",
  "description":"Läs mer om RST-filformat och API:er som kan skapa och öppna RST-filer.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Vad är en RST fil?

En RST-fil är ett filformat för teknisk dokumentation som främst används i Python-programmeringsgemenskapen. Det är en textfil skriven i märkningsspråket reStructuredText som tillämpar stilar och formatering på vanliga textdokument för generering av dokumentation. RST-filer använder kommentarerna och annan information i Python-programkoden för att skapa teknisk dokumentation av applikationen. Dessa kan dock också innehålla text som kan konverteras till enkla webbsidor och [e-böcker](/sv/ebook/). Textredigerare som Github Atom, GNU Emacs (plattformsoberoende), Microsoft Notepad (Windows), Apple TextEdit (Mac) och Vim (Linux) kan användas för att öppna RST-filer.

## RST filformat

RST-filer innehåller kod som är skriven i reStructuredText markup language. Det är en del av Docutils-projektet för Python Doc-SIG (Documentation Special Interest Group) som tillhandahåller en uppsättning verktyg för Python liknande Javadoc för Java. Parsern för RST-filformat är inbäddad i Docutils och kan extrahera information från Python-program för att formatera dem till programdokumentation.

### reStructuredText RST Exempel

Låt oss ta ett exempel på text skriven i RST-filformat enligt följande.

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

När den här texten matas in till en rST-processor som Docutils är utmatningen som följer.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referens ##

* [reStructuredText - av Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

