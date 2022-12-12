{
  "date" : "2019-10-11",
  "keywords" :[ "plik osm", "co to jest plik osm", "plik", "przykład osm", "rozszerzenie pliku osm", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - format pliku OpenStreetMap",
  "description":"Poznaj format plików OSM i interfejsy API, które mogą tworzyć i otwierać pliki OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik OSM?

OpenStreetMap (OSM) to ogromny zbiór dobrowolnie przechowywanych informacji geograficznych w różnych typach plików, wykorzystujących różne schematy kodowania do konwersji tych danych na bity i bajty. OSM to wspólny wysiłek mający na celu stworzenie bezpłatnej edytowalnej mapy świata. Głównym wynikiem tej współpracy są dane geograficzne, a nie sama mapa. Ograniczenia dotyczące wykorzystania lub dostępności informacji geograficznych w wielu częściach świata powodują potrzebę stworzenia OSM. Dane dostępne z OSM są gotowe do zastąpienia Google Maps dla klasycznych aplikacji (Facebook, Craigslist itp.) oraz danych domyślnych dla aplikacji odbiornika GPS. źródła danych.

## Krótka historia ##

Zainspirowany sukcesem Wikipedii, Steve Coast, brytyjski przedsiębiorca, stworzył w 2004 roku ten społeczny projekt mapowania świata w Wielkiej Brytanii. Początkowo skupiał się na mapowaniu Wielkiej Brytanii. Fundacja OpenStreetMap została założona w kwietniu 2006 r., aby wspierać ewolucję, ekspansję i obieg bezpłatnych danych geoprzestrzennych dla każdego. W grudniu 2006 r. Yahoo pomogło OpenStreetMap w wykonaniu zdjęć lotniczych do produkcji map. Pełne dane drogowe dla Holandii oraz dane o drogach głównych dla Indii i Chin zostały przesłane do OSM w kwietniu 2007 przez Automotive Navigation Data (AND). W grudniu 2007 r. Uniwersytet Oksfordzki był najbardziej znaną organizacją, która zintegrowała dane OpenStreetMap ze swoją główną witryną internetową. Od tego czasu ponad 2 miliony zarejestrowanych użytkowników wnosi dane do tego projektu za pomocą urządzeń GPS, zdjęć lotniczych i ręcznych ankiet. Te dane przekazane przez społeczność są udostępniane na licencji Open Database License. Zarejestrowana w Anglii organizacja non-profit OpenStreetMap Foundation utrzymywała witrynę OSM.

## Format pliku OSM ##

Istnieje wiele sposobów i formatów plików do przechowywania danych geograficznych, ale format plików **OSM** jest ograniczony do OpenStreetMap. OSM to specjalnie zaprojektowany standardowy format przeznaczony do łatwego transportu przez Internet. Uporządkowany format uporządkowany, zakodowany w XML stanowi plik .osm. W OpenStreetMap istnieją cztery elementy przestawne do przechowywania topologicznej struktury danych:

{{< figure src="../OSM.png" alt="Format pliku OSM" >}}


|Węzły|Sposoby|Relacje|Tagi
---|---|---|---|
|<ul><li> Reprezentuje położenie geograficzne zapisane jako pary szerokości i długości geograficznej.</li><li> Służy do reprezentowania obiektów mapy bez rozmiaru, takich jak szczyty górskie.</li></ul> |<ul><li> Posortowane listy węzłów oznaczające polilinię lub wielokąt</li><li> Reprezentuj obiekty liniowe, takie jak drogi i rzeki, oraz strefy, takie jak parkingi, dżungle i parki.</li></ul> |<ul><li> Posortowane listy węzłów i dróg przedstawiają ich relacje, takie jak bariery i zakręty na drogach, autostrady obejmują różne istniejące drogi i obszary z dziurami.</li></ul> |<ul><li> Przechowuj metadane dotyczące obiektów mapy.* Zawsze dołączone do dowolnego węzła, drogi lub relacji</li></ul>


Tagi są używane do charakteryzowania obiektów fizycznych na ziemi (budynki, drogi itp.) w OpenStreetMap. Każdy znacznik odnosi się do geograficznej charakterystyki obiektu reprezentowanego przez ten konkretny węzeł lub relację. W tym darmowym systemie tagowania, aby opisać obiekt, na mapie można umieścić nieograniczoną liczbę atrybutów. Konkretne kombinacje kluczy i wartości zatwierdzone przez zarejestrowanych użytkowników działają jako nieformalne standardy dla często używanych tagów. Jednak nowe znaczniki można tworzyć zawsze wtedy, gdy nowe aspekty wymagają przeanalizowania wcześniej niezmapowanych atrybutów cech. Większość funkcji używa tylko niewielkiej liczby tagów do opisu.

OSM używa trzech rodzajów plików do przechowywania swoich głównych danych.

OSM obsługuje wszystkie te pliki z informacjami o szczegółach ich formatowania. Ale te same obiekty wewnętrzne są tworzone przez te pliki. W przypadku plików danych widoczna flaga obiektów OSM jest zawsze prawdziwa, co nie ma miejsca w przypadku plików historii i plików zmian.

W powszechnym użyciu istnieje różnorodność formatów plików OSM. Formaty plików definiują kodowanie treści na dysku lub przewodzie w bitach i bajtach. OSM jest w stanie odczytywać i zapisywać maksymalnie te formaty.

**XML**

Oryginalny format OSM jest oparty na XML. Dane zwrotne głównego API bazy danych OSM są w formacie XML.

**PBF**

Kodowanie buforów protokołów opiera się na formacie binarnym i jednym z najbardziej kompaktowych formatów.

**O5M/O5C**

Prostszy format oparty na formacie binarnym, ale stosunkowo rzadziej używany. OSM może czytać, ale nie może zapisywać tego formatu.

**OPL**

Prosty format proponowany do użycia ze standardowymi narzędziami wiersza poleceń systemu UNIX. Blisko plików CSV, pozwala na jedną jednostkę OSM w jednej linii.

**ODPLUSKWIĆ**

Format tekstowy przeznaczony do tworzenia na potrzeby debugowania. OSM może zapisać ten format, ale nie może go odczytać.

**CZARNA DZIURA**

Fikcyjny format, który usuwa wszystkie dane. OSM może zapisać ten format, ale nie może go odczytać.

## Przechowywanie danych OSM ##

Główna baza danych OSM **PostgreSQL** przechowuje główną kopię danych OSM z rozszerzeniem PostGIS. Dla każdego prymitywu danych główna baza danych utrzymuje tabelę, której wiersze przechowują poszczególne obiekty. Wszystkie edycje aktualizują tę bazę danych, a wszystkie inne formaty są tworzone przy użyciu tej bazy danych. Liczne pule baz danych do pobrania są tworzone w celu przesyłania danych z jednego miejsca do drugiego. Te pule definiują dwa formaty, jeden wykorzystujący XML i drugi korzystający z formatu binarnego bufora protokołu (PBF). Pełne dane są przechowywane w pliku o nazwie planet.osm

## Kompresja w plikach OSM ##

Formaty tekstowe (XML, OPL i Debug) używają opcjonalnie kompresji gzip lub bzip2.

## Bibliografia ##

* [Podręcznik formatów plików OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Poznaj OSM](https://learnosm.org/en/osm-data/getting-data/)

