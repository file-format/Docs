{
  "date" : "2019-10-11",
  "keywords" :[ "archivo gpx", "qué es un archivo gpx", "archivo", "ejemplo gpx", "extensión de archivo gpx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Formato de archivo de intercambio GPX",
  "description":"Obtenga información sobre el formato de archivo GPX y las API que pueden crear y abrir archivos GPX",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GPX?

Los archivos con extensión GPX representan el formato GPS Exchange para el intercambio de datos GPS entre aplicaciones y servicios web en Internet. Es un formato de archivo XML liviano que contiene datos de GPS, es decir, waypoints, rutas y tracks para ser importados y registrados por múltiples programas. El formato de archivo GPX está abierto y es compatible con una variedad de aplicaciones y dispositivos GPS. Los datos GPS de dichos archivos se pueden cargar para mostrarlos en aplicaciones de mapas con fines geoespaciales.

## Formato de archivo GPX ##

Un archivo GPX consta de datos de ubicación de latitud y longitud, valores de elevación y otra información posiblemente descriptiva. Los datos de ubicación se expresan en grados decimales y la elevación se expresa en metros. La hora en un archivo GPX está en hora universal coordinada (UTC) usando el formato ISO 8601. Los beneficios de usar un archivo GPX son los siguientes:

* GPX le permite intercambiar datos con una lista creciente de programas para Windows, MacOS, Linux, Palm y PocketPC.
* GPX se puede transformar en otros formatos de archivo usando una página web simple o un programa de conversión.
* GPX se basa en el estándar XML, por lo que muchos de los nuevos programas que utiliza (Microsoft Excel, por ejemplo) pueden leer archivos GPX.
* GPX facilita que cualquiera en la web desarrolle nuevas funciones que funcionarán instantáneamente con sus programas favoritos.

El [Esquema GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) muestra la representación del formato de archivo GPX como referencia.

### Datos esenciales ###

Los siguientes son datos esenciales que forman parte de un archivo GPX para la representación de datos GPS.

* **Waypoints**: Un waypoint es una coordenada WGS84 (GPS) de un punto y representa una capa de características de tipo OGR wkbPoint
* **Rutas**: Representan una capa de entidades de tipo OGR wkbLineString. Incluye una lista de puntos de seguimiento, que son puntos de ruta que muestran un giro o puntos de etapa que conducen a un destino.
* **Pistas**: Las pistas representan una capa de características de tipo OGR wkbMultiLineString. Está compuesto por al menos un segmento que contiene puntos de ruta en una lista ordenada de puntos que describen una ruta. Consiste en una lista de puntos de seguimiento que representan un seguimiento GPS continuo.

### Archivo de ejemplo GPX ###

El siguiente archivo GPX muestra la organización de los datos GPS en un archivo GPX y puede dar una buena idea sobre el contenido de un archivo GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Referencias ##

* [Formato de archivo GPX] (http://www.topografix.com/gpx.asp)
* [GPX - Por Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

