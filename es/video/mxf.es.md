{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Formato de intercambio de materiales",
  "keywords" :[ "MXF", "video matroska", "formato mkv", "cómo reproducir archivos MXF", "SMPTE", "multimedia", "video" ],
  "description":"Obtenga más información sobre el formato de archivo MXF y las API que pueden crear y abrir archivos MXF",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## ¿Qué es un archivo MXF?

Un archivo con extensión .mxf es un formato de contenedor multimedia que contiene medios de audio y video digital junto con información de metadatos sobre el archivo. Sigue el estándar SMPTE (Society of Motion Picture and Television Engineers), que es una asociación global de profesionales de ingeniería, tecnología y ejecutivos que trabajan en la industria de los medios y el entretenimiento. Los archivos MXF se pueden convertir a otros formatos de archivo como [AVI](/es/video/avi/) o [MOV](/es/video/mov/).

## Formato de archivo MXF

Los archivos MXF son, de hecho, archivos binarios que consisten en una secuencia de bytes en un formato definido. Las aplicaciones de decodificación deben cumplir con este formato para comprenderlo y extraer información de él. El formato permite agregar nuevos elementos sin romper la compatibilidad con versiones anteriores utilizando la codificación KLV que se describe a continuación.

* Clave: el identificador del elemento, una etiqueta universal SMPTE (UL)
* Longitud: la longitud de los datos, que es la codificación de longitud variable utilizada para reducir la cantidad de espacio necesario para este elemento
* Valor: el valor real del elemento.

### Especificaciones del formato SMPTE

El formato de archivo MXF ha sido definido por las siguientes especificaciones SMPTE.

* SMPTE ST 377-1:2011. Televisión — Formato de intercambio de material (MXF) — Especificación de formato de archivo
* SMPTE ST 377-2 (trabajo en progreso a partir de enero de 2012). Sintaxis de extensión codificada KLV para MXF.
* SMPTE ST 378:2004 (Archivado en 2010). Televisión — Formato de intercambio de material (MXF) — Patrón operativo 1a (Artículo único, Paquete único)
* SMPTE ST 379-1:2009. Formato de intercambio de material (MXF): contenedor genérico MXF
* SMPTE ST 379-2:2010. Formato de intercambio de material (MXF): contenedor genérico restringido MXF
* SMPTE ST 380:2004. Televisión — Formato de intercambio de materiales (MXF) — Esquema de metadatos descriptivos-1 (estándar, dinámico)
* SMPTE ST 381-1:2005. Televisión — Formato de intercambio de material (MXF) — Asignación de secuencias MPEG en el contenedor genérico MXF (dinámico)
* SMPTE ST 381-2:2011. Formato de intercambio de materiales (MXF): asignación de secuencias MPEG en el contenedor genérico restringido de MXF
* SMPTE ST 382:2007. Formato de intercambio de material (MXF): asignación de secuencias AES3 y transmisión de audio de onda al contenedor genérico MXF
* SMPTE ST 383:2008. Televisión — Formato de intercambio de materiales (MXF) — Asignación de datos DV-DIF al contenedor genérico MXF
* SMPTE ST 384:2005. Televisión — Formato de intercambio de materiales (MXF) — Mapeo de imágenes sin comprimir en el contenedor genérico MXF
* SMPTE ST 385:2004. Televisión — Formato de intercambio de materiales (MXF) — Asignación de metadatos y esencia SDTI-CP en el contenedor genérico MXF
* SMPTE ST 386:2004 (Archivado en 2010). Televisión — Formato de intercambio de materiales (MXF) — Asignación de datos de esencia tipo D-10 al contenedor genérico MXF
* SMPTE ST 387:2004 (Archivado en 2010). Televisión — Formato de intercambio de materiales (MXF) — Asignación de datos de esencia tipo D-11 al contenedor genérico MXF
* SMPTE ST 388:2004 (Archivado en 2010). Televisión — Formato de intercambio de material (MXF) — Mapeo de audio codificado de ley A en el contenedor genérico MXF
* SMPTE ST 389:2005. Televisión — Formato de intercambio de material (MXF) — Elemento del sistema de reproducción inversa de contenedor genérico MXF
* SMPTE ST 390:2011. Televisión — Formato de intercambio de materiales (MXF) — Patrón operativo especializado "Átomo" (Representación simplificada de un solo elemento)
* SMPTE ST 391:2004 (Archivado en 2010). Televisión — Formato de intercambio de materiales (MXF) — Patrón operativo 1b (artículo único, paquetes agrupados)
* SMPTE ST 392:2004. Televisión — Formato de intercambio de material (MXF) — Patrón operativo 2a (elementos de la lista de reproducción, paquete único)
* SMPTE ST 393:2004. Televisión — Formato de intercambio de material (MXF) — Patrón operativo 2b (elementos de la lista de reproducción, paquetes agrupados)
* SMPTE ST 394:2006. Televisión — Formato de intercambio de material (MXF) — Esquema de sistema 1 para el contenedor genérico MXF
* SMPTE ST 405:2006. Televisión — Formato de intercambio de materiales (MXF) — Elementos y elementos de datos individuales para el esquema del sistema de contenedores genéricos MXF 1
* SMPTE ST 407:2006. Televisión — MXF — Patrones operativos 3a y 3b
* SMPTE ST 408:2006. Televisión — MXF — Patrones operativos 1c, 2c y 3c
* SMPTE ST 410: 2008. Formato de intercambio de material - Partición de flujo genérico.
* SMPTE ST 422:2006. Formato de intercambio de material: mapeo de flujos de código JPEG2000 en el contenedor genérico MXF
* SMPTE ST 429.4:2006. Paquete D-Cinema: aplicación MXF JPEG 2000
* SMPTE ST 429.5:2006. Empaquetado de D-Cinema: archivo de pista de texto cronometrado
* SMPTE ST 429.6:2006. Paquete D-Cinema: MXF Track File Essence Encryption
* SMPTE ST 434:2006. Formato de intercambio de material: codificación XML para metadatos e información de estructura de archivos
* SMPTE ST 436:2006. Televisión: asignaciones MXF para líneas VBI y paquetes de datos auxiliares
* SMPTE ST 2019-4:2009. Asignación de unidades de codificación VC-3 en el contenedor genérico MXF
* SMPTE ST 2037:2009. Asignación de VC-1 al contenedor genérico MXF
* SMPTE RP 2008:2008. Formato de intercambio de material: mapeo de flujos AVC en el contenedor genérico MXF
* SMPTE RP 2057:2011. Transporte de metadatos basados en texto en MXF
* SMPTE EG 41:2004. Formato de intercambio de materiales (MXF): directriz de ingeniería. Nota: Este documento ya no figuraba en el sitio web de SMPTE cuando se consultó en enero de 2012.
* SMPTE EG 42:2004. Formato de intercambio de materiales (MXF): metadatos descriptivos de MXF
* SMPTE RDD 3:2008. Especificación de interoperabilidad e-VTR MXF
* SMPTE RDD 9-2009. Especificación de interoperabilidad MXF de productos Sony MPEG Long GOP
* Menú de hoja de cálculo de registro de metadatos SMPTE.

### Metadatos estructurales MXF

Los metadatos estructurales son fundamentales en un archivo MXF, ya que contienen información útil sobre el contenido del archivo. Los metadatos MXF contienen información como la velocidad de fotogramas, el tamaño del fotograma, la fecha de creación del archivo y la fecha de modificación personalizada. Los metadatos estructurales describen la estructura y las capacidades de un archivo MXF que incluye la descripción técnica de los diversos componentes esenciales y la transmisión de cómo se compone la línea de tiempo de salida.

## Referencias

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Informe de progreso](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Biblioteca OpenSource C++ para MXF](http://www.freemxf.org/)

