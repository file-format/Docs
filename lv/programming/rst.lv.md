{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RST faila formāts - restrukturēta teksta fails",
  "description": "Uzziniet par RST faila formātu un API, kas var izveidot un atvērt RST failus.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-lvt"
}
},
  "lastmod": "2022-04-11"
}

## Kas ir RST fails?

RST fails ir tehniskās dokumentācijas faila formāts, ko galvenokārt izmanto Python programmēšanas kopienā. Tas ir teksta fails, kas rakstīts reStructuredText iezīmēšanas valodā, kas izmanto stilus un formatējumu vienkārša teksta dokumentiem dokumentācijas ģenerēšanai. RST faili izmanto komentārus un citu informāciju Python programmu kodā, lai izveidotu lietojumprogrammas tehnisko dokumentāciju. Tomēr tajos var būt arī teksts, ko var pārvērst vienkāršās tīmekļa lapās un [eBooks](/ebook/). Lai atvērtu RST failus, var izmantot tādus teksta redaktorus kā Github Atom, GNU Emacs (starpplatformu), Microsoft Notepad (Windows), Apple TextEdit (Mac) un Vim (Linux).

## RST faila formāts

RST faili satur kodu, kas rakstīts reStructuredText iezīmēšanas valodā. Tā ir daļa no Python Doc-SIG (Dokumentācijas īpašās interešu grupas) projekta Docutils, kas nodrošina Python rīku komplektu, kas ir līdzīgs Javadoc for Java. RST faila formāta parsētājs ir iegults programmā Docutils un var iegūt informāciju no Python programmām, lai tās formatētu programmas dokumentācijā.

### reStructuredText RST piemērs

Ņemsim teksta piemēru, kas rakstīts RST faila formātā, kā norādīts tālāk.

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

Kad šis teksts tiek ievadīts rST procesorā, piemēram, Docutils, izvade ir šāda.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Atsauce Nr.

* [ReStructuredText — Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)


