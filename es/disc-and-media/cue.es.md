{
  "date" : "2021-06-09",
  "keywords" :[ "señal", "archivo", "extensión", "formato", "qué es un archivo de señal", "música", "formato de archivo de señal", "especificación de formato de archivo de señal", "hoja de señal", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo CUE y las API que pueden crear, convertir y abrir archivos CUE",
  "title" :"CUE - Archivo de hoja de referencia",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## ¿Qué es un archivo CUE?

Un archivo con extensión .cue, también conocido como archivo de hoja de referencia, es un archivo de metadatos que contiene información sobre el diseño de las pistas en un CD o DVD. Estos son compatibles con los reproductores multimedia y las aplicaciones de creación de discos ópticos. El archivo cue hace referencia a los principales datos de audio almacenados en el CD, junto con las especificaciones de la duración de las pistas, los títulos de los discos y los intérpretes. Por lo tanto, si un solo archivo de audio contiene varias pistas, el archivo de referencia se puede usar para dividir el audio en varios archivos o hacer referencia a varias pistas.

## Formato de archivo CUE

Los archivos CUE o de hoja de referencia se almacenan en formato de texto sin formato que es legible por humanos. La información en un archivo cue son comandos con uno o más parámetros. Estos comandos se aplican a todo el archivo o a una pista individual, según el comando en particular y el contexto. La guía del usuario de CDRWIN describe las especificaciones para la sintaxis y la semántica de la hoja de referencia.

## Comandos esenciales de la hoja CUE

|Comando|Descripción|
---|---|
|ARCHIVO| Hace referencia al archivo que contiene los datos y su formato, como [MP3](/es/audio/mp3/), [WAV](/es/audio/wav/), o imagen de disco binario sin formato)|
|PISTA| Define la información de contexto de la pista, como su número y tipo o modo.|
|ÍNDICE| Representa la posición como un índice dentro del ARCHIVO. El formato es mm:ss:ff (minuto-segundo-fotograma).|
|PREGAP y POSTGAP|Esto indica el intervalo previo o posterior de una pista, que no se almacena en ningún archivo de datos. La duración se especifica en el mismo formato de cuadro de minuto y segundo que para ÍNDICE.|

### Ejemplo de hoja CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referencias

* [Archivo .cda - Por Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

