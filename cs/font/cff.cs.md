{
  "date" : "2020-08-20",
  "keywords" :[ "soubor cff", "formát souboru cff", "co je soubor cff", "soubor", "příklad cff", "přípona souboru cff", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Kompaktní formát souboru písem",
  "description":"Další informace o formátu souborů CFF a rozhraních API pro vytváření a otevírání souborů CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Co je soubor CFF?

Soubor s příponou .cff je kompaktní formát písma a je také známý jako PostScript Type 1 nebo CIDFont. CFF funguje jako kontejner pro ukládání více písem dohromady v jedné jednotce známé jako FontSet. Návrh písem CFF umožňuje vkládání kódu jazyka PostScript, který umožňuje další flexibilitu a rozšiřitelnost formátu pro použití v prostředí tiskárny. Soubory písem CFF lze otevřít a převést pomocí rozhraní API, jako je [Aspose.Font] (https://products.aspose.com/font).

## Formát souboru CFF

Soubory CFF jsou binární soubory, které obsahují strukturované rozložení dat, mají definované datové typy, záhlaví, organizaci glyfů a slovníky tabulek. Další podrobnosti o nich lze nalézt ve [specifikacích formátu kompaktního písma] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Rozložení dat
Rozložení dat formátu souboru CFF je znázorněno níže.

|Příspěvek|Komentáře|
---|---|
|Záhlaví|–|
|JménoINDEX|–|
|Top DICT INDEX|–|
|Řetězec INDEX|–|
|Globální dílčí INDEX|–|
|Kódování–Znakové sady|–|
|FDSelect|CIDFonts only|
|CharStrings INDEX|za-font|
|Písmo DICT INDEX|pro písmo, pouze CIDFfonty|
|Soukromé DICT|pro písmo|
|Místní dílčí INDEX|pro písmo nebo soukromé DICT pro CIDFonts|
|Oznámení o autorských právech a ochranných známkách|–|

### Typy dat

Datové typy CFF jsou uvedeny v následující tabulce.

|Název|Rozsah|Popis|
---|---|---|
|Karta8|0 –255|1bajtové číslo bez znaménka|
|Karta16|0 – 65535|2bajtové číslo bez znaménka|
|Offset|různé|1, 2, 3 nebo 4 byte offset (určeno polem OffSize)|
|OffSize|1–4|1bajtové číslo bez znaménka určuje velikost pole nebo polí Offset|
|SID|0 – 64999|2bajtový identifikátor řetězce|

### Záhlaví

Binární data začínají záhlavím ve formátu uvedeném v následující tabulce.

|Typ|Název|Popis|
---|---|---|
|Karta8|hlavní|Formátovat hlavní verzi (počínaje 1)|
|Karta8|vedlejší|Formátovat vedlejší verzi (počínaje 0)|
|Karta8|Velikost hdr| Velikost záhlaví (bajty)|
|OffSize|offSize|Absolutní offset (0) velikost|

## Reference

* [Tabulka kompaktních formátů písem](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Formát souboru CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

