{
  "date" : "2019-10-11",
  "keywords" :[ "fișier geojson", "ce este un fișier geojson", "fișier", "exemplu geojson", "extensie fișier geojson", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Format de fișier geografic bazat pe JSON",
  "description":"Aflați despre formatul de fișier GeoJSON și despre API-urile care pot crea și deschide fișiere GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GeoJSON?

GeoJSON este un format bazat pe JSON conceput pentru a reprezenta caracteristicile geografice cu atributele lor non-spațiale. Acest format definește diferite obiecte JSON (JavaScript Object Notation) și modul de îmbinare a acestora. Formatul JSON reprezintă o informație colectivă despre caracteristicile geografice, întinderile lor spațiale și proprietățile. Un obiect al acestui fișier poate indica o geometrie (Point, LineString, Polygon), o caracteristică sau o colecție de caracteristici. Caracteristicile reflectă adresele și locurile ca străzi ale punctelor, drumurile principale și granițele ca șiruri de linii și țările, provinciile și regiunile terestre ca poligoane. Folosind GeoJSON, diferite aplicații mobile de rutare și navigare pot indica acoperirea serviciilor lor. O extensie a GeoJSON este TopoJSON, care are dimensiuni mai mici și codifică topologia geospațială.

## Scurt istoric ##

Internet Engineering Task Force (IETF), în asociere cu autorii formatului, a creat un [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) pentru a lansa GeoJSON în aprilie 2015. Înlocuind 2008 Specificația GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), noua specificație standard a formatului GeoJSON publicată în august 2016.

## Format de fișier GeoJSON ##

### Coordonate ###

Coordonatele este elementul de bază al oricărei date geografice. Aceasta este o singură dimensiune (Longitudine, latitudine) care reprezintă un singur număr (format zecimal) și, uneori, înregistrează și o coordonată pentru altitudine. Timpul este și o dimensiune, dar complexitatea sa face dificilă înregistrarea lui ca coordonate. Coordonatele din ambele JSON GeoJSON sunt formatate ca numere.

### Poziție ###

O matrice ordonată de coordonate reprezintă [poziția](http://geojson.org/geojson-spec.html#positions). Aceasta este cea mai mică unitate care poate indica un punct de pe pământ.

`[Longitudine, latitudine, altitudine]`

Înainte de lansarea specificației curente, GeoJSON a permis să înregistreze trei coordonate pe poziție, dar nu este permis de noua specificație.

### Geometrie ###

Geometriile sunt forme simple (puncte, curbe și suprafețe) în GeoJSON, care constau dintr-un tip și o colecție de coordonate. Punctul este cea mai simplă geometrie care reprezintă o singură poziție

`{ "type": "Punct", "coordonate": [0, 0] }`

### LineStrings ###

Cel puțin două locuri conectate sunt folosite pentru a reprezenta o linie.

`{ "type": "LineString", "coordonate": [[10, 30], [10, 10]] }`

Șirurile de puncte și linii sunt cele mai simple două categorii de geometrie. Ambele tipuri de geometrie nu deranjează multe reguli geometrice. Un punct poate fi reprezentat într-un loc oriunde, iar o linie poate avea mai multe puncte, chiar dacă punctele se auto-încrucișează.

### Poligoane ###

Geometriile GeoJSON par mult mai complexe în Poligoane. Poligoanele au zone interioare și exterioare și pot avea găuri în interior.

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

În comparație cu LineStrings, în poligoane, lista de coordonate este mai imbricată cu un nivel și poate avea decupaje precum gogoși.

### Nivel de coordonate ###

În formatul GeoJSON, pentru proprietatea coordonate, există patru niveluri de adâncime.

### Caracteristici ###

Geometriile sunt partea centrală a GeoJSON, prin urmare, datele din lumea reală sunt mai mult decât aceste forme simple care au identitate și atribute. Caracteristicile înregistrează geometria, precum și proprietățile acestora.

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

Proprietățile unei caracteristici pot fi un tip de obiect [JSON](http://json.org/) care conține mapări cu valori cheie cu o singură adâncime.

### FeatureColelection ###

La nivelul superior al fișierelor GeoJSON, FeatureCollection este cel mai comun lucru care arată astfel:

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

O mulțime de pachete software de cartografiere și GIS acceptă GeoJSON, inclusiv software-ul GeoDjango, OpenLayers și Geoforge. De asemenea, este compatibil cu PostGIS și Mapnik. Serviciile API ale hărților Google, Yahoo și Bing acceptă și GeoJSON.

## Referințe ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - După Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

