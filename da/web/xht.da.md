{
  "date": "2021-05-24",
  "keywords": [
"xht",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"udvidet hypertekst markup sprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHT",
  "description": "Lær om XHT-filformat og API'er, der kan oprette og åbne XHT-filer.",
  "linktitle": "XHT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xh-dat"
}
},
  "lastmod": "2021-05-24"
}

## Hvad er en XHT fil?

En fil med filtypen .xht er en webfil, der er knyttet til filtypen [XHTML](/web/xhtml/) (Extended Hypertext Markup Language), som i sig selv er en [XML](/web/xml/)-baseret markup-fil. Begge disse filer ligner HTML, men har en mere stringent XML-lignende syntaks. XHT-filer er designet på en måde, så de er mere strukturerede, involverer mindre scripting og er generiske ud over at bruge de eksisterende faciliteter i XML.

## XHT filformat

En XHT-fil oprettes og gemmes som en almindelig tekstfil med UTF-8-kodning som standard. Den indeholder den komplette kildekode til et XHTML-dokument, der kan åbnes og redigeres med enhver teksteditor, der understøtter Unicode-kodning. Ud over teksteditorer er XHT-filformat forståeligt af de fleste af de moderne webbrowsere og kan åbnes ved hjælp af disse.

## XHT eksempel

Følgende eksempel på et XHT-dokument definerer XML-deklarationerne.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Referencer ##

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


