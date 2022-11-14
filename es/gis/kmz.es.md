{
  "date" : "2019-10-11",
  "keywords" :[ "archivo kmz", "qué es un archivo kmz", "archivo", "ejemplo kmz", "extensión de archivo kmz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Formato de archivo comprimido KML",
  "description":"Obtenga información sobre el formato de archivo KMZ y las API que pueden crear y abrir archivos KMZ",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo KMZ?

El archivo KMZ (KML comprimido) es una representación del archivo comprimido [KML](/es/gis/kml/) que contiene información geoespacial visible en aplicaciones GIS como Google Earth. La información sobre las marcas de posición se representa en el archivo como latitud y longitud junto con un nombre personalizado. El archivo KMZ empaquetado único se puede compartir fácilmente con otros usuarios. Los archivos KMZ también pueden incluir datos de modelos 3D para la representación geográfica del modelo. Un archivo KMZ se puede abrir en Google Maps guardando el archivo en una ubicación en línea y luego escribiendo la URL en el cuadro de búsqueda de Google Maps.

## Estructura de archivo ##

El contenido de un archivo MKZ consiste en un archivo KML principal y cero o más archivos asociados. Se puede extraer utilizando una utilidad de descompresión estándar como WinZIP. El formato de archivo KMZ también se comprime en un archivo con una relación de compresión de 10:1. Puede exportar datos de Google Earth como aplicaciones directamente al formato de archivo KMZ. El archivo KML principal se llama **doc.kml**. Al empaquetar un archivo KMZ, se le pueden agregar más de un archivo KML, pero esto no será de beneficio ya que Google Earth busca el primer archivo KML al abrir el archivo KMZ y lo lee. Ignora cualquier otro archivo KML que se encuentre en el archivo. Para asegurarse de que Google Earth lea el archivo KML deseado, se recomienda colocar un solo archivo KML dentro del archivo KMZ.

Las imágenes, modelos, texturas, archivos de sonido y otros recursos a los que se hace referencia en el archivo doc.kml se colocan en otra subcarpeta dentro de la carpeta principal. Esto también puede implicar cierta complejidad dependiendo de la cantidad de archivos de soporte. Los enlaces a estos recursos constituyentes pueden ser referenciados de forma relativa o absoluta.

### Referencias relativas ###

Cuando los recursos se colocan junto al doc.kml principal dentro de una subcarpeta dentro de la carpeta principal, la referencia relativa puede apuntar a estos archivos auxiliares como se muestra en el siguiente ejemplo (solo para el icono).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Referencia absoluta ###

Los recursos también pueden ser referenciados absolutamente. Las referencias absolutas contienen la URL completa del archivo vinculado. Cuando los archivos se publican en un servidor central, la referencia absoluta garantiza que permanezcan sin ambigüedades en comparación con las referencias relativas. No se recomienda hacer referencia absoluta a los archivos locales, ya que estos enlaces se romperán cuando los archivos se muevan a un nuevo sistema. Un ejemplo de referencia absoluta es el siguiente:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Ver también ##

* [GeoJSON](/es/gis/geojson/)

## Referencias ##

* [Archivos de Google Earth y KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

