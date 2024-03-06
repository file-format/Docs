{
  "date": "2019-10-11",
  "keywords": [
"geojson failu",
"kas ir geojson fails",
"failu",
"ģeojson piemērs",
"geojson faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON — uz JSON balstīts ģeogrāfiskais faila formāts",
  "description": "Uzziniet par GeoJSON faila formātu un API, kas var izveidot un atvērt GeoJSON failus.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-lvn"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GeoJSON fails?

GeoJSON ir uz JSON balstīts formāts, kas paredzēts ģeogrāfisko objektu attēlošanai ar to netelpiskajiem atribūtiem. Šis formāts definē dažādus JSON (JavaScript Object Notation) objektus un to savienošanas veidu. JSON formāts ir kolektīva informācija par ģeogrāfiskajiem objektiem, to telpiskajiem apjomiem un īpašībām. Šī faila objekts var norādīt uz ģeometriju (punktu, līniju virkni, daudzstūri), objektu vai pazīmju kopumu. Objekti atspoguļo adreses un vietas kā punktu ielas, galvenos ceļus un robežas kā līniju virknes un valstis, provinces un zemes reģionus kā daudzstūrus. Izmantojot GeoJSON, dažādas mobilās maršrutēšanas un navigācijas lietojumprogrammas var norādīt savu pakalpojumu pārklājumu. GeoJSON paplašinājums ir TopoJSON, kas ir mazāks un kodē ģeotelpisko topoloģiju.

## Īsa vēsture ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON faila formāts ##

### Koordināta ###

Koordinātas ir jebkuru ģeogrāfisko datu pamatelements. Šī ir viena dimensija (garums, platums), kas apzīmē vienu skaitli (decimālais formāts), un dažreiz ieraksta arī augstuma koordinātas. Arī laiks ir dimensija, taču tā sarežģītība apgrūtina tā ierakstīšanu kā koordinātu. Abu JSON GeoJSON koordinātas ir formatētas kā cipari.

### Pozīcija ###

Sakārtots koordinātu masīvs attēlo [position](https://geojson.org/geojson-spec.html#positions). Šī ir mazākā vienība, kas var norādīt uz zemes punktu.

[Garums, platums, augstums].

Pirms pašreizējās specifikācijas izlaišanas GeoJSON atļāva ierakstīt trīs koordinātas katrā pozīcijā, taču jaunā specifikācija to neatļauj.

### Ģeometrija ###

Ģeometrijas ir vienkāršas formas (punkti, līknes un virsmas) pakalpojumā GeoJSON, kas sastāv no tipa un koordinātu kopas. Punkts ir vienkāršākā ģeometrija, kas attēlo vienu pozīciju

`{ tips: Punkts, koordinātas: [0, 0] }`

### LineStrings ###

Lai attēlotu līniju, tiek izmantotas vismaz divas savienotas vietas.

`{ tips: Līnijas virkne, koordinātas: [[10, 30], [10, 10]] }`

Punktu un līniju virknes ir divas vienkāršākās ģeometrijas kategorijas. Abi ģeometrijas veidi netraucē daudziem ģeometriskiem noteikumiem. Punktu var attēlot jebkurā vietā, un līnijai var būt vairāk nekā viens punkts, pat ja punkti savstarpēji šķērso.

### Daudzstūri ###

GeoJSON ģeometrijas daudzstūros šķiet ievērojami sarežģītākas. Daudzstūriem ir iekšpuses un ārpuses, un tajās var būt caurumi.

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

Salīdzinot ar LineStrings, daudzstūros koordinātu saraksts ir ligzdots vēl vienā līmenī, un tajā var būt izgriezumi, piemēram, virtuļi.

### Koordinātu līmenis ###

GeoJSON formātā koordinātu īpašumam ir četri dziļuma līmeņi.

### Iespējas ###

Ģeometrijas ir GeoJSON centrālā daļa, tāpēc reālās pasaules dati ir kas vairāk par vienkāršām formām ar identitāti un atribūtiem. Funkcijas ieraksta ģeometriju, kā arī to īpašības.

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

Objekta rekvizīti var būt [JSON](http://json.org/) objekta tips, kas satur viena dziļuma atslēgas vērtību kartējumus.

### Iezīmju kolekcija ###

GeoJSON failu augšējā līmenī FeatureCollection ir visizplatītākā lieta, kas izskatās šādi:

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

Daudzas kartēšanas un ĢIS programmatūras pakotnes atbalsta GeoJSON, tostarp GeoDjango, OpenLayers un Geoforge programmatūru. Tas ir saderīgs arī ar PostGIS un Mapnik. Google, Yahoo un Bing karšu API pakalpojumi atbalsta arī GeoJSON.

## Atsauces Nr.

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON — Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)


