{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file RST - file di testo strutturato",
  "description":"Scopri il formato di file RST e le API che possono creare e aprire file RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Che cos'è un file RST?

Un file RST è un formato di file di documentazione tecnica, utilizzato principalmente nella comunità di programmazione Python. È un file di testo scritto nel linguaggio di markup reStructuredText che applica stili e formattazione a documenti di testo normale per la generazione di documentazione. I file RST utilizzano i commenti e altre informazioni nel codice dei programmi Python per creare documentazione tecnica dell'applicazione. Tuttavia, questi possono contenere anche testo che può essere convertito in semplici pagine Web e [eBook](/it/ebook/). Editor di testo come Github Atom, GNU Emacs (multipiattaforma), Microsoft Notepad (Windows), Apple TextEdit (Mac) e Vim (Linux) possono essere utilizzati per aprire file RST.

## Formato file RST

I file RST contengono codice scritto nel linguaggio di markup reStructuredText. Fa parte del progetto Docutils di Python Doc-SIG (Documentation Special Interest Group) che fornisce un insieme di strumenti per Python simili a Javadoc per Java. Il parser per il formato di file RST è incorporato in Docutils e può estrarre informazioni dai programmi Python per formattarli nella documentazione del programma.

### Esempio RST reStructuredText

Prendiamo un testo di esempio scritto in formato file RST come segue.

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

Quando questo testo viene immesso in un processore rST come Docutils, l'output è il seguente.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Riferimento ##

* [reStructuredText - di Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

