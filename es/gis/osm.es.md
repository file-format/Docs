{
  "date" : "2019-10-11",
  "keywords" :[ "archivo osm", "qué es un archivo osm", "archivo", "ejemplo de osm", "extensión de archivo osm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Formato de archivo OpenStreetMap",
  "description":"Obtenga más información sobre el formato de archivo OSM y las API que pueden crear y abrir archivos OSM",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo OSM?

OpenStreetMap (OSM) es una gran colección de almacenes de información geográfica voluntarios en diferentes tipos de archivos, que utilizan diferentes esquemas de codificación para convertir estos datos en bits y bytes. OSM es un esfuerzo de colaboración hacia la creación de un mapa editable gratuito del mundo. El resultado principal de este esfuerzo de colaboración son los datos geográficos en lugar del mapa en sí. Las restricciones sobre el uso o la disponibilidad de información geográfica en gran parte del mundo desencadenan la necesidad de crear un OSM. Los datos disponibles de OSM están listos para reemplazar Google Maps para las aplicaciones clásicas (Facebook, Craigslist, etc.) y los datos predeterminados para las aplicaciones del receptor GPS.^^ ^^Aunque la calidad de los datos es diversa en todo el mundo, los datos de OpenStreetMap se pueden comparar convenientemente con fuentes de datos.

## Breve historia ##

Inspirado por el éxito de Wikipedia, en 2004, Steve Coast, un empresario británico, creó este proyecto de mapeo mundial basado en la comunidad en el Reino Unido. Inicialmente se centró en cartografiar el Reino Unido. OpenStreetMap Foundation se estableció por primera vez en abril de 2006 para apoyar la evolución, expansión y circulación de geoespacial gratuito para cualquier persona. En diciembre de 2006, Yahoo ayudó a OpenStreetMap con su fotografía aérea para la producción de mapas. Los datos completos de carreteras para los Países Bajos y los datos de carreteras troncales para India y China fueron aportados a OSM en abril de 2007 por Automotive Navigation Data (AND). En diciembre de 2007, la Universidad de Oxford fue la organización más destacada que integró los datos de OpenStreetMap en su sitio web principal. Desde entonces, más de 2 millones de usuarios registrados aportan datos en este proyecto utilizando dispositivos GPS, fotografía aérea y levantamientos manuales. Estos datos aportados por la comunidad están disponibles bajo la Licencia de base de datos abierta. Una organización sin fines de lucro registrada en Inglaterra, OpenStreetMap Foundation, mantuvo el sitio de OSM.

## Formato de archivo OSM ##

Hay muchas formas y formatos de archivo para almacenar datos geográficos, pero el formato de archivo **OSM** está restringido a OpenStreetMap. OSM es un formato estándar especialmente diseñado para ser transportado fácilmente a través de Internet. Un formato ordenado estructurado, codificado en XML constituye un archivo .osm. En OpenStreetMap hay cuatro elementos pivote para almacenar la estructura de datos topológicos:

{{< figure src="../OSM.png" alt="Formato de archivo OSM" >}}


|Nodos|Vías|Relaciones|Etiquetas
---|---|---|---|
|<ul><li> Representa la posición geográfica almacenada como pares de latitud y longitud.</li><li> Se utiliza para representar entidades de mapas sin tamaño, como picos de montañas.</li></ul> |<ul><li> Listas ordenadas de nodos, lo que significa una polilínea o un polígono</li><li> Representa características lineales, como caminos y ríos, y zonas, como áreas de estacionamiento, junglas y parques.</li></ul> |<ul><li> Las listas ordenadas de nodos y vías representan su relación como barreras y giros en las carreteras, las autopistas abarcan diferentes vías existentes y áreas con huecos.</li></ul> |<ul><li> Almacenar metadatos sobre los objetos del mapa.* Siempre adjunto a cualquier nodo, vía o relación</li></ul>


Las etiquetas se utilizan para caracterizar las características físicas del suelo (edificios y carreteras, etc.) en OpenStreetMap. Cada etiqueta relaciona una característica geográfica de la característica representada por ese nodo o relación específica. En este sistema de etiquetado gratuito, para describir una característica, se puede incluir una cantidad ilimitada de atributos en un mapa. Las combinaciones específicas de clave y valor respaldadas por usuarios registrados actúan como estándares informales para las etiquetas de uso frecuente. Sin embargo, se pueden crear nuevas etiquetas cada vez que los nuevos aspectos requieran analizar atributos de las características que no estaban mapeados previamente. La mayoría de las funciones usan solo una pequeña cantidad de etiquetas para la descripción.

OSM utiliza tres tipos de archivos para almacenar sus datos principales.

OSM maneja todos estos archivos con la información sobre sus detalles de formato. Pero estos archivos producen los mismos objetos internos. Para los archivos de datos, la marca visible en los objetos OSM siempre es verdadera, lo que no es el caso para los archivos de historial y cambios.

De uso común, existe una diversidad de formatos de archivos OSM. Los formatos de archivo definen la codificación del contenido en el disco o el cable en bits y bytes. OSM es capaz de leer y escribir el máximo de estos formatos.

**XML**

El formato OSM original está basado en XML. Los datos de retorno de la API de la base de datos principal de OSM están en formato XML.

**PBF**

Los búferes de protocolo se basan en formato binario y uno de los formatos más compactos.

**O5M/O5C**

Formato binario basado en un formato más simple pero relativamente menos utilizado. OSM puede leer pero no puede escribir este formato.

**OPL**

Un formato simple propuesto para usar con herramientas de línea de comandos estándar de UNIX. Cercano a los archivos CSV, permite una entidad OSM en una línea.

**DEPURAR**

Un formato basado en texto destinado a crear para la depuración. El OSM puede escribir este formato pero no puede leer.

**AGUJERO NEGRO**

Un formato ficticio que elimina todos los datos. El OSM puede escribir este formato pero no puede leer.

## Almacenamiento de datos OSM ##

La base de datos **PostgreSQL** principal de OSM mantiene la copia principal de los datos de OSM con la extensión PostGIS. Para cada primitivo de datos, la base de datos principal mantiene una tabla cuyas filas almacenan objetos individuales. Todas las ediciones actualizan esta base de datos y todos los demás formatos se forman utilizando esta base de datos. Se crean numerosos grupos de bases de datos descargables para transferir datos de un lugar a otro. Dos formatos, uno que usa XML y otro que usa el formato binario de búfer de protocolo (PBF) definen estos grupos. Los datos completos se almacenan en un archivo llamado planet.osm

## Compresión en archivos OSM ##

Los formatos basados en texto (XML, OPL y Debug) usan compresión gzip o bzip2 opcionalmente.

## Referencias ##

* [Manual de formatos de archivos OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#Historia)
* [Aprender OSM](https://learnosm.org/en/osm-data/getting-data/)

