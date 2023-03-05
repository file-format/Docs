{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "archivo", "extensión", "formato", "formato de archivo de intercambio de audio", "música" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo WAV y las API que pueden crear y abrir archivos WAV",
  "title" :"WAV - Formato de archivo de audio de forma de onda",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## ¿Qué es un archivo WAV?

WAV, conocido por WAVE (formato de archivo de audio de forma de onda), es un subconjunto de la especificación de formato de archivo de intercambio de recursos (RIFF) de Microsoft para almacenar archivos de audio digital. El formato no aplica ninguna compresión al flujo de bits y almacena las grabaciones de audio con diferentes tasas de muestreo y tasas de bits. Ha sido y es uno de los formatos estándar para CD de audio. Los archivos Wave son más grandes en tamaño en comparación con los nuevos formatos de archivo de audio, como [MP3](/es/audio/mp3/), que utiliza compresión con pérdida para reducir el tamaño del archivo manteniendo la misma calidad de audio. Sin embargo, los archivos WAV se pueden comprimir con los códecs Audio Compression Manager (ACM). Hay varias API y aplicaciones disponibles que pueden convertir archivos WAV a otros formatos de archivos de audio populares.

**¿Sabías?**
Puede convertirse en colaborador en FileFormat.com para mantener la comunidad de formato de archivo actualizada con sus hallazgos. Si tiene que compartir algo sobre WAV o formatos de archivos de audio, puede publicar sus hallazgos en la sección [Noticias sobre formatos de archivos de audio](https://news.fileformat.com/t/audio) para que las personas se mantengan actualizadas.

## Formato de archivo WAV ##

El formato de archivo WAVE, que es un subconjunto de la especificación RIFF de Microsoft, comienza con un encabezado de archivo seguido de una secuencia de fragmentos de datos. Un archivo WAVE tiene un solo fragmento "WAVE" que consta de dos subfragmentos:

* un trozo "fmt" - especifica el formato de datos
* un fragmento de "datos": contiene los datos de muestra reales

### Encabezado del archivo WAV ###

El encabezado de un archivo WAV (RIFF) tiene una longitud de 44 bytes y tiene el siguiente formato:


|Posiciones|Valor de muestra|Descripción
---|---|---|
|1 - 4|"RIFF"|Marca el archivo como archivo riff. Los caracteres tienen 1 byte de longitud cada uno.
|5 - 8|Tamaño del archivo (entero)|Tamaño del archivo total: 8 bytes, en bytes (entero de 32 bits). Por lo general, completará esto después de la creación.
|9 -12|"WAVE"|Encabezado de tipo de archivo. Para nuestros propósitos, siempre es igual a "ONDA".
|13-16|"fmt "|Marcador de fragmento de formato. Incluye cero final
|17-20|16|Longitud de los datos de formato como se indica arriba
|21-22|1|Tipo de formato (1 es PCM) - entero de 2 bytes
|23-24|2|Número de canales: entero de 2 bytes
|25-28|44100|Frecuencia de muestreo: entero de 32 bytes. Los valores comunes son 44100 (CD), 48000 (DAT). Frecuencia de muestreo = Número de muestras por segundo, o Hertz.
|29-32|176400|(Frecuencia de muestreo * Bits por muestra * Canales) / 8.
|33-34|4|(BitsPerSample * Canales) / 8.1 - mono de 8 bits2 - estéreo de 8 bits/mono de 16 bits4 - estéreo de 16 bits
|35-36|16|Bits por muestra
|37-40|"datos"|encabezado de fragmento de "datos". Marca el comienzo de la sección de datos.
|41-44|Tamaño del archivo (datos)|Tamaño de la sección de datos.
|Los valores de muestra se dan arriba para una fuente estéreo de 16 bits.

## Referencias ##

* [WAV - Por Wikipedia](https://en.wikipedia.org/wiki/WAV)

