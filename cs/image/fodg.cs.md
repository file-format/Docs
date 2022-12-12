{
  "date" : "2019-10-11",
  "keywords" :[ "soubor fodg", "formát souboru fodg", "co je soubor fodg", "soubor", "příklad fodg", "přípona souboru fodg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - formát výkresového souboru OpenDocument",
  "description":"Další informace o formátu souborů FODG a rozhraních API, která mohou vytvářet a otevírat soubory FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor FODG?

Soubor s příponou .fodg je formát souboru výkresu Apache OpenOffice pro ukládání prvků výkresu. Je založen na specifikacích formátu souborů uvedených v Advancement of Structural Information Standards (OASIS). Dalším podobným formátem souborů pro grafiku OpenOffice je [ODG](/cs/image/odg/), který ukládá prvky výkresu jako vektorový obrázek. Soubory FODG lze otevřít pomocí OpenOffice i LibreOffice. Mezi další formáty souborů podporované OpenOffice patří například [ODT](/cs/textový procesor/odt/), ODF, [ODP](/cs/prezentace/odp/) a [ODS](/cs/tabulkový procesor/ods/).

## Formát souboru FODG

FODG je založeno na formátu souboru XML OpenDocument, který odpovídá formátu OASIS OpenDocument ISO/IEC 26300. Má Internet Media Type application/vnd.oasis.opendocument.graphics a také odpovídá org.oasis-open.opendocument public.composite-content . Struktura XML je společná pro všechny typy dokumentů, jako jsou tabulky, výkresové soubory a textové dokumenty. Dokumenty OpenOffice využívají oddělení problémů oddělením obsahu, stylů, metadat a nastavení aplikace do čtyř samostatných souborů XML.

`<office:document-content> ` - Obsah dokumentu a automatické styly použité v obsahu.
`<office:document-styles> ` - Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
`<office:document-meta> ` - Metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
`<office:document-settings> ` - Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

## Reference ##
* [Budoucí specifikace pro standardizaci verze 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Formát otevřených dokumentů OASIS pro aplikace Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formát OpenDocument – Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

