{
  "date" : "2019-10-11",
  "keywords" :[ "archivo apng", "formato de archivo apng", "qué es un archivo apng", "archivo", "ejemplo apng", "extensión de archivo apng","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo APNG: archivo gráfico de red portátil animado",
  "description":"Obtenga información sobre el formato de archivo APNG y las API que pueden crear y abrir archivos APNG",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo APNG?

Un archivo con la extensión .apng (Gráficos de red portátiles animados) es un formato gráfico de trama y es una extensión no oficial del Gráfico de red portátil ([PNG](/es/image/png/) ). Se compone de varios fotogramas (cada uno de ellos una imagen PNG) que representa una secuencia de animación. Esto proporciona una visualización similar a la de un archivo [GIF](/es/image/gif/). Los archivos APNG admiten imágenes de 24 bits y transparencia de 8 bits. APNG es compatible con versiones anteriores de archivos GIF no animados. Los archivos APNG usan la misma extensión .png y pueden abrirse con aplicaciones como Mozilla Firefox, Chrome con compatibilidad con APNG, aplicaciones de iMessage para iOS 10.

## Breve historia

* Las especificaciones APNG se crearon en 2004 para proporcionar soporte para imágenes PNG animadas
* Los decodificadores APNG se desarrollaron con un tamaño mucho más pequeño y utilizando la parte posterior del decodificador PNG
* Después de continuas deliberaciones, se formuló un nuevo tipo MIME image/apng manteniendo la misma extensión como .png en lugar de .apng
* APNG fue rechazado oficialmente por el grupo PNG el 20 de abril de 2007 debido a su uniformidad con las imágenes PNG y al mismo tiempo tener diferentes especificaciones

## Formato de archivo APNG

Los archivos APNG se almacenan como archivos binarios en el disco y usan las especificaciones extendidas de PNG para imágenes animadas. El primer cuadro de un archivo APNG es un flujo PNG normal que los decodificadores PNG pueden leer para su visualización. El formato de archivo APNG sigue las especificaciones PNG y los datos se almacenan en segmentos llamados fragmentos. Sin embargo, APNG introdujo los siguientes fragmentos nuevos:

`Chunk de control de animación (acTL)`: indica que este archivo es un archivo PNG animado en lugar de un archivo PNG normal. Actúa como un marcador y viene antes del fragmento IDAT. También contiene la cantidad de fotogramas e información sobre los tiempos para repetir las animaciones.

`Porción de control de fotogramas`: se produce al comienzo de cada uno de los metadatos e información como dimensiones, posición, aplicación de transparencia e información de reemplazo por el fotograma anterior o siguiente una vez que finaliza.

`Frame Data Chunk`: almacena el contenido del marco y comienza con un número de secuencia. Este número de secuencia tiene la misma estructura que el fragmento IDAT de la imagen predeterminada.

{{< figure src="../APNG.png" alt="PNG animado - Formato de archivo APNG" >}}

APNG es compatible con versiones anteriores de PNG, ya que las especificaciones del lateral se diseñaron de tal manera que se supone que una aplicación que lee un archivo PNG simplemente ignora los fragmentos que no comprende. Las especificaciones relativas a la profundidad de bits, el tipo de color, la compresión, los filtros, los métodos de entrelazado y la información de la paleta se utilizan de la misma manera que en el formato PNG predeterminado.

## APNG frente a GIF

Con GIF ya implementado y usándose durante un largo período de tiempo, es posible que se pregunte en qué se diferencia APNG de GIF. Lo que sigue es un conjunto de comparación entre APNG y GIF que da una breve idea de ambos formatos de archivo.

||APNG|GIF|
---|---|---|
|Publicado|2004|1987|
|Profundidad de color|24 bits|8 bits|
|Velocidad de fotogramas|Ilimitado|10 fotogramas por segundo|
|Transparencia|Completa y parcial|Completa|
|Compresión|Muy buena|Buena|

## Referencias

* [Formato de archivo APNG](https://en.wikipedia.org/wiki/APNG)
* [Especificaciones oficiales del formato PNG](https://www.w3.org/TR/PNG/)

