{
  "date" : "2019-10-11",
  "keywords" :[ "file geojson", "che cos'è un file geojson", "file", "esempio geojson", "estensione file geojson", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Formato di file geografico basato su JSON",
  "description":"Scopri il formato di file GeoJSON e le API che possono creare e aprire file GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GeoJSON?

GeoJSON è un formato basato su JSON progettato per rappresentare le caratteristiche geografiche con i loro attributi non spaziali. Questo formato definisce diversi oggetti JSON (JavaScript Object Notation) e la loro modalità di unione. Il formato JSON rappresenta un'informazione collettiva sulle caratteristiche geografiche, le loro estensioni spaziali e le proprietà. Un oggetto di questo file può indicare una geometria (Point, LineString, Polygon), una funzione o una raccolta di funzioni. Le caratteristiche riflettono indirizzi e luoghi come strade di punti, strade principali e confini come stringhe di linee e paesi, province e regioni di terra come poligoni. Utilizzando GeoJSON, diverse applicazioni di navigazione e routing mobile possono indicare la copertura dei loro servizi. Un'estensione di GeoJSON è TopoJSON che è di dimensioni inferiori e codifica la topologia geospaziale.

## Breve storia ##

L'Internet Engineering Task Force (IETF), in associazione con gli autori del formato, ha creato un [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) per rilasciare GeoJSON nell'aprile 2015. Sostituendo il 2008 Specifica GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), la nuova specifica standard del formato GeoJSON pubblicata nell'agosto 2016.

## Formato file GeoJSON ##

### Coordinata ###

La coordinata è l'elemento base di qualsiasi dato geografico. Questa è una singola dimensione (longitudine, latitudine) che rappresenta un singolo numero (formato decimale) e talvolta registra anche una coordinata per l'elevazione. Anche il tempo è una dimensione, ma la sua complessità rende difficile registrarlo come coordinata. Le coordinate in entrambi JSON GeoJSON sono formattate come numeri.

### Posizione ###

Una matrice ordinata di coordinate rappresenta la [posizione](http://geojson.org/geojson-spec.html#posizioni). Questa è l'unità più piccola che può indicare un punto sulla terra.

`[Longitudine, latitudine, altitudine]`

Prima del rilascio della specifica attuale, GeoJSON consentiva di registrare tre coordinate per posizione, ma non è consentito dalla nuova specifica.

### Geometria ###

Le geometrie sono forme semplici (punti, curve e superfici) in GeoJSON che consistono in un tipo e una raccolta di coordinate. Il punto è la geometria più semplice che rappresenta una singola posizione

`{ "tipo": "Punto", "coordinate": [0, 0] }`

### LineStrings ###

Almeno due luoghi collegati vengono utilizzati per rappresentare una linea.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Le stringhe di punti e di linee sono le due categorie più semplici di geometria. Entrambi i tipi di geometria non infastidiscono molte regole geometriche. Un punto può essere rappresentato in un luogo ovunque e una linea può avere più di un punto, anche se i punti sono autoincrocianti.

### Poligoni ###

Le geometrie GeoJSON sembrano significativamente più complesse in Polygons. I poligoni hanno aree interne ed esterne e possono possedere buchi in quella interna.

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

Rispetto a LineStrings, nei poligoni, l'elenco delle coordinate è nidificato di un livello in più e può avere ritagli come ciambelle.

### Livello di coordinate ###

Nel formato GeoJSON, per la proprietà coordinate, ci sono quattro livelli di profondità.

### Caratteristiche ###

Le geometrie sono la parte centrale di GeoJSON, quindi i dati del mondo reale sono più di queste semplici forme che hanno identità e attributi. Caratteristiche registra la geometria e le relative proprietà.

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

Le proprietà di una funzione possono essere un tipo di oggetto [JSON](http://json.org/) che contiene mappature di valori chiave a profondità singola.

### FeatureCollection ###

Al livello più alto dei file GeoJSON, FeatureCollection è la cosa più comune che assomiglia a:

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

Molti pacchetti software di mappatura e GIS supportano GeoJSON, inclusi GeoDjango, OpenLayers e Geoforge. È anche compatibile con PostGIS e Mapnik. Anche i servizi API di Google, yahoo e Bing maps supportano GeoJSON.

## Riferimenti ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Di Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

