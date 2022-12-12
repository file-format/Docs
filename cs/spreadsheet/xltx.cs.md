{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "soubor", "rozšíření", "formát souboru", "Excel Open XML", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souborů, abyste věděli, co je soubor XLTX a rozhraní API, která je mohou vytvářet a otevírat.",
  "title" :"Co je soubor XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor XLTX?

Soubory s příponou .xltx představují soubory šablon Microsoft Excel, které jsou založeny na specifikacích formátu souborů Office OpenXML. Používá se k vytvoření standardního souboru šablony, který lze použít ke generování souborů [XLSX](/cs/spreadsheet/xlsx/), které vykazují stejná nastavení jako v souboru XLTX.

## Stručná historie

Bylo to počátkem roku 2000, kdy se Microsoft rozhodl přistoupit ke změně, aby vyhovoval standardu pro **Office Open XML**. Dokumenty různých typů podle tohoto nového standardu byly identifikovány připojením "X" v jejich rozšíření, kde "X" je pro XML. V roce 2007 se tento nový formát souborů stal součástí sady Office 2007 a je používán i v nových verzích sady Microsoft Office. Nový typ souboru přidal výhody malých velikostí souborů, méně změn poškození a dobře formátované reprezentace obrázků.

## Specifikace formátu souboru XLTX

Soubory XLTX jsou založeny na formátu souborů Office OpenXML a ke zmenšení velikosti souboru používají XML a [ZIP](/cs/compression/zip/). Byl vytvořen s vydáním sady Microsoft Office 2007, aby nahradil binární formát souboru XLT. Podobně jako u XLTX lze formát souboru XLT použít k vytvoření souborů [XLS](/cs/spreadsheet/xls/) pomocí Microsoft Excel 2003 a 2007. Tyto lze otevřít v aplikaci Microsoft Excel dvojitým kliknutím na soubor. Uspořádání souborů ve formátu souboru XLTX lze sledovat přejmenováním souboru na ZIP a následným rozbalením jeho obsahu na disk.

### [Content_Types].xml ###

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML.

### \_rels (složka) ###

Toto je složka Relationships, která obsahuje jeden soubor XML, ve kterém jsou uloženy vztahy na úrovni balíčku. Odkazy na klíčové části souborů Xltx jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu dokumentu Office umístěnému jako xl/workbook.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.

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

## Reference ##

* [[MS-XLSX] – Formát souboru .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

