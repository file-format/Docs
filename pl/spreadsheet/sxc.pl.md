{
  "date" : "2021-02-26",
  "keywords" :["SXC", "plik", "rozszerzenie", "format pliku", "Sun XML Calc", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku SXC i interfejsy API, które mogą tworzyć i otwierać pliki SXC.",
  "title" :"Format Pliku SXC",
  "linktitle" : "SXC",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-02-26"
}

## Czym jest plik SXC? ##

Format pliku SXC (Sun XML Calc) należy do pakietu biurowego o nazwie OpenOffice.org. Ten format zasadniczo zaspokaja potrzeby użytkowników związane z arkuszami kalkulacyjnymi, ponieważ jest to format pliku arkusza kalkulacyjnego oparty na XML. Format SXC obsługuje formuły, funkcje, makra i wykresy wraz z DataPilot, co jest niesamowitą funkcją, ponieważ automatycznie indywidualizuje i zapewnia podsumowania surowych importowanych danych. Pliki utworzone za pomocą tego oprogramowania są zapisywane z rozszerzeniem .sxc.


## Format pliku SXC ##

Pliki z rozszerzeniem .sxc można otwierać za pomocą programu Microsoft Excel, który jest arkuszem kalkulacyjnym z pakietu Microsoft Office. Istnieją inne programy, które mogą otwierać pliki z rozszerzeniem .sxc, np. Libre Office, StarOffice itp.

Typ zawartości dla tego formatu to:

* application/vnd.sun.xml.calc
* application/vnd.sun.xml.calc.template

## Kompatybilność plików ##

Pliki SXC są kompatybilne z Apache Open Office calc, a dane można eksportować do pliku Microsoft Excel i innych formatów.

## Obsługa plików ##

Polecenia ImportMatrix i ExportMatrix mogą odczytywać i zapisywać pliki SXC. Gdy plik źródłowy jest plikiem SXC, a plik docelowy jest również plikiem SXC, powoduje to, że **f** jest traktowane jako plik arkusza kalkulacyjnego Sun XML Calc. Zarówno macierz importu, jak i eksportu obsługują ten format, który jest automatycznie wykrywany, gdy format jest nieokreślony, a nazwa pliku kończy się na .sxc.

W celu otwarcia pliku SXC wymagane jest powiązanie z plikiem odpowiedniego programu. Ilekroć plik z rozszerzeniem .sxc ma zostać otwarty, upewnij się, że jest wolny od błędów i nie jest uszkodzony. Każdy błąd w pliku może być łatwo obsłużony przez użytkownika i w większości przypadków nie wymaga pomocy technicznej.


## Bibliografia ##

* [StarOffice – z Wikipedii](https://en.wikipedia.org/wiki/StarOffice)

