{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Mar - Microsoft Access Reports File",
  "keywords" :[ "mar", "soubor mar", "formát souboru mar", "co je zpráva o přístupu", "zpráva o přístupu", "zpráva o přístupu společnosti Microsoft"],
  "description":"Další informace o formátu souboru Acess Report (MAR), který používá software Microsoft Access k vytvoření zástupce nebo odkazu na Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Co je zpráva o přístupu (soubor MAR)? ##
Soubor vytvořený aplikací Microsoft Access jako zástupce jeho sestavy je uložen s příponou .mar. **Sestava Microsoft Access** nabízí způsob formátování, zobrazení a shrnutí informací v databázi Microsoft Access. Tyto sestavy vám umožňují formátovat data v přesném a informativním uspořádání pro zobrazení na obrazovce nebo tisk. Sestava zobrazuje pouze statická data, což znamená, že při prohlížení sestavy Access nemůžeme data v tabulkách měnit. Při otevření sestavy se zobrazí nejnovější data.

## Formát souboru Microsoft Access Report (Mar).

Formát souboru MAR používá software Microsoft Access k vytvoření zástupce nebo odkazu na Microsoft Access Report, což je databázový objekt, který se stane užitečným, když potřebujete prezentovat informace v databázi pro kterékoli z následujících použití:

- Zobrazení souhrnu dat.
- Archivujte snímky dat.
- Zobrazení podrobností o jednotlivých záznamech.
- Vytvářejte štítky.

## Části zprávy o přístupu
Návrh sestavy aplikace Access je rozdělen do různých částí, které lze zobrazit v zobrazení Návrh. Následující tabulka vysvětluje, jak jednotlivé části fungují a jak vám mohou pomoci při vytváření sestav.
| Sekce | Jak se sekce zobrazí při tisku | Kde lze sekci použít |
---------|----|------|
| Záhlaví zprávy | Na začátku zprávy. | Záhlaví sestavy použijte pro informace, které se normálně mohou objevit na titulní stránce, jako je logo, název nebo datum. Když do záhlaví sestavy umístíte vypočítaný ovládací prvek, který používá agregační funkci Součet, vypočítaný součet platí pro celou sestavu. Záhlaví sestavy se vytiskne před záhlavím stránky. |
| Záhlaví stránky | V horní části každé stránky. | Použijte záhlaví stránky k opakování názvu sestavy na každé stránce. |
| Záhlaví skupiny | Na začátku každé nové skupiny záznamů. | Pomocí záhlaví skupiny vytiskněte název skupiny. Například v sestavě, která je seskupena podle produktu, použijte záhlaví skupiny k vytištění názvu produktu. Když do záhlaví skupiny umístíte vypočítaný ovládací prvek, který používá agregační funkci Součet, součet je pro aktuální skupinu. V sestavě můžete mít více sekcí záhlaví skupiny v závislosti na tom, kolik úrovní seskupení jste přidali. Další informace o vytváření záhlaví a zápatí skupin naleznete v části Přidání seskupení, řazení nebo součtů. |
| Detail | Objeví se jednou pro každý řádek ve zdroji záznamů. | Zde umístíte ovládací prvky, které tvoří hlavní část sestavy. |
| Zápatí skupiny | Na konci každé skupiny záznamů. | Použijte zápatí skupiny k tisku souhrnných informací pro skupinu. V sestavě můžete mít více sekcí zápatí skupiny v závislosti na tom, kolik úrovní seskupení jste přidali. |
| Zápatí stránky | Na konci každé stránky. | K tisku čísel stránek nebo informací na stránku použijte zápatí stránky. |
| Zápatí zprávy | Na konci zprávy. Poznámka: V zobrazení Návrh se zápatí sestavy zobrazí pod zápatím stránky. Ve všech ostatních zobrazeních (například zobrazení rozvržení nebo při tisku nebo náhledu sestavy) se však zápatí sestavy zobrazuje nad zápatím stránky, hned za posledním zápatím skupiny nebo řádkem podrobností na poslední stránce. | Pomocí zápatí sestavy můžete vytisknout součty sestavy nebo jiné souhrnné informace pro celou sestavu. |






## Reference ##

- [Úvod do přehledů v Accessu](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
– [Designing Reports in Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

