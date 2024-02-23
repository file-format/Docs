{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik EAZ - Co to jest plik EAZ i jak go otworzyć?",
  "description":"Dowiedz się o formacie pliku EAZ i interfejsach API, które umożliwiają tworzenie i otwieranie plików EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-plz"
}
},
  "lastmod" : "2023-12-23"
}

## Czym jest plik EAZ?

Plik EAZ to plik dodatku wykorzystywany przez ArcGIS Explorer, bezpłatną aplikację opracowaną przez ESRI do eksploracji, wizualizacji i udostępniania map. Zawiera skompresowane archiwum plików, które zawiera [XML file](/web/xml/), skompilowany kod i pliki pomocnicze niezbędne dla dodatku. Pliki te służą do rozszerzenia podstawowej funkcjonalności oprogramowania poprzez dodanie nowych przycisków, dokowalnych okien i innych rozszerzeń.

## Format pliku EAZ — więcej informacji

Pliki EAZ są tworzone przy wykorzystaniu zestawu ArcGIS Explorer SDK, zestawu programistycznego przeznaczonego do tworzenia niestandardowych funkcjonalności w ArcGIS Explorer. Pliki te wykorzystują kompresję [ZIP](/compression/zip/), aby efektywnie pakować swoją zawartość. Sercem archiwum jest plik **Addins.xml**, który znajduje się w katalogu głównym i stanowi istotny element opisujący i wyszczególniający różne dostosowania zawarte w pliku EAZ.

Plik Addins.xml zasadniczo pełni rolę planu działania, oferując wgląd w konkretne ulepszenia, modyfikacje i rozszerzenia, które plik EAZ wprowadza do ArcGIS Explorer. Dzięki tej kompleksowej strukturze programiści mogą hermetyzować i bezproblemowo integrować nowe funkcje, przyciski i dokowalne okna, zwiększając ogólną funkcjonalność i wygodę użytkowania aplikacji ArcGIS Explorer.

## Bibliografia

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
