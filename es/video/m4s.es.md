{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo M4S - ¿Qué es un archivo M4S?",
  "description":"Obtenga información sobre el formato de archivo M4S y las API que pueden crear y abrir archivos M4S",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## ¿Qué es un archivo M4S?

Un archivo M4S es un pequeño segmento de un video que se transmite por Internet mediante la técnica de transmisión **MPEG-DASH**. Contiene un segmento de video en forma de datos binarios. La aplicación receptora (generalmente un navegador web o un reproductor multimedia) reproduce estos segmentos en el orden en que se reciben. El primer segmento M4S se identifica por los datos de inicialización que contiene. En **resumen**, los archivos M4S son pequeños segmentos multimedia individuales de un archivo completo.

## Formato de archivo M4S

Los archivos M4S se basan en el [formato ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Estos pequeños segmentos de un archivo grande se pueden descargar de forma independiente a través de HTTP. Por lo tanto, si tiene un archivo de película [MP4](/es/video/mp4/) de gran tamaño, se puede transmitir utilizando la técnica MPEG-DASH (Transmisión dinámica adaptativa sobre HTTP) segmentándolo como archivos de segmento M4S. Si este archivo de película grande se descarga en un disco como M4S, se descargan varios archivos M4S. Si se concatenan todos estos segmentos .m4s, se produce un archivo reproducible completo. Los reproductores multimedia no pueden reproducir el archivo a menos que el primer segmento de inicialización también esté disponible con el archivo.

## Acerca de la transmisión MPEG-DASH

MPEG-DASH utiliza una técnica de transmisión de tasa de bits adaptativa que hace posible la transmisión de contenido multimedia de alta calidad a través de Internet. Esto se hace dividiendo el contenido en una secuencia de pequeños segmentos que se transmiten a través de HTTP. Los archivos multimedia grandes, como películas, podcasts o transmisiones en vivo de un evento deportivo, se pueden transmitir de esta manera. Estos segmentos están codificados a diferentes velocidades de bits. Los reproductores multimedia compatibles con MPEG-DASH seleccionan automáticamente el segmento con la tasa de bits más alta mediante un algoritmo de adaptación de tasa de bits. Esto evita que los eventos se detengan o vuelvan a almacenar en búfer en la reproducción.

### API de código abierto para archivos M4S

Hay API de código abierto disponibles que se pueden usar para leer y convertir archivos M4S.

* [libdash](https://github.com/bitmovin/libdash) - API .NET para archivos M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Cliente Javascript para archivo M4S
* [Ir a la biblioteca para crear archivos Dash] (https://github.com/zencoder/go-dash)

### API de código abierto para convertir M4S a MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referencias ###

* [Formato de archivo de medios base ISO (ISOBMFF)] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Streaming adaptativo dinámico sobre HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

