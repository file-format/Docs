{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Zmień format pliku",
  "description":"Dowiedz się o formacie pliku OSC i interfejsach API, które umożliwiają tworzenie i otwieranie plików OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-pl",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Czym jest plik OSC?

Plik OSC to format pliku zmian, który zawiera zmodyfikowane dane mapy ulic dla istniejącej mapy ulic w formacie .osm. Zawiera informacje o zmianach jakie nastąpią w [OSM file](/gis/osm/). Plik OSC może mieć trzy możliwe typy operacji modyfikacji danych OSM, tj. wstaw”, modyfikuj” lub usuń”. Te pliki zmian są powszechnie używane do eksportowania danych z edytora OSM i importowania do innego edytora.

Możesz otwierać pliki OSC za pomocą oprogramowania Merkaartar i osmchange.

## Format pliku OSC

Pliki OSC są zwykle zapisywane w formacie pliku JOSM, w którym zmiany są reprezentowane przez znaczniki. Rozpoczyna się znacznikiem osmChange”, który wskazuje początek pliku. Podznaczniki określają, czy jest to operacja wstawiania, modyfikowania czy usuwania, która ma zostać wykonana na odpowiednim węźle w pliku OSM. Zawartość węzła faktycznie zawiera zawartość znacznika osm.

### Przykład formatu pliku OSC

Poniżej znajduje się przykład operacji modyfikacji na węźle. Każdy element musi mieć identyfikator zestawu zmian i numer wersji.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Bibliografia

* [Format pliku JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


