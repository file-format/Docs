{
  "date" : "2020-03-16",
  "keywords" :[ "Plik STL", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku STL i interfejsy API, które mogą tworzyć i otwierać pliki STL.",
  "title" :"Format Pliku STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik STL?

STL, skrót od stereolitrografii, to wymienny format pliku reprezentujący trójwymiarową geometrię powierzchni. Format pliku znajduje zastosowanie w kilku dziedzinach, takich jak szybkie prototypowanie, drukowanie 3D i produkcja wspomagana komputerowo. Reprezentuje powierzchnię jako serię małych trójkątów, zwanych ściankami, gdzie każda ścianka jest opisana przez prostopadły kierunek i trzy punkty reprezentujące wierzchołki trójkąta. Dane wynikowe są wykorzystywane przez aplikacje do określania przekroju kształtu 3D, który ma zostać zbudowany przez wytwórcę. W formacie pliku STL nie ma dostępnych informacji dotyczących reprezentacji koloru, tekstury lub innych typowych atrybutów modelu [CAD](/pl/cad/).

## Krótka historia ##

Rozwój formatu plików STL sięga 1987 roku. Został opracowany przez 3D Systems do użytku w komercyjnych drukarkach 3D. Poprawiona wersja formatu pliku STL, znana jako STL 2.0, została zaproponowana w 2009 roku wraz z aktualizacjami formatu pliku.

## Specyfikacje formatu plików ##

Plik STL reprezentuje geometrię powierzchni za pomocą faset. Fasety definiują powierzchnię obiektu 3D i są jednoznacznie identyfikowane przez normalną jednostkową, która jest linią prostopadłą do trójkąta o długości 1,0, oraz przez trzy wierzchołki. W sumie dla każdego aspektu przechowywanych jest 12 liczb jako normalnych, a każdy wierzchołek jest określony przez trzy współrzędne. Plik StL nie zawiera żadnych informacji o skali; współrzędne są w dowolnych jednostkach.

Specyfikacje formatu pliku STL można zbadać w dwóch aspektach.

### Orientacja fasetek ###

Orientacja fasetki jest określona przez kierunek normalnej jednostki i kolejność, w jakiej wymienione są wierzchołki. Orientację faset określa się na dwa sposoby:

* Kierunek normalnej jest na zewnątrz
* Wierzchołki są wymienione w kolejności przeciwnej do ruchu wskazówek zegara z zewnątrz, zgodnie z regułą prawej ręki.

### Reguła wierzchołka do wierzchołka ###

Zgodnie z tą zasadą każdy trójkąt ma wspólne dwa wierzchołki z każdym sąsiednim trójkątem. Zatem wierzchołek jednego trójkąta nie może leżeć na boku innego trójkąta.

## Formaty plików ##

STL jest dostępny w ASCII, jak również w reprezentacjach binarnych dla kompaktowego formatu pliku.

### Format STL ASCII ###

Wersja ASCII formatu pliku STL jest zapisana w zwykłym ASCII. Jednak ze względu na duży rozmiar format pliku nie jest wybierany jako preferowany format do użytku. Składnia pliku ASCII STL jest następująca:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Pogrubione słowa oznaczają słowa kluczowe, które zawsze powinny być pisane małymi literami. Symbole pisane kursywą to zmienne, które należy zastąpić wartościami określonymi przez użytkownika. Dane liczbowe w wierszach **normalnej płaszczyzny** i **wierzchołku** to liczby zmiennoprzecinkowe pojedynczej precyzji, na przykład 1,23456E+789. Współrzędna **faset normalna** może mieć wiodący znak minus; współrzędna **wierzchołku** może nie.

### Format binarny STL ###

Format binarny wykorzystuje reprezentację liczbową całkowitą i zmiennoprzecinkową IEEE. Format pliku jest reprezentowany w następujący sposób:

|Pole|Informacje|
---|---|
|Nagłówek|80 znaków|
|Liczba trójkątów|4-bajtowa liczba całkowita little endian bez znaku|
|Dane dla każdego trójkąta|12 32-bitowych liczb zmiennoprzecinkowych|

Bardziej szczegółowy widok formatu pliku przedstawiono poniżej.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Bibliografia ##

* [Format STL](http://www.fabbers.com/tech/STL_Format)
* [STL – z Wikipedii](https://en.wikipedia.org/wiki/STL_(file_format))

