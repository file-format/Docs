{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier RST – fișier text reStructurat",
  "description":"Aflați despre formatul de fișier RST și despre API-urile care pot crea și deschide fișiere RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Ce este un fișier RST?

Un fișier RST este un format de fișier de documentație tehnică, utilizat în principal în comunitatea de programare Python. Este un fișier text scris în limbajul de marcare reStructuredText care aplică stiluri și formatare documentelor text simplu pentru generarea documentației. Fișierele RST folosesc comentariile și alte informații din codul programelor Python pentru a crea documentația tehnică a aplicației. Totuși, acestea pot conține și text care poate fi convertit în pagini web simple și [eBooks](/ro/ebook/). Pentru a deschide fișiere RST pot fi utilizate editori de text precum Github Atom, GNU Emacs (multplatform), Microsoft Notepad (Windows), Apple TextEdit (Mac) și Vim (Linux).

## Format de fișier RST

Fișierele RST conțin cod care este scris în limbajul de marcare reStructuredText. Face parte din proiectul Docutils al Python Doc-SIG (Documentation Special Interest Group) care oferă un set de instrumente pentru Python similar cu Javadoc pentru Java. Analizatorul pentru formatul fișierului RST este încorporat în Doctils și poate extrage informații din programele Python pentru a le formata în documentația programului.

### reStructuredText RST Exemplu

Să luăm un exemplu de text scris în format de fișier RST, după cum urmează.

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

Când acest text este introdus într-un procesor rST, cum ar fi Doctils, rezultatul este după cum urmează.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referință ##

* [reStructuredText - de Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

