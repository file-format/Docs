{
  "date": "2019-10-11",
  "keywords": [
"geojson failą",
"kas yra geojson failas",
"failą",
"geojson pavyzdys",
"geojson failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON – JSON pagrįstas geografinio failo formatas",
  "description": "Sužinokite apie GeoJSON failo formatą ir API, kurios gali kurti ir atidaryti GeoJSON failus.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-ltn"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GeoJSON failas?

GeoJSON yra JSON pagrįstas formatas, skirtas geografinėms ypatybėms su jų neerdviniais atributais pavaizduoti. Šis formatas apibrėžia skirtingus JSON (JavaScript Object Notation) objektus ir jų sujungimo būdus. JSON formatas yra kolektyvinė informacija apie geografines ypatybes, jų erdvinius dydžius ir savybes. Šio failo objektas gali nurodyti geometriją (tašką, eilutę, daugiakampį), ypatybę arba funkcijų rinkinį. Funkcijos atspindi adresus ir vietas kaip taško gatves, pagrindinius kelius ir sienas kaip linijų eilutes ir šalis, provincijas ir sausumos regionus kaip daugiakampius. Naudojant GeoJSON, įvairios mobiliosios maršruto parinkimo ir navigacijos programos gali nurodyti savo paslaugų aprėptį. GeoJSON plėtinys yra TopoJSON, kuris yra mažesnio dydžio ir koduoja geoerdvinę topologiją.

## Trumpa istorija ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON failo formatas ##

### Koordinatė ###

Koordinatė yra pagrindinis bet kokių geografinių duomenų elementas. Tai yra vienas matmuo (ilguma, platuma), reiškiantis vieną skaičių (dešimtainis formatas), o kartais taip pat įrašomas aukščio koordinatas. Laikas taip pat yra matmuo, tačiau dėl jo sudėtingumo sunku jį įrašyti kaip koordinates. Abiejų JSON GeoJSON koordinatės suformatuotos kaip skaičiai.

### Pozicija ###

Sutvarkytas koordinačių masyvas reiškia [position](https://geojson.org/geojson-spec.html#positions). Tai mažiausias vienetas, galintis nurodyti tašką žemėje.

[ilguma, platuma, aukštis].

Prieš išleidžiant dabartinę specifikaciją, GeoJSON leido įrašyti tris koordinates vienoje pozicijoje, bet to neleidžia naujoji specifikacija.

### Geometrija ###

Geometrijos yra paprastos GeoJSON formos (taškai, kreivės ir paviršiai), kurias sudaro tipas ir koordinačių rinkinys. Taškas yra paprasčiausia geometrija, vaizduojanti vieną padėtį

`{ tipas: Taškas, koordinatės: [0, 0] }`

### Eilučių eilutės ###

Linijai pavaizduoti naudojamos mažiausiai dvi sujungtos vietos.

`{ tipas: Eilutės eilutė, koordinatės: [[10, 30], [10, 10]] }`

Taško ir linijos eilutės yra dvi paprasčiausios geometrijos kategorijos. Abu geometrijos tipai netrukdo daugeliui geometrinių taisyklių. Taškas gali būti pavaizduotas bet kurioje vietoje, o linija gali turėti daugiau nei vieną tašką, net jei taškai kertasi savaime.

### Daugiakampiai ###

GeoJSON geometrijos daugiakampiuose atrodo daug sudėtingesnės. Daugiakampiai turi vidines ir išorines sritis, o viduje gali būti skylių.

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

Palyginti su LineStrings, daugiakampiuose koordinačių sąrašas yra įdėtas dar vienu lygiu ir gali turėti išpjovas, pavyzdžiui, spurgas.

### Koordinačių lygis ###

GeoJSON formatu koordinatės ypatybei yra keturi gylio lygiai.

### Funkcijos ###

Geometrijos yra pagrindinė GeoJSON dalis, todėl realaus pasaulio duomenys yra daugiau nei paprastos figūros, turinčios tapatybę ir atributus. Funkcijos įrašo geometriją ir jų savybes.

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

Objekto ypatybės gali būti [JSON](http://json.org/) objekto tipas, kuriame yra vieno gylio rakto reikšmių susiejimas.

### Funkcijų kolekcija ###

Aukščiausiame GeoJSON failų lygyje FeatureCollection yra labiausiai paplitęs dalykas, kuris atrodo taip:

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

Daugelis žemėlapių ir GIS programinės įrangos paketų palaiko GeoJSON, įskaitant GeoDjango, OpenLayers ir Geoforge programinę įrangą. Jis taip pat suderinamas su PostGIS ir Mapnik. Google, yahoo ir Bing žemėlapių API paslaugos taip pat palaiko GeoJSON.

## Nuorodos Nr.

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON – pateikė Vikipedija](https://en.wikipedia.org/wiki/GeoJSON)


