{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RST failo formatas – restruktūrizuoto teksto failas",
  "description": "Sužinokite apie RST failo formatą ir API, kurios gali kurti ir atidaryti RST failus.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-ltt"
}
},
  "lastmod": "2022-04-11"
}

## Kas yra RST failas?

RST failas yra techninės dokumentacijos failo formatas, daugiausia naudojamas Python programavimo bendruomenėje. Tai tekstinis failas, parašytas reStructuredText žymėjimo kalba, kuris taiko stilius ir formatavimą paprasto teksto dokumentams, kad būtų sukurta dokumentacija. RST failai naudoja Python programų kode esančius komentarus ir kitą informaciją, kad sukurtų techninę programos dokumentaciją. Tačiau juose taip pat gali būti teksto, kurį galima konvertuoti į paprastus tinklalapius ir [eBooks](/ebook/). RST failams atidaryti galima naudoti tokius teksto redaktorius kaip Github Atom, GNU Emacs (keli platforma), Microsoft Notepad (Windows), Apple TextEdit (Mac) ir Vim (Linux).

## RST failo formatas

RST failuose yra kodas, parašytas reStructuredText žymėjimo kalba. Tai yra Python Doc-SIG (Specialios dokumentacijos grupės) projekto Docutils dalis, teikianti Python įrankių rinkinį, panašų į Javadoc for Java. RST failo formato analizatorius yra įdėtas į Docutils ir gali išgauti informaciją iš Python programų, kad suformatuotų jas į programos dokumentaciją.

### reStructuredText RST pavyzdys

Paimkime pavyzdinį tekstą, parašytą RST failo formatu, kaip nurodyta toliau.

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

Kai šis tekstas įvedamas į rST procesorių, pvz., Docutils, išvestis yra tokia.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Nuoroda ##

* [ReStructuredText – pateikė Vikipedija](https://en.wikipedia.org/wiki/ReStructuredText)


