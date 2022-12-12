{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Přípona souboru INC - Co je soubor INC?",
  "description":"Další informace o formátu souboru INC Include a rozhraních API, která mohou vytvářet a otevírat soubory INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Co je soubor INC?

Soubor INC je začleněný soubor, který používá zdrojový kód softwarového programu k odkazování na informace v záhlaví. Je podobný [formátu souboru .h](/cs/programming/h/) a obsahuje deklarace, funkce, hlavičky nebo makra, která mohou být znovu použita soubory zdrojového kódu, jako je C++. Soubory INC používají různé programovací jazyky, jako je C, [C++](/cs/programming/cpp/), Pascal, [PHP](/cs/programming/php/) a [Java](/cs/programming/java/). K otevření souborů INC lze použít textové editory, jako je Microsoft Notepad, Notepad++ a TextEdit.

## Formát souboru INC – Další informace

Soubor INC se uloží jako prostý textový soubor se všemi deklaracemi zahrnutými podle syntaxe deklarace. Jeden soubor INC může odkazovat i na jiné soubory INC. Po vytvoření se soubor INC stane součástí projektu a lze na něj odkazovat ze zdrojových souborů, jako je C++. Lze na něj odkazovat více zdrojovými soubory, aby se předešlo duplicitě.

## Obsah souboru INC

Soubory INC mohou obsahovat následující informace.

**`Proměnné`** – V případě objektově orientovaného programování (OOP) obsahuje soubor záhlaví třídy definice všech proměnných na úrovni třídy, které jsou přístupné napříč soubory zdrojového kódu implementace.

**`Deklarace metod`** - Všechny deklarace metod jsou zahrnuty v hlavičkových souborech .h, aby byly přístupné ve více souborech implementace.

**`Definice neinline funkcí`** - Soubory záhlaví mohou také obsahovat definice neinline metod.

## Nevýhoda použití INC souboru v PHP

PHP jsou skripty na straně serveru, které běží na serveru a vracejí výsledky na volající webové stránky. Pokud soubor PHP odkazuje na soubor INC a server není nakonfigurován k analýze souborů .inc (což je velmi běžné), uživatel může zobrazit zdrojový kód php v souboru .inc návštěvou adresáře URL. Při používání souborů INC jako začleněných souborů v PHP je tedy třeba být opatrný.

## Reference

* [Používání INC v PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

