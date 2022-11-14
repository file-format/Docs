{
  "date" : "2021-26-08",
  "keywords" :[ "archivo dcr", "formato de archivo dcr", "qué es un archivo dcr", "archivo", "ejemplo de dcr", "extensión de archivo dcr","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Archivo de imagen RAW de cámara digital",
  "description":"Obtenga información sobre el formato de archivo DCR y las API que pueden crear y abrir archivos DCR",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## ¿Qué es un archivo DCR? ##
Un archivo con extensión dcr contiene el contenido de una fotografía digital guardada en el formato Kodak Digital Camera RAW (DCR). El DCR es la abreviatura de **Digital Camera Raw**; contiene la versión sin comprimir y sin pérdidas de los datos de las imágenes capturadas por una cámara digital Kodak. A los fotógrafos profesionales les gusta usar estos archivos porque almacenan imágenes con una calidad superior a los formatos de imágenes comprimidas de baja calidad.

## formato de archivo DCR
El DCR es un formato patentado desarrollado por Eastman Kodak Company; conocido simplemente como Kodak. Un archivo de imagen Digital Camera Raw (DCR) contiene datos mínimamente procesados del sensor de imagen de una cámara digital. Estos archivos aún no se han procesado y, por lo tanto, no están listos para imprimirse o editarse con un editor de gráficos de mapa de bits.
Por lo general, un convertidor sin formato procesa la imagen en un espacio de color interno de amplia gama en el que se puede lograr precisión y refinamiento antes de la conversión a un formato de archivo de trama, como TIFF o JPEG, para su almacenamiento, impresión o manipulación adicional.
### Contenido del archivo
La estructura de los archivos sin formato suele seguir un patrón genérico:
- Un encabezado de archivo corto que contiene un indicador del orden de bytes del archivo.
- Metadatos del sensor de la cámara que se requieren para interpretar los datos de la imagen del sensor, incluidos los atributos del CFA, el tamaño del sensor y su perfil de color.
- Metadatos de imágenes que pueden ser útiles para su inclusión en cualquier entorno o base de datos CMS. Algunos archivos sin procesar contienen una sección de metadatos estandarizados con datos en formato Exif.
- Una miniatura de la imagen.
- Una conversión JPEG de tamaño completo de la imagen, que se utiliza para obtener una vista previa del archivo en el panel LCD de la cámara.
- En el caso de escaneos de películas cinematográficas, ya sea el código de tiempo, el código clave o el número de fotograma en la secuencia de archivo que representa la secuencia de fotogramas en un carrete escaneado.
- Los datos de la imagen del sensor
### Datos de imagen del sensor
El archivo en bruto desempeña un papel en la fotografía digital similar al que desempeña la película fotográfica en la fotografía cinematográfica. Los archivos sin procesar contienen, por lo tanto, los datos de resolución completa tal como se leen de cada uno de los píxeles del sensor de imagen de la cámara. El sensor de la cámara está superpuesto casi constantemente con un CFA (matriz de filtros de color). Se puede utilizar en la conversión de imágenes de alto rango dinámico cuando hay datos en formato sin procesar disponibles; como una alternativa más simple al enfoque HDI de exposición múltiple de capturar tres imágenes separadas.


## Referencias ##

* [Formato de imagen sin procesar: por Wikipedia] (https://en.wikipedia.org/wiki/Raw_image_format)
* [Qué es un archivo DCR](https://expertphotography.com/dcr-file/)

