{
  "date" : "2019-10-11",
  "keywords" :["plik geojson", "co to jest plik geojson", "plik", "przykład geojson", "rozszerzenie pliku geojson", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Geograficzny format pliku oparty na JSON",
  "description":"Poznaj format pliku GeoJSON i interfejsy API, które mogą tworzyć i otwierać pliki GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik GeoJSON?

GeoJSON to format oparty na formacie JSON przeznaczony do reprezentowania obiektów geograficznych z ich atrybutami nieprzestrzennymi. Ten format definiuje różne obiekty JSON (JavaScript Object Notation) i sposób ich łączenia. Format JSON reprezentuje zbiorcze informacje o obiektach geograficznych, ich zasięgu przestrzennym i właściwościach. Obiekt tego pliku może wskazywać geometrię (punkt, ciąg linii, wielokąt), cechę lub zbiór cech. Obiekty odzwierciedlają adresy i miejsca jako ulice punktów, główne drogi i granice jako ciągi linii, a kraje, prowincje i regiony lądowe jako wielokąty. Korzystając z GeoJSON, różne mobilne aplikacje do wyznaczania tras i nawigacji mogą wskazywać zasięg swoich usług. Rozszerzeniem GeoJSON jest TopoJSON, który jest mniejszy i koduje topologię geoprzestrzenną.

## Krótka historia ##

Internet Engineering Task Force (IETF) we współpracy z autorami formatu stworzył [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) w celu wydania GeoJSON w kwietniu 2015 r. Zastąpienie 2008 Specyfikacja GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), nowa standardowa specyfikacja formatu GeoJSON opublikowana w sierpniu 2016 r.

## Format pliku GeoJSON ##

### Współrzędna ###

Współrzędne to podstawowy element wszelkich danych geograficznych. Jest to pojedynczy wymiar (długość geograficzna, szerokość geograficzna) reprezentujący pojedynczą liczbę (format dziesiętny), a czasami rejestruje również współrzędne wysokości. Czas też jest wymiarem, ale jego złożoność sprawia, że trudno go zapisać jako współrzędne. Współrzędne w obu JSON GeoJSON są sformatowane jak liczby.

### Pozycja ###

Uporządkowana tablica współrzędnych reprezentuje [pozycję](http://geojson.org/geojson-spec.html#positions). Jest to najmniejsza jednostka, która może wskazać punkt na ziemi.

`[Długość, szerokość geograficzna, wysokość]`

Przed wydaniem obecnej specyfikacji GeoJSON pozwalał na rejestrowanie trzech współrzędnych na pozycję, ale nowa specyfikacja nie pozwala na to.

### Geometria ###

Geometria to proste kształty (punkty, krzywe i powierzchnie) w GeoJSON, które składają się z typu i zbioru współrzędnych. Punkt to najprostsza geometria reprezentująca pojedynczą pozycję

`{ "typ": "Punkt", "współrzędne": [0, 0] }`

### Ciągi linii ###

Co najmniej dwa połączone miejsca są używane do reprezentowania linii.

`{ "typ": "Ciąg linii", "współrzędne": [[10, 30], [10, 10]] }`

Ciągi punktów i linii to dwie najprostsze kategorie geometrii. Oba typy geometrii nie przeszkadzają wielu regułom geometrycznym. Punkt może być reprezentowany w dowolnym miejscu, a linia może mieć więcej niż jeden punkt, nawet jeśli punkty te przecinają się samoczynnie.

### Wielokąty ###

Geometrie GeoJSON wydają się znacznie bardziej złożone w wielokątach. Wielokąty mają obszary wewnętrzne i zewnętrzne i mogą zawierać dziury w środku.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

W porównaniu do LineStrings, w wielokątach lista współrzędnych jest zagnieżdżona o jeden poziom więcej i może mieć wycięcia jak pączki.

### Poziom współrzędnych ###

W formacie GeoJSON właściwość współrzędnych ma cztery poziomy głębokości.

### Cechy ###

Geometria jest centralną częścią GeoJSON, dlatego rzeczywiste dane to coś więcej niż te proste kształty posiadające tożsamość i atrybuty. Operacje rejestrują geometrię oraz ich właściwości.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Właściwości funkcji mogą być obiektem typu [JSON](http://json.org/) zawierającym mapowania wartości klucza o pojedynczej głębokości.

### Kolekcja cech ###

Na najwyższym poziomie plików GeoJSON FeatureCollection to najczęstsza rzecz, która wygląda następująco:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Wiele pakietów oprogramowania do mapowania i GIS obsługuje GeoJSON, w tym oprogramowanie GeoDjango, OpenLayers i Geoforge. Jest również kompatybilny z PostGIS i Mapnikiem. Usługi API map Google, Yahoo i Bing obsługują również GeoJSON.

## Bibliografia ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON – z Wikipedii](https://en.wikipedia.org/wiki/GeoJSON)

