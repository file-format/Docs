{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ kompilovaný zdrojový skript",
  "description":"Další informace o formátu souboru RES s příkladem RES a rozhraními API, která mohou vytvářet a otevírat soubory RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor RES?
Soubor s příponou .res nebo příponou může patřit do mnoha kategorií formátů souborů. Zde diskutujeme o formátu souboru RES, což je kompilovaný zdrojový skript C++; binární soubor vytvořený Microsoft Resource Compiler (rc), který obsahuje zdrojová data; na základě obsahu souboru s definicí prostředků; relevantní pro jeho nadřazený softwarový projekt. Soubor .res se obvykle přeformátuje na zdrojový objektový soubor, aby se propojil se spustitelným souborem aplikace.

## Formát souboru RES
Formát souboru RES patří do Microsoft Resource Compiler (rc). Kompilátor prostředků je nástroj, který kompiluje prostředky, jako jsou kurzory, ikony, nabídky a dialogová okna, které vaše aplikace používá. Zdrojové soubory mají obvykle příponu .res; obsahuje prostředky, jako jsou kurzory, obrázky a informace o verzi. Soubor RES může být 16bitový nebo 32bitový zdrojový soubor.
## Struktura souboru zdrojů
Soubor prostředků obsahuje řadu různých položek prostředků. Každý záznam obsahuje hlavičku zdroje a relevantní data. Záhlaví prostředku je obvykle v souboru zarovnáno DWORD a obsahuje následující:

- **DWORD** k určení velikosti záhlaví prostředku
- **DWORD** pro určení velikosti dat zdroje
- Typ zdroje
- Název zdroje
- Další informace o zdrojích

Struktura záhlaví zdroje definuje formát souboru RES. Data pro zdroj následují za hlavičkou zdroje. Některé prostředky také přidávají vzor záhlaví skupiny specifický pro prostředek, který poskytuje informace o skupině prostředků. Níže jsou uvedeny některé typy záznamů zdrojů a jejich popis:

### Zdroje tabulky akcelerátoru
Tabulka akcelerátoru je položka zdroje v souboru RES bez záhlaví skupiny. Vzor **ACCELTABLEENTRY** definuje každou položku v tabulce akcelerátorů. Soubor RES může mít více tabulek akcelerátorů.

### Zdroje kurzoru a ikon
Systém sice považuje každou ikonu a kurzor za jeden soubor, ale tyto jsou uloženy v souborech RES jako skupina prostředků ikony nebo skupina prostředků kurzoru. Formáty souborů ikon a kurzorových prostředků jsou stejné. Záhlaví skupiny prostředků následuje za všemi jednotlivými komponentami skupiny ikon nebo kurzorů v souboru .res.

### Zdroje dialogového okna
Dialogové okno je také realizováno jako záznam zdroje v souboru RES. Obsahuje jeden vzor záhlaví dialogového okna **DLGTEMPLATE** a jeden vzor **DLGITEMTEMPLATE** pro každý konkrétní ovládací prvek v dialogovém okně. Vzory **DLGTEMPLATEEX** a **DLGITEMTEMPLATEEX** vysvětlují formát zdrojů rozšířeného dialogového okna.

### Zdroje písem
Zdroj nabídky obsahuje vzor **MENUHEADER** a následně jeden nebo více vzorů **NORMALMENUITEM** nebo **POPUPMENUITEM**, jeden pro každou položku nabídky v šabloně nabídky. Vzory **MENUEX_TEMPLATE_HEADER** a **MENUEX_TEMPLATE_ITEM** vysvětlují formát zdrojů rozšířené nabídky.

### Zdroje tabulky zpráv
Tabulka zpráv se skládá z formátovaného textu, který se zobrazí jako chybová zpráva nebo v okně zprávy. Hlavním vzorem v prostředku tabulky zpráv je struktura **MESSAGE_RESOURCE_DATA**.

### Zdroje verze
Hlavním vzorem prostředku verze je **VS_FIXEDFILEINFO**. Mezi další vzory patří **VarFileInfo** pro ukládání dat souvisejících s jazykovými informacemi a **StringFileInfo** pro informace o vlastních řetězcích.




## Reference

* [Formáty zdrojových souborů](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



