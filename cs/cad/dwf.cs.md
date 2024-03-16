{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Formát souboru", "Otevřít", "Číst", "Vytvořit", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů DWF a rozhraních API, která mohou vytvářet a otevírat soubory DWF.",
  "title" :"Formát souboru DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DWF?

Design Web Format (DWF) představuje 2D/3D výkres v komprimovaném formátu pro prohlížení, prohlížení nebo tisk souborů návrhů. Obsahuje grafiku a text jako součást dat návrhu a zmenšuje velikost souboru díky jeho komprimovanému formátu. Menší velikost souboru umožňuje efektivní distribuci a komunikaci bohatých návrhových dat. DWF nevyžaduje, aby příjemce věděl o použití softwaru CAD, který vytvořil původní výkres. Obsah souboru ve formátu DWF může být jednoduchý a může zahrnovat pouze jeden list nebo může být dostatečně složitý, aby obsahoval písma, barvy a obrázky.

## Stručná historie ##

Autodesk představil formát souborů DWF v roce 1995 jako součást zásuvného modulu Netscape Navigation, WHIP. Formát se vyvinul z formátu pouze 2D a postupem času zahrnoval 3D obsah. Mnoho aplikací třetích stran také využívá tento formát.

## Formát souboru DWF ##

DWF je otevřený, zabezpečený formát navržený speciálně pro sdílení bohatých konstrukčních návrhových dat. Je nezávislý na původním aplikačním softwaru, hardwaru a operačním systému použitém k vytvoření těchto návrhových dat. To umožňuje členům týmu, kteří nepoužívají aplikace CAD, podílet se na digitálních procesech prohlížením návrhů budov, GIS nebo produktů. Archiv souborů DWF se skládá z několika souborů XML a binárních souborů, které jsou společně zabaleny do komprimovaného archivu vytvořeného pomocí komprese [ZIP](/cs/compression/zip/). Příponu souboru DWF můžete přejmenovat na ZIP a zobrazit obsah souboru. Balíček DWF může obsahovat mnoho druhů dat návrhu, jako je 2D grafika, 3D grafika, metadata balíčku a řezu a další zdrojové soubory.

**Soubory metadat DWF** – soubory XML, které obsahují informace týkající se metadat a struktury (autor, název, čas vytvoření, závislosti sekcí, řazení sekcí, popisy zdrojových souborů, role, mimetypy atd.) a týkající se sekce (strana informace, metadata návrhu atd.). Strukturální metadata se používají k vytváření logických objektů (sbírek souborů reprezentujících část nebo stránku atd.).

**Soubory zdrojů** – soubory médií nebo jiného obsahu, na které se odkazuje z metadat balíčku/sekcí a obvykle jde o prezentace návrhových dat v různých formátech (ZGL, W2D, [JPG](/cs/image/jpeg/), [PNG](/cs/image/png/), AVI, XML, [TXT](/cs/word-processing/txt/), [DOC](/cs/word-processing/doc/) atd.)

### Podrobnosti o formátu souboru ###

Soubory DWF jsou uspořádány do tří hlavních sekcí, jak je uvedeno níže.

* Identifikační záhlaví souboru
* Blok dat souboru
* Upoutávka na ukončení souboru

#### Záhlaví identifikátoru souboru ####

Záhlaví identifikátoru souboru umožňuje identifikaci souborů DWF aplikacemi. Také identifikuje, která verze specifikací DWF byla použita pro kódování souboru. Jedná se o 12bajtové záhlaví, které je uspořádáno takto:


|Bajt|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Znak|(|D|W|F|(mezera)|V|0|0|.|3|0|)

Zde je shrnutí této tabulky:

* Prvních šest bajtů záhlaví vždy představuje znaky ASCII "(DWF V"
* Následujících 5 bajtů obsahuje informace o čísle verze, např. "00.30" s hodnotou hlavní a vedlejší verze formátu

Aplikace vytvářející soubor DWF by měly specifikovat nejnižší možné číslo verze, kterou musí čtecí aplikace podporovat, aby mohla data správně používat.

#### Blok dat souboru ####

Datový blok souboru začíná na 13. bajtu souboru DWF a je sérií párů operačních kódů a operandů, jak je uvedeno v následující tabulce.

|Pole 1|Pole 2|Pole 3|Pole 4|Pole 5|Pole 5
--- | --- |--- | --- |--- | --- |
|operand|operand|operand|operand|operand|operand

Soubor DWF může obsahovat páry operační kód-operand jako čitelné ASCII i binární kód nebo kombinaci obou. Všechny operace DWF mají čitelný ASCII tvar operačního kódu/operandu a většina operací má také kódovaný binární tvar operačního kódu/operandu. Operační kódy jsou v jednom byte, což umožňuje více než 200 operací. Rozšířené ASCII a rozšířené binární jsou výjimečné případy. Hodnoty operačních kódů se mohou s některými výjimkami pohybovat v rozmezí 0-255. Kromě dvou speciálních typů operačních kódů rozšířeného ASCII a rozšířeného binárního musí čtenář souborů vědět, jak vypočítat délku operandu.

##### Zakázané operační kódy #####

Reprezentace ASCII pro následující položky nelze použít jako operační kódy:

Následující reprezentace ASCII nelze použít jako operační kódy:

* Prostor (0x20)
* Tab (0x09)
* Spojovník (0x2D)
* ASCII číslice 0-9 (0x30 - 0x39)
* Návrat vozíku (0x0D)
* Posuv řádku (0x0A)
* Jednoduchá uvozovka (0x27)
* dvojité uvozovky (0x22)
* Období (0x2E)
* Závorky (0x28 a 0x29)
* Složené závorky (0x7B a 0x7D)
* Hranaté závorky (0x5B a 0x5D)
* Zpětné lomítko (0x5C)

#### Upoutávka na ukončení souboru ####

Upoutávka ukončení souboru pro DWF je jednoduše speciální operační kód označující konec souboru. Některé aplikace mohou po operačním kódu ukončení ukládat data jiná než DWF. Upoutávka je uvedena níže:


|Byt|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Postava|(|E|n|d|0|f|D|W|F|)

## Reference ##

* [DWF – z Wikipedie](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Datový formát WHIP](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

