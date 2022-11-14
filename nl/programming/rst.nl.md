{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST-bestandsindeling - reStructuredText-bestand",
  "description":"Meer informatie over RST-bestandsindeling en API's die RST-bestanden kunnen maken en openen.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Wat is een RST-bestand?

Een RST-bestand is een bestandsindeling voor technische documentatie, die voornamelijk wordt gebruikt in de Python-programmeergemeenschap. Het is een tekstbestand geschreven in de opmaaktaal reStructuredText die stijlen en opmaak toepast op platte tekstdocumenten voor het genereren van documentatie. RST-bestanden gebruiken de opmerkingen en andere informatie in de code van Python-programma's om technische documentatie van de toepassing te maken. Deze kunnen echter ook tekst bevatten die kan worden omgezet in eenvoudige webpagina's en [eBooks](/nl/ebook/). Teksteditors zoals Github Atom, GNU Emacs (cross-platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) en Vim (Linux) kunnen worden gebruikt om RST-bestanden te openen.

## RST-bestandsindeling

RST-bestanden bevatten code die is geschreven in de opmaaktaal reStructuredText. Het maakt deel uit van het Docutils-project van Python Doc-SIG (Documentation Special Interest Group) dat een reeks tools voor Python biedt die vergelijkbaar zijn met Javadoc voor Java. De parser voor het RST-bestandsformaat is ingebed in de Docutils en kan informatie uit Python-programma's extraheren om ze op te maken in programmadocumentatie.

### reStructuredText RST Voorbeeld

Laten we een voorbeeldtekst nemen die als volgt is geschreven in RST-bestandsindeling.

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

Wanneer deze tekst wordt ingevoerd in een rST-processor zoals Docutils, is de uitvoer als volgt.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referentie ##

* [reStructuredText - door Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

