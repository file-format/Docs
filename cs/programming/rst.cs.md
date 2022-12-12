{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru RST-reStructuredText File",
  "description":"Další informace o formátu souboru RST a rozhraních API, která mohou vytvářet a otevírat soubory RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Co je soubor RST?

Soubor RST je formát souboru technické dokumentace, který se používá především v programovací komunitě Pythonu. Jedná se o textový soubor napsaný ve značkovacím jazyce reStructuredText, který aplikuje styly a formátování na dokumenty ve formátu prostého textu pro generování dokumentace. Soubory RST používají komentáře a další informace v kódu programů Python k vytvoření technické dokumentace aplikace. Mohou však také obsahovat text, který lze převést na jednoduché webové stránky a [e-knihy](/cs/ebook/). K otevření souborů RST lze použít textové editory, jako je Github Atom, GNU Emacs (pro více platforem), Microsoft Notepad (Windows), Apple TextEdit (Mac) a Vim (Linux).

## Formát souboru RST

Soubory RST obsahují kód, který je napsán ve značkovacím jazyce reStructuredText. Je součástí projektu Docutils Pythonu Doc-SIG (Documentation Special Interest Group), který poskytuje sadu nástrojů pro Python podobně jako Javadoc pro Javu. Analyzátor pro formát souboru RST je zabudován v Docutils a může extrahovat informace z programů Python pro jejich formátování do dokumentace programu.

### reStructuredText Příklad RST

Vezměme si příklad textu napsaného ve formátu souboru RST následovně.

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

Když je tento text vložen do procesoru rST, jako je Docutils, výstup je následující.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## reference ##

* [reStructuredText – od Wikipedie](https://en.wikipedia.org/wiki/ReStructuredText)

