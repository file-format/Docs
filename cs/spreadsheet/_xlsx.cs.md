{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souboru, abyste věděli, co je soubor _XLSX a rozhraní API, která mohou vytvářet a otevírat soubory _XLSX.",
  "title" :"Co je soubor _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Co je soubor _XLSX?

Soubor s příponou .\_xlsx je ve skutečnosti soubor [XLSX](/cs/spreadsheet/xlsx/), který je přejmenován jinou aplikací. To se může stát v určitých případech, když název souboru obsahuje příponu . na konci názvu souboru. Soubory \_XLSX lze otevřít v aplikaci Microsoft Excel podobně jako soubory XLSX opětovným přejmenováním na příponu .xlsx.

## Formát souboru _XLSX – Další informace

Soubory _XLSX se neliší od souborů XLSX a používají standard Open XML přijatý společností Microsoft v roce 2000. Před XLSX byl [XLS](/cs/spreadsheet/xls/) primárním formátem souborů používaným pro práci s tabulkami aplikace Excel k ukládání dokumentů. v binárním formátu. Tento nový formát souborů založený na XML přišel s výhodami, jako jsou malé velikosti souborů, odolnost proti poškození souborů a dobře formátovaná reprezentace obrázků. Tento nový formát souborů založený na XML se stal součástí sady Office 2007 a funguje také v nových verzích Microsoftu.

## \_Specifikace formátu souboru XLSX

Protože soubor \_XLSX je přejmenovaný soubor XLSX, má stejné specifikace jako původní soubor. Je to pouze archivní soubor, který je založen na formátu archivního souboru [ZIP](/cs/compression/zip/). Chcete-li zobrazit obsah tohoto archivu, přejmenujte soubor na příponu .zip a rozbalte jej, abyste mohli zobrazit základní soubory tohoto sešitu aplikace Excel. Prázdný sešit, když je extrahován do svých souborů, má následující základní soubory a složky.

### [Content_Types].xml

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML.

### \_rels (složka)

Toto je složka Relationships, která obsahuje jeden soubor XML, ve kterém jsou uloženy vztahy na úrovni balíčku. Odkazy na klíčové části souborů Xlsx jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu dokumentu Office umístěnému jako xl/workbook.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.

### docProps

Tato složka obsahuje celkové vlastnosti dokumentu. Patří mezi ně sada základních vlastností, sada rozšířených vlastností nebo vlastností specifických pro aplikaci a miniaturní náhled dokumentu. Prázdný sešit má v této složce dva soubory, jmenovitě app.xml a core.xml. Core.xml obsahuje informace, jako je autor, datum vytvoření a uložení a úpravy. App.xml obsahuje informace o obsahu souboru.

### xl (složka)

Toto je hlavní složka, která obsahuje všechny podrobnosti o obsahu sešitu. Ve výchozím nastavení má následující složky:

* \_rels
* téma
* pracovní listy

a následující xml soubory:

* styly.xml
* sešit.xml

## Reference

* [MS-XLSX – formát souboru .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

