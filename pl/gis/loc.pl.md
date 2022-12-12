{
  "date" : "2021-07-18",
  "keywords" :["LOC", "plik", "rozszerzenie", "format pliku", "Lokalizacja GPS", "Punkt trasy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Format pliku lokalizacji GPS",
  "description":"Poznaj format pliku LOC i interfejsy API, które mogą tworzyć i otwierać pliki LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Czym jest plik LOC?

Plik z rozszerzeniem .loc to plik lokalizacji GPS, który zawiera lokalizacje geoprzestrzenne jako punkty trasy. Punkt trasy to para wartości szerokości i długości geograficznej, która odnosi się do lokalizacji używanej przez aplikacje systemu informacji geograficznej (GIS). Programy do mapowania GPS, takie jak DeLorme Topo, używają plików LOC do odczytywania i wyświetlania informacji zawartych w tych plikach LOC jako warstwy do wyboru przez użytkowników końcowych. Ponadto służą one do wymiany danych GPS między aplikacjami. Pliki LOC można otwierać za pomocą aplikacji takich jak [TopoGrafix EasyGPS] (https://www.easygps.com/), która wyświetla zawartość takich plików jako warstwy i dane wykreślone na mapie w odpowiedniej geolokalizacji.

## Format pliku LOC — więcej informacji

Pliki LOC są podobne do plików [GPX](/pl/gis/gpx/), ale są zapisywane w innym formacie. Są one zapisywane jako pliki [XML](/pl/web/xml/), w których zawartość punktów trasy i powiązane informacje są zawarte w znacznikach strukturalnych. Ponieważ XML jest uogólnionym językiem wymiany danych między różnymi aplikacjami, ułatwia to wymianę danych LOC z innymi aplikacjami.

## Format pliku LOC — przykład

Poniżej znajduje się nagłówek i tekst jednego punktu z pliku LOC. Jak widać, informacja nagłówka zawiera źródło lokalizacji danych. Punkt trasy zawiera informacje, takie jak „ID” i powiązane dane zawartości powiązane z punktem trasy. Punkt nawigacyjny to zbiór wartości szerokości i długości geograficznej oraz tekstu powiązanego z tym konkretnym punktem nawigacyjnym.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Bibliografia

* [TopGraphic EasyGPS](https://www.easygps.com/)

