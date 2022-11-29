{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Fil", "Extension", "Filformat", "Filtillägg", "Extensible Object Markup Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Windows Workflow File Format",
  "description":"Läs mer om XOML-filformat och API:er som kan skapa och öppna XOML-filer.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en XOML fil?

XOML är en akronym för Extensible Object Markup Language och är ett serialiseringsformat för Windows Workflow Foundations arbetsflödesobjekt. Baserat på **[XAML](/sv/web/xaml/)**, används det mest för att skapa användargränssnitt i vanligt **[XML](/sv/web/xml/)**. Dessa används för att deklarera arbetsflödet för användargränssnittet och kompileras tillsammans med den separata filen som innehåller implementeringslogik. Den innehåller en trädbaserad struktur som definierar en rotarbetsflödesnod, kapslade underelement och inbäddade kodsegment. När ett nytt arbetsflöde skapas med Visual Studio för .NET, har det ett alternativ för dig att välja om det ska vara i kodformat eller kodseparerat format. Om du väljer den senare kommer IDE att skapa två filer åt dig; en i XOML-format (bestående av arbetsflödeslayout och inställningar), och den andra är i formatet [.CS](/sv/programming/cs/)/[.VB](/sv/programming/vb/) där programmeringskoden finns.

