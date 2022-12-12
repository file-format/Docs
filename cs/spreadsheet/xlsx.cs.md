{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "soubor", "přípona", "formát souboru", "Excel", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Zjistěte, co je soubor XLSX a rozhraní API, která mohou vytvářet a otevírat soubory XLSX.",
  "title" :"Formát souboru XLSX - Co je soubor XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor XLSX?

**XLSX** je dobře známý formát pro dokumenty Microsoft Excel, který zavedla společnost Microsoft s vydáním sady Microsoft Office 2007. Na základě struktury organizované podle úmluv o otevřeném balení, jak je uvedeno v [části 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) standardu OOXML ECMA-376, nový formát je balíček zip, který obsahuje řadu souborů XML. Základní strukturu a soubory lze prozkoumat jednoduchým rozbalením souboru .xlsx.

## Stručná historie formátu souboru XLSX

Formát souboru XLSX byl představen v roce 2007 a používá standard Open XML upravený společností Microsoft již v roce 2000. Před XLSX byl běžným používaným formátem souboru [XLS](/cs/spreadsheet/xls/), což byl čistě binární formát souboru. Nový typ souboru přidal výhody malých velikostí souborů, méně změn poškození a dobře formátované reprezentace obrázků. Bylo to počátkem roku 2000, kdy se Microsoft rozhodl přistoupit ke změně, aby vyhovoval standardu pro **Office Open XML**. V roce 2007 se tento nový formát souborů stal součástí sady Office 2007 a je používán i v nových verzích sady Microsoft Office.

## Specifikace formátu souboru XLSX

Oficiální [specifikace formátu souboru XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) jsou k dispozici online od společnosti Microsoft. Chcete-li vidět, co je uvnitř souboru XLSX, stačí jej přejmenovat na soubor [ZIP](/cs/compression/zip/) změnou jeho přípony a poté jej rozbalit, abyste mohli zobrazit základní soubory tohoto sešitu aplikace Excel. Prázdný sešit, když je extrahován do svých souborů, má následující základní soubory a složky.

### [Content_Types].xml ###

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML.

### \_rels (složka) ###

Toto je složka Relationships, která obsahuje jeden soubor XML, ve kterém jsou uloženy vztahy na úrovni balíčku. Odkazy na klíčové části souborů Xlsx jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu dokumentu Office umístěnému jako xl/workbook.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.

### docProps ###

Tato složka obsahuje celkové vlastnosti dokumentu. Patří mezi ně sada základních vlastností, sada rozšířených vlastností nebo vlastností specifických pro aplikaci a miniaturní náhled dokumentu. Prázdný sešit má v této složce dva soubory, jmenovitě app.xml a core.xml. Core.xml obsahuje informace, jako je autor, datum vytvoření a uložení a úpravy. App.xml obsahuje informace o obsahu souboru.

### xl (složka) ###

Toto je hlavní složka, která obsahuje všechny podrobnosti o obsahu sešitu. Ve výchozím nastavení má následující složky:

* \_rels
* téma
* pracovní listy

a následující xml soubory:

* styly.xml
* sešit.xml

## Příklad formátu XLSX ##


Pro každý list aplikace Excel obsažený v sešitu existuje jeden soubor XML. Tyto soubory XML najdete ve složce xl/worksheets. Všechny informace obsažené v listu jsou uspořádány v různých částech souboru XML. Podívejme se na ukázkový pracovní list ze sešitu, který je znázorněn na následujícím obrázku.

{{< figure src="../XLSX file format.png" alt="Formát souboru XLSX" >}}

Jak je vidět, tento list obsahuje obsah v buňkách A1 až B2 a obrázek. Kromě toho je buňka G13 aktuálně aktivní buňkou v listu. Nyní se podívejme na soubor xl/worksheets/sheet1.xml, abychom viděli, jak jsou tyto informace reprezentovány v souboru XML. Obsah tohoto souboru XML je uveden níže.

{{< figure src="../XLSX File Format Details.png" alt="Formát souboru XPS" >}}

1. Karta má barvu motivu. Je to zmíněno v souboru XML s tagem<tabColor> podle id tématu.
1. Hodnota tabSelected je nastavena na 1, což ukazuje, že se jedná o vybraný list
1. Jak je vidět na prvním obrázku výše, buňka G13 v listu je aktivní buňkou, která je také zmíněna v souboru XML.
1. Karta sheetData představuje data obsažená v listu. Můžete však vidět, že původní obsah listu není nikde v této části. Je to proto, že text je nepřímo odkazován z listu XML „sharedStrings“. Toto propojení zajišťuje, že každý text je uložen pouze jednou a lze na něj znovu odkazovat, aby se ušetřilo místo.
1. Na obrázek, jak je vidět, odkazuje referenční id "rId2"

## Přispět

Potřebujete se podělit o něco o formátech souborů XLSX nebo Tabulkový procesor? Svá zjištění můžete zveřejnit v sekci [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Reference

* [[MS-XLSX] – formát souboru XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

