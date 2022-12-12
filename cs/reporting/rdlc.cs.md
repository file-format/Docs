{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC – klientská strana jazyka sestavy",
  "keywords" :[ "rdlc", "jazyk definice sestavy", "formát mkv", "XSD", "klientská strana jazyka definice sestavy"],
  "description":"Další informace o formátu souboru RDLC, což je reprezentace XML definice sestavy SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Co je soubor RDLC? ##

RDLC je zkratka pro Report Definition Language Client side. Ve skutečnosti se jedná o rozšíření souboru sestavy vytvořené pomocí technologie vytváření sestav společnosti Microsoft. K vytvoření těchto souborů se používá verze SQL Server 2005 Návrháře sestav. Ovládací prvek **ReportViewer** na straně klienta může přímo spouštět zprávy RDLC.

## Soubory RDL VS RDLC
|.rdl soubory |.rdlc soubory|
---|---|
|Soubory RDL jsou vytvářeny verzí Návrháře sestav pro SQL Server 2005|Soubory RDLC jsou vytvářeny verzí Návrháře sestav pro Visual Studio 2005|
|Používá se v SQL Server Reporting Services|Používá se v sadě Visual Studio|
|Je to vzdálená zpráva|Je to místní zpráva|
|K jejímu spuštění je potřeba instance Reporting Services|Není potřeba instance Reporting Services|

## Vytváření souborů definice klientské sestavy (.rdlc).
Ovládací prvek ReportViewer se používá ke spouštění souborů definice klientské sestavy (.rdlc) pomocí vestavěné schopnosti zpracování ovládacího prvku. Klientské sestavy, které spustíte v režimu místního zpracování, lze snadno vytvořit v projektu aplikace. Níže jsou uvedeny přístupy k vytvoření přehledu:

- Pomocí **Průvodce sestavou** vytvořte novou definici klientské sestavy (.rdlc).

- Vytvořte nový soubor definice klientské sestavy (.rdlc) pomocí sady Visual Studio.

- Programově vygenerujte definici sestavy.


Náhled sestavy můžete zobrazit pouze jejím spuštěním v ovládacím prvku **ReportViewer**. Vezměte prosím na vědomí, že definici sestavy můžete kdykoli otevřít a upravit a poté sestavit nebo nasadit aplikaci a zkontrolovat výsledky.

## Reference ##

- [Vytváření souborů definice klientských sestav (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

