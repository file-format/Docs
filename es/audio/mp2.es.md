{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "archivo mp2", "extensión", "formato", "qué es un archivo mp2", "música", "formato de archivo mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MP2 y las API que pueden crear, convertir y abrir archivos MP2",
  "title" :"MP2 - Formato de archivo de audio MPEG Layer 2",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## ¿Qué es un archivo MP2?

Un archivo MP2, también llamado archivo MPA, es un archivo de audio comprimido con la Capa II de MPEG-1 o MPEG-2; un formato de compresión de audio con pérdida definido por ISO/IEC 11172-3 junto con MPEG-1 Audio Layer I y MPEG-1 Audio Layer III ([MP3](/es/audio/mp3/)), para reducir el tamaño del archivo de audio. Considerando que, MP3 es más popular que MP2 debido a su menor tamaño y disponibilidad en Internet. Por lo tanto, MP2 sigue siendo un estándar vital para la transmisión de audio.

## Formato de archivo MP2

MPEG Audio Layer II (MP2) es el algoritmo central de los estándares MP3. La codificación MPEG-1 Audio Layer 2 se obtuvo del códec de audio MUSICAM. Comenzó como el proyecto Digital Audio Broadcast (DAB) en Alemania como parte del programa de investigación EUREKA. El Eureka 147 contenía tres elementos principales: Codificación y multiplexación de transmisión, Modulación COFDM y Codificación de audio MUSICAM (Patrón de enmascaramiento Codificación y multiplexación integrada de subbanda universal). MUSICAM fue una de las pocas codificaciones que pudo lograr una alta calidad de audio a velocidades de bits en el rango de 64 a 192 kbit/s por canal monofónico. El objetivo era proporcionar unidades de bajo retardo, baja complejidad, robustez ante errores, acceso corto y cumplir con los requisitos técnicos de radiodifusión, telecomunicaciones y grabación en medios de almacenamiento digital.

MP2 es un codificador de audio de subbanda, que puede comprimirse en el dominio del tiempo con un banco de filtros de bajo retardo que genera 32 componentes en el dominio de la frecuencia. En comparación, MP3 es un codificador de audio transformado con un banco de filtros híbrido, lo que significa que la compresión se aplica en el dominio de la frecuencia después de una transformación híbrida del dominio del tiempo. El codificador MP2 puede aprovechar las redundancias entre canales utilizando la codificación de intensidad "estéreo conjunta" opcional.

### Especificaciones del formato de archivo MP2

El formato de archivo MP2 se basa en cuadros digitales sucesivos de 1152 intervalos de muestreo con cuatro formatos posibles:

- formato mono
- formato estéreo
- formato estéreo conjunto codificado por intensidad (irrelevancia estéreo)
- formato de doble canal (no correlacionado)
Algunas especificaciones técnicas importantes de MP2 se dan en la siguiente tabla:

|Especificación| Descripción|
---|---|
|**Tasas de muestreo**| 32, 44,1 y 48kHz|
|**Tasas de bits**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 y 384 kbit/s|
|**Frecuencias de muestreo adicionales**|16, 22,05 y 24 kHz|
|**Tasas de bits adicionales**|8, 16, 24, 40 y 144 kbit/s|
|**Soporte multicanal**|Hasta 5 canales de audio de rango completo y un canal LFE (canal de mejora de baja frecuencia)|

## Referencias ##

* [MPEG-1 Audio Layer II - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

