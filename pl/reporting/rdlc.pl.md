{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - język definicji raportów po stronie klienta",
  "keywords" :["rdlc", "język definicji raportu", "format mkv", "XSD", "język definicji raportu po stronie klienta"],
  "description":"Dowiedz się więcej o formacie pliku RDLC, który jest reprezentacją XML definicji raportu SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Czym jest plik RLC? ##

RDLC to skrót od Report Definition Language Client side. W rzeczywistości jest to rozszerzenie pliku raportu utworzonego przy użyciu technologii raportowania firmy Microsoft. Do tworzenia tych plików używana jest wersja programu SQL Server 2005 programu Report Designer. Kontrolka **ReportViewer** po stronie klienta może bezpośrednio wykonywać raporty RDLC.

## Pliki RDL VS RDLC
|Pliki .rdl |Pliki .rdlc|
---|---|
|Pliki RDL są tworzone przez program Report Designer w wersji SQL Server 2005|Pliki RDLC są tworzone przez program Report Designer w wersji Visual Studio 2005|
|Jest używany w SQL Server Reporting Services|Jest używany w Visual Studio|
|Jest to raport zdalny|To jest raport lokalny|
|Do uruchomienia potrzebna jest instancja usług Reporting Services|Nie jest potrzebna instancja usług Reporting Services|

## Tworzenie plików definicji raportu klienta (.rdlc).
Formant ReportViewer służy do uruchamiania plików definicji raportów klienta (rdlc) przy użyciu wbudowanych możliwości przetwarzania formantu. Raporty klienta uruchamiane w trybie przetwarzania lokalnego można łatwo tworzyć w projekcie aplikacji. Oto metody tworzenia raportu:

- Użyj **Kreatora raportów**, aby utworzyć nową definicję raportu klienta (.rdlc).

— Utwórz nowy plik definicji raportu klienta (rdlc) przy użyciu programu Visual Studio.

- Programowo generuj definicję raportu.


Podgląd raportu można wyświetlić tylko przez uruchomienie go w kontrolce **ReportViewer**. Pamiętaj, że w dowolnym momencie możesz otworzyć i edytować definicję raportu, a następnie zbudować lub wdrożyć aplikację, aby sprawdzić wyniki.

## Bibliografia ##

- [Tworzenie plików definicji raportu klienta (.rdlc)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

