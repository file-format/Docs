{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - soubor šablony zprávy elixíru",
  "description":"Další informace o souboru RML a rozhraních API, která mohou vytvářet a otevírat soubory RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Co je soubor RML?

Soubor RML je soubor šablony pro vytváření sestav s nástrojem pro vytváření sestav [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Soubor šablony se používá ke generování zpráv se zdrojem dat připojeným k systému souborů Elixir. Data se čtou a naplňují v souboru šablony RML a lze je exportovat do řady různých formátů souborů, jako je [PDF](/cs/pdf/), [RTF](/cs/word-processing/rtf/) a tabulkový procesor [XLS](/cs/tabulka/xls/). Reportovací engine Elixir Repertoire lze připojit k široké škále zdrojů dat JDBC.

## Formát souboru RML

Podrobnosti o interní struktuře souboru formátu RML nejsou veřejně dostupné. Soubory jsou generovány a ukládány interně aplikací Elixir Repertoire pro generování sestav s daty naplněnými z připojených datových zdrojů. Soubor šablony RML obsahuje informace o celkovém rozvržení a zástupných symbolech konečné zprávy, která má být z dat vygenerována.

## Jak vytvořit soubor šablony RML?

Chcete-li vygenerovat šablonu RML v repertoáru Elixir, můžete postupovat podle následujících kroků.

1. Připojte zdroj dat JDBC k systému souborů.
1. Spusťte Průvodce šablonou sestavy
1. Pomocí softwaru vyhledejte soubor .ds zdroje dat
1. Jako volbu exportu zvolte tabulkový report
1. Vyberte pole, která mají být zahrnuta do šablony zprávy
1. Nakonec kliknutím na tlačítko Dokončit se do úložiště přidá First report.rml a otevře se karta Layout.

## Reference

* [Repertoár elixíru](https://elixirtech.com/repertoire-2/)

