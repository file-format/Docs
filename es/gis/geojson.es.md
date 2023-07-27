{
  "date" : "2019-10-11",
  "keywords" :[ "archivo geojson", "qué es un archivo geojson", "archivo", "ejemplo de geojson", "extensión de archivo geojson","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Formato de archivo geográfico basado en JSON",
  "description":"Obtenga información sobre el formato de archivo GeoJSON y las API que pueden crear y abrir archivos GeoJSON",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GeoJSON?

GeoJSON es un formato basado en JSON diseñado para representar las características geográficas con sus atributos no espaciales. Este formato define diferentes objetos JSON (Notación de objetos de JavaScript) y su forma de unión. El formato JSON representa una información colectiva sobre las características geográficas, sus extensiones espaciales y sus propiedades. Un objeto de este archivo puede indicar una geometría (punto, cadena lineal, polígono), una característica o una colección de características. Las entidades reflejan direcciones y lugares como calles de puntos, carreteras principales y fronteras como cadenas de líneas y países, provincias y regiones terrestres como polígonos. Usando el GeoJSON, diferentes aplicaciones móviles de enrutamiento y navegación pueden indicar la cobertura de sus servicios. Una extensión de GeoJSON es TopoJSON que es de menor tamaño y codifica la topología geoespacial.

## Breve historia ##

El Grupo de Trabajo de Ingeniería de Internet (IETF), en asociación con los autores del formato, formó un [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) para lanzar GeoJSON en abril de 2015. Reemplazo del 2008 Especificación GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), la nueva especificación estándar del formato GeoJSON publicada en agosto de 2016.

## Formato de archivo GeoJSON ##

### Coordenada ###

La coordenada es el elemento básico de cualquier dato geográfico. Esta es una sola dimensión (longitud, latitud) que representa un solo número (formato decimal) y, a veces, también registra una coordenada para la elevación. El tiempo también es una dimensión, pero su complejidad hace que sea difícil registrarlo como una coordenada. Las coordenadas en ambos JSON GeoJSON tienen formato de números.

### Posición ###

Una matriz ordenada de coordenadas representa la [posición](https://geojson.org/geojson-spec.html#positions). Esta es la unidad más pequeña que puede indicar un punto en la tierra.

`[Longitud, latitud, elevación]`

Antes del lanzamiento de la especificación actual, GeoJSON permitía registrar tres coordenadas por posición, pero la nueva especificación no lo permite.

### Geometría ###

Las geometrías son formas simples (puntos, curvas y superficies) en GeoJSON que consisten en un tipo y una colección de coordenadas. El punto es la geometría más simple que representa una sola posición.

`{ "tipo": "Punto", "coordenadas": [0, 0] }`

### Cadenas de líneas ###

Se utilizan al menos dos lugares conectados para representar una línea.

`{ "tipo": "LineString", "coordenadas": [[10, 30], [10, 10]] }`

Las cadenas de puntos y líneas son las dos categorías más simples de geometría. Ambos tipos de geometría no molestan a muchas reglas geométricas. Un punto se puede representar en un lugar en cualquier lugar, y una línea puede tener más de un punto, incluso si los puntos se cruzan entre sí.

### Polígonos ###

Las geometrías de GeoJSON parecen significativamente más complejas en Polygons. Los polígonos tienen áreas internas y externas y pueden tener agujeros en ese interior.

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

En comparación con LineStrings, en los polígonos, la lista de coordenadas es un nivel más anidado y puede tener recortes como donas.

### Nivel de coordenadas ###

En formato GeoJSON, para la propiedad de coordenadas, hay cuatro niveles de profundidad.

### Características ###

Las geometrías son la parte central de GeoJSON, por lo tanto, los datos del mundo real son más que estas formas simples que tienen identidad y atributos. Las funciones registran la geometría y sus propiedades.

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

Las propiedades de una característica pueden ser un tipo de objeto [JSON](http://json.org/) que contienen asignaciones de valores clave de profundidad única.

### Colección de características ###

En el nivel superior de los archivos GeoJSON, FeatureCollection es lo más común que se ve así:

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

Una gran cantidad de paquetes de software GIS y de mapeo son compatibles con GeoJSON, incluido el software GeoDjango, OpenLayers y Geoforge. También es compatible con PostGIS y Mapnik. Los servicios API de Google, Yahoo y Bing Maps también son compatibles con GeoJSON.

## Referencias ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-segundo-mordisco.html)
* [GeoJSON - Por Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

