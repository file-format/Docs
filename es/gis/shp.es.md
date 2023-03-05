{
  "date" : "2019-10-11",
  "keywords" :[ "archivo shp", "formato de archivo shp", "qué es un archivo shp", "archivo", "ejemplo de shp", "extensión de archivo shp","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - archivo de forma ESRI",
  "description":"Obtenga información sobre el formato de archivo SHP y las API que pueden crear y abrir archivos SHP",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo SHP?

SHP es la extensión de archivo para uno de los principales tipos de archivos utilizados para la representación de ESRI Shapefile. Representa información geoespacial en forma de datos vectoriales para ser utilizada por aplicaciones de Sistemas de Información Geográfica (SIG). El formato se ha desarrollado como especificaciones abiertas para facilitar la interoperabilidad entre ESRI y otros productos de software.

## Representación de datos

Como se mencionó, un formato de archivo de forma describe la información geoespacial de un conjunto de datos como características vectoriales. Estas características vectoriales incluyen:

* puntos
* líneas
* polígonos

Estas características en combinación pueden representar casi cualquier tipo de forma como pozos de agua, límites de países, puntos espaciales, flujo de ríos, lagos, etc. Cada característica vectorial puede tener atributos que realmente definen el propósito de esa característica. Por ejemplo, un archivo de forma que contiene las ciudades de Los Ángeles puede tener el nombre de la ciudad y la temperatura como atributos que brindan una representación significativa de los datos espaciales.

## Archivos asociados

Las aplicaciones de software no pueden utilizar un archivo shp independiente para dar sentido a los datos que contiene. Para dar sentido a la información contenida en dicho archivo, un archivo de forma utiliza los siguientes archivos obligatorios adicionales.

* archivo shx - archivo de índice
* archivo dbf: un archivo dBASE que almacena todos los atributos de las formas en el archivo principal
* archivo prj - almacena información del proyecto del archivo

También puede haber otros archivos opcionales que compartan el mismo nombre que el archivo principal.

## Especificaciones del formato de archivo SHP

Las especificaciones abiertas de shapefile están disponibles en línea en ESRI en forma de [Descripción técnica](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) y elabora la estructura general del archivo en detalle. La información en el archivo .shp principal consta de encabezados y registros. El encabezado del archivo de longitud fija es seguido por registros de longitud variable donde cada registro se compone de un encabezado de registro de longitud fija seguido por contenidos de registros de longitud variable.

### Encabezado principal del archivo SHP

El encabezado del archivo principal comienza desde el principio del archivo y tiene una longitud de 100 bytes. La organización de este encabezado de archivo principal junto con la posición del byte, el valor, el tipo y el orden de los bytes se muestra en la siguiente tabla.


|Bytes|Campo|Valor|Tipo|Orden de bytes
---|---|---|---|---|
|0-3|Código de archivo|9994|Entero|Big Endian
|4-23|Sin usar|0|Entero|Big Endian
|24-27|Longitud de archivo|Longitud de archivo|Entero|Big Endian
|28-31|Versión|1000|Entero|Little Endian
|32-35|Tipo de forma|Tipo de forma|Entero|Little Endian
|36-67|Rectángulo delimitador mínimo|Xmin, Ymin, Xmax e Ymax|doble|Little Endian
|68-83|Cuadro delimitador|Zmin, Zmax|doble|Little Endian
|84-99|Cuadro delimitador|Mmin, Mmax|doble|

Cabe señalar que el valor de la longitud del archivo es la longitud total del archivo en palabras de 16 bits que también incluye las cincuenta palabras de 16 bits que componen el encabezado.

#### Tipos de formas

Los valores del campo de tipos de forma en la tabla anterior son los siguientes:


|Valor|Tipo de forma
---|---|
|0|Forma nula
|1|Punto
|3|Polilínea
|5|Polígono
|8|Multipunto
|11|PuntoZ
|13|PolyLineZ
|15|PolígonoZ
|18|MultiPuntoZ
|21|PuntoM
|23|PolilíneaM
|25|Polígono M
|28|MultipuntoM
|31|Multiparche

### Registros de datos ###

El encabezado del archivo principal es seguido por registros de longitud variable donde cada registro consiste en un encabezado de registro de longitud fija seguido por contenidos de registro de longitud variable.

#### Cabecera de registro ####

El encabezado del registro contiene información sobre el número de registro y la longitud del contenido del registro en una longitud fija de 8 bytes. La organización del encabezado del registro es como se muestra a continuación:


|Bytes|Campo|Valor|Tipo|Orden de bytes
---|---|---|---|---|
|0-3|Número de registro|Número de registro|Entero|Grande
|4-7|Longitud de registro|Longitud de registro|Entero|Grande

#### Contenido del registro ####

El contenido de un registro de shapefile consta de un tipo de forma seguido de los datos geométricos de esa forma. Un tipo de forma de 0 representa una forma nula que no tiene datos geométricos para la forma. La longitud del contenido del registro es un reflejo de las partes de la forma y los vértices. Tomemos un ejemplo del tipo Point Shape para elaborar cómo un registro contiene información sobre dicho tipo de forma.

Un punto representa una cierta ubicación geográfica en el orden X,Y donde cada coordenada está representada por un valor de doble precisión. La siguiente tabla muestra la disposición de un tipo de forma Punto.


|Bytes|Tipo de forma|Valor|Tipo|Número|Orden de bytes
---|---|---|---|---|---|
|0-3|Tipo de forma|1|Entero|1|Pequeño
|4-11|X|X|doble|1|pequeño
|12-19|Y|Y|doble|1|pequeño

Se pueden encontrar ejemplos de otros tipos de formas en el documento de descripción técnica de ESRI.

## Referencias ##

* [Descripción técnica de ESRI Shapefile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) por ESRI

