{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "soubor", "přípona", "formát souboru", "Excel", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů OTS a rozhraních API, která mohou vytvářet a otevírat soubory OTS.",
  "title" :"OTS - Formát souboru šablony OpenDocument Spreadsheet Template",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Co je soubor OTS?

Soubor s příponou .ots je soubor šablony OpenDocument Spreadsheet Template, který je vytvořen pomocí aplikačního softwaru Calc, který je součástí Apache OpenOffice. Aplikační software Calc je obdobou Excelu dostupného v Microsoft Office. Formát souboru OTS se používá k vytváření šablon, které obsahují předdefinovaná nastavení týkající se stylů, písma, dat, rozložení tabulky a formátování. Soubory OTF mají `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Tyto soubory šablon lze použít jako výchozí bod pro generování a ukládání skutečných datových souborů, které jsou uloženy ve [formát souboru ODS](/cs/spreadsheet/ods/). Soubory OTS lze používat s aplikacemi, jako jsou OpenOffice a LibreOffice.

## Formát souboru OTS

Soubory OTS jsou uloženy ve formátu souboru OASIS OpenDocument založeném na XML, který se skládá z kolekce několika dílčích dokumentů s balíčkem jako archiv [ZIP](/cs/compression/zip/). Každý archiv zip ukládá část celého dokumentu a každý vnořený dokument ukládá konkrétní aspekt dokumentu. Například jeden vnořený dokument obsahuje informace o stylu a jiný vnořený dokument obsahuje obsah dokumentu. Typický dokument ODF má následující součásti:

### Obsah OTS.xml

Soubor content.xml obsahuje skutečný obsah dokumentu. To však nezahrnuje binární data, jako jsou obrázky.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml formátu souboru OTS

Soubor styles.xml obsahuje informace o stylu a hojně se používá pro formátování a rozvržení. Mezi typy stylů patří:

* Styly odstavců
* Styly stránek
* Styly postav
* Styly rámů
* Seznam stylů

### Meta.xml

Soubor meta.xml obsahuje informace o metadatech souboru, jako je Autor, Datum poslední změny atd.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Soubor `settings.xml` obsahuje nastavení na úrovni dokumentu, jako je faktor přiblížení a pozice kurzoru.

## Reference ##

* [Specifikace OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

