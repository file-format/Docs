{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "archivo", "extensión", "formato de archivo", "Ubicación GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Formato de archivo de ubicación GPS",
  "description":"Obtenga información sobre el formato de archivo LOC y las API que pueden crear y abrir archivos LOC",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## ¿Qué es un archivo LOC?

Un archivo con extensión .loc es un archivo de ubicación GPS que contiene ubicaciones geoespaciales como waypoints. Un waypoint es un par de valores de latitud y longitud que se refieren a una ubicación utilizada por las aplicaciones del sistema de información geográfica (SIG). Los programas de mapas GPS, como DeLorme Topo, usan archivos LOC para leer y mostrar información contenida en estos archivos LOC como capas seleccionables por los usuarios finales. Además, se utilizan para intercambiar datos GPS entre aplicaciones. Los archivos LOC se pueden abrir usando aplicaciones como [TopoGrafix EasyGPS](https://www.easygps.com/) que muestra el contenido de dichos archivos como capas y datos trazados en el mapa en la geolocalización respectiva.

## Formato de archivo LOC - Más información

Los archivos LOC tienen similitudes con los archivos [GPX](/es/gis/gpx/), pero se guardan en un formato diferente. Estos se guardan como archivos [XML](/es/web/xml/) donde el contenido de los waypoints y la información asociada se encuentran en etiquetas estructuradas. Dado que XML es un lenguaje generalizado para el intercambio de datos entre diferentes aplicaciones, esto facilita el intercambio de datos LOC con otras aplicaciones.

## Formato de archivo LOC - Ejemplo

Lo siguiente es el encabezado y el texto de un waypoint de un archivo LOC. Como puede verse, la información del encabezado contiene la fuente de ubicación de los datos. El punto de referencia contiene información como el "ID" y los datos de contenido asociados con el punto de referencia. Finalmente, el waypoint es una colección de valores de latitud y longitud y el texto asociado con este waypoint en particular.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Referencias

* [TopGraphic EasyGPS](https://www.easygps.com/)

