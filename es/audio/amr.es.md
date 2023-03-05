{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "archivo", "extensión", "formato", "qué es un archivo amr", "música", "formato de archivo amr", "archivo amr","convertir archivo amr a mp3", "reproducir archivo amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo AMR y las API que pueden crear, convertir y abrir archivos AMR",
  "title" :"AMR - Archivo de códec adaptable de velocidad múltiple",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## ¿Qué es un archivo AMR?
El archivo con extensión .amr es un formato de datos de audio relevante para el códec de audio **Adaptive Multi-Rate**; consta de un códec de voz de banda estrecha de velocidad múltiple que codifica señales de banda estrecha a una velocidad de bits de 4,75-12,2 kbit/s con voz de calidad interurbana a partir de 7,4 kbit/s; utiliza la adaptación de enlace para seleccionar una de las ocho tasas de bits diferentes basadas.

## Formato de archivo AMR
El formato de archivo AMR utiliza muchas técnicas de codificación, el algoritmo ACELP (Algebraic Code Excited Linear Prediction) es una de las mejores técnicas; diseñado para comprimir audio hablado humano de una manera más eficiente. 3GPP estableció el AMR como el códec de voz o habla estándar en 1999. El formato de archivo AMR también se usa para almacenar el audio hablado usando el códec de audio **Adaptive Multi-Rate** que usan muchos teléfonos inteligentes para almacenar audio grabado. discursos

### Estructura de formato de archivo
El AMR (Adaptive Multi-Rate) es un formato de audio; ampliamente utilizado en varias aplicaciones y dispositivos móviles, generalmente en reproductores/grabadores de audio o en aplicaciones de tipo VoIP. AMR se puede clasificar además como:

1. AMR-NB (banda estrecha)
2. AMR-WB (banda ancha)

Por lo general, AMR se refiere a AMR-NB. El formato de archivo AMR tiene la siguiente estructura:

Cada archivo AMR contiene un encabezado de 6 bytes que reconoce el archivo como audio AMR. Este encabezado siempre se establece en:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Esto suele ser similar en todos los archivos AMR-NB. Si el encabezado sigue un estándar, es probable que el archivo esté dañado y no deba usarse. el archivo AMR consta de un número entero de fotogramas de audio empaquetados. Cada uno de estos fotogramas compone 20 ms de audio. Cada cuadro se puede codificar usando cualquiera de los modos AMR-NB válidos (0-7, 8 SID en modo DTX). Dado que las tramas se pueden codificar a diferentes velocidades de bits, este método típico se denomina velocidad múltiple adaptativa (AMR).
#### Modos AMR
Los siguientes son los diferentes modos AMR y sus correspondientes tasas de bits:

|MODO| TARIFAS DE BITS|
---|---|
|0| AMR 4.75 - Codifica a 4.75kbit/s|
|1 | AMR 5.15 - Codifica a 5.15kbit/s|
|2 | AMR 5.9 - Codifica a 5,9 kbit/s|
|3 | AMR 6.7 - Codifica a 6.7kbit/s|
|4 | AMR 7.4 - Codifica a 7.4kbit/s|
|5 | AMR 7.95 - Codifica a 7.95kbit/s|
|6 | AMR 10.2 - Codifica a 10,2 kbit/s|
|7 | AMR 12.2 - Codifica a 12,2 kbit/s|

El tamaño de trama de los modos AMR en bytes (incluido el byte de encabezado) se proporciona a continuación:

|CMR |MODO |TAMAÑO DE FOTOGRAMA (en bytes)|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |RAM 5,9 |16|
|3 |RAM 6,7 |18|
|4 |RAM 7,4 |20|
|5 |AMR 7,95 |21|

## Referencias ##

* [Códec de audio adaptativo de velocidad múltiple: por Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Formato de carga útil RTP y formato de almacenamiento de archivos para códecs de audio AMR y AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

