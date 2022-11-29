{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir Report Template File",
  "description":"Läs mer om RML-filer och API:er som kan skapa och öppna RML-filer.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Vad är en RML fil?

En RML-fil är en rapportmallsfil med rapporteringsmotorn [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Mallfilen används för att generera rapporter med datakällan kopplad till Elixir FileSystem. Data läses och fylls i i RML-mallfilen och kan exporteras till ett antal olika filformat såsom [PDF](/sv/pdf/), [RTF](/sv/ordbehandling/rtf/) och kalkylblad [XLS] (/sv/kalkylblad/xls/). Elixir Repertoire-rapporteringsmotor kan kopplas till en mängd olika JDBC-datakällor.

## RML filformat

De interna filstrukturdetaljerna för RML-filformat är inte tillgängliga offentligt. Filerna genereras och sparas internt av Elixir Repertoire-applikationen för att generera rapporter med data som fylls i från de anslutna datakällorna. RML-mallfilen innehåller den övergripande layouten och platshållarinformationen för den slutliga rapporten som ska genereras från data.

## Hur man RML-mallfil?

För att generera RML-mall i Elixir Repertoire kan följande steg följas.

1. Anslut en JDBC-datakälla till filsystemet.
1. Starta guiden Rapportmall
1. Använd programvaran för att hitta datakällans .ds-fil
1. Välj tabellrapport som val av export
1. Välj de fält som ska inkluderas i rapportmallen
1. När du slutligen klickar på knappen Slutför läggs First report.rml till i arkivet och öppnas för att visa fliken Layout.

## Referenser

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)

