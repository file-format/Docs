{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "tillägg", "fil", "format", "serietidningar", "serietidningar filformat", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om CBC-filformat och API:er som kan skapa och öppna CBC-filer.",
  "title" :"CBC - Comic Book Collection File Format",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Vad är en CBC fil?

En fil med filtillägget .cbc är en komprimerad samling av serietidningsfiler för e-böcker och innehåller filerna [CBZ](/sv/ebook/cbz/) och [CBR](/sv/ebook/cbr/). Den används av [Calibre](https://calibre-ebook.com/), en eBook-konverteringsapplikation, som är en plattformsoberoende öppen källkodshantering för e-böcker och låter dig hantera dina e-böcker och konvertera dessa till olika format . En CBC-fil innehåller en .txt-fil, comics.txt, som listar andra filer som är en del av arkivet. Det finns flera applikationer online som kan konvertera CBC-filer till [AZW3](/sv/ebook/azw3/), [EPUB](/sv/ebook/epub/), [FB2](/sv/ebook/fb2/), [MOBI](/sv/ebook/ mobi/), [TXT](/sv/word-processing/txt/), [PDF](/sv/pdf/) och andra populära filformat.

## CBC filformat

CBC-filer är komprimerade arkiv som innehåller CBZ, CBR och en textfil för att lista innehållet. Textfilen comics.txt är UTF8-kodad och innehåller en lista över de CBC-filer som ska användas av läsare för att organisera sina samlingar. En CBC-fil har vanligtvis flera attribut som tillåter organisationen av den här samlingen, såsom Comic, Category, Publisher, Series, Edition och Artist.

Innehållet i en CBC-exempel-fil listas enligt följande:

* comics.txt - Textfil som innehåller en lista över CBR- och CBZ-filer
* 1.cbz
* 2.cbz
* 3.cbz
* CBZ-fil(er)

där comics.txt-filen listar innehållet enligt följande:

* 1.cbz: Första kapitlet
* 2.cbz: Andra kapitlet
* 3.cbz: Tredje kapitlet

Läsare bearbetar filen comics.txt och genererar innehållsförteckningen baserat på de angivna uppgifterna.

## Referenser

* [Calibre](https://calibre-ebook.com/)

