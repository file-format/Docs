{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "soubor", "přípona", "formát souboru", "Soubor makra Microsoft Excel", "Tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souboru, abyste věděli, co je soubor maker XLM a rozhraní API, která mohou vytvářet a otevírat soubory XLM.",
  "title" :"Co je soubor XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor XLM?

XLM, pro Excel Macro, je typ tabulkových souborů, které se používají k ukládání maker. Z aplikačního hlediska je makro sada instrukcí, které se používají pro automatizaci procesů. Makro se používá k zaznamenání kroků, které jsou opakovaně prováděny pro formát souboru [XLS](/cs/tabulkový procesor/xls/) a usnadňuje provádění akcí opětovným spuštěním makra. Makra se programují pomocí jazyka Microsoft Visual Basic for Applications (VBA) ze sešitu aplikace Excel pomocí editoru jazyka Visual Basic a lze je spouštět/ladit přímo odtud.

## Stručná historie ##

Microsoft Excel podporoval programování maker od svého prvního veřejného spuštění. Funkce maker zůstaly stejné i přes další verze Excelu s rozšířením podle nových funkcí. XLM byl výchozí jazyk maker pro Excel až Excel 4.0. Excel 5.0 ve výchozím nastavení zaznamenával makra ve VBA, ale ve verzi 5.0 bylo nahrávání XLM stále povoleno jako možnost. Po verzi 5.0 byla tato možnost ukončena. Všechny verze Excelu, včetně Excelu 2010, jsou schopny spouštět makro XLM, i když Microsoft jejich použití nedoporučuje.

## Záznam makra v XLM ##

Excel poskytuje snadno použitelné kroky pro záznam makra. Chcete-li pracovat s makry, musíte mít nainstalované vývojářské nástroje. Jakmile je záznam makra v procesu, zaznamená každou akci uživatele, která se přehraje později. Makro záznam ve skutečnosti zahrnuje všechny kroky, které uživatel provede po zahájení záznamu. Pokud tedy obsah buňky označíte tučným písmem, kurzívou a nastavíte její zarovnání textu po spuštění záznamu makra, budou zaznamenány všechny tyto příkazy. Každému zaznamenanému makru lze přiřadit také zkratku pro pozdější rychlé přehrávání. Záznam maker generuje kód VBA ve formě makra, které lze upravovat pomocí editoru jazyka Visual Basic (VBE).

## Objektový model Excel ##

Makra používají rutiny VBA na zadní straně a pro tento účel se řídí [Objektový model Excel] (https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Tento model identifikuje objekty tabulky pro interakci s tabulkou prostřednictvím uživatelsky definovaných panelů nástrojů příkazů, panelů příkazů nebo zpráv. Například přístup k vlastnostem sešitu je udělen pomocí objektu Sešit. Podobně je v modelu objekt Worksheet pro programovou práci s listy sešitu.

## Makra a zabezpečení ##

VBA umožňuje přístup ke všem oblastem aplikace i souborovému systému a může být také nebezpečný. To vyvolává obavy při sdílení sešitu s někým, kdo může soubor spustit na jeho konci. To znamená, že aplikace Microsoft Excel varuje před otevřením takového souboru. Makra mohou být certifikována digitálním podpisem, aby si ostatní uživatelé ověřili, že jsou důvěryhodná. Makra lze tedy povolit po ověření jejich zdroje.

## Reference ##

* [[MS-XLS] – struktura binárního formátu souboru Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programování maker](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

