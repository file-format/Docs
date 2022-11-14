{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "archivo", "extensión", "formato", "qué es un archivo cda", "música", "formato de archivo cda", "especificación de formato de archivo cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo CDA y las API que pueden crear, convertir y abrir archivos CDA",
  "title" :"CDA - Archivo de acceso directo de pista de audio de CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## ¿Qué es un archivo CDA?

Un archivo con extensión .cda es un pequeño archivo auxiliar generado por Microsoft Windows para cada pista de audio en un CD de audio. Estos archivos contienen información típica, como tiempos de pista y un acceso directo de Windows que permite a los usuarios acceder a pistas de audio específicas. Los archivos CDA no son música, pero apuntan a un archivo de música que existe en algún lugar del almacenamiento. Podemos decirlo como un atajo de un archivo de audio que se encuentra en un CD.

## Formato de archivo CDA

El formato de archivo CDA se usa para decirle a una computadora qué archivo de audio reproducir en un CD. Entonces, los archivos CDA se vuelven inútiles separados de un CD que representan. Los archivos CDA se consideran comúnmente como recursos RIFF. Solo hay un fragmento que se llama "CDDA" y contiene solo un bloque de datos llamado "FMT" en la versión actual del archivo .cda. Este bloque tiene una longitud de 24 bytes. El identificador creado por Windows es utilizado por la unidad de CD relacionada con Windows 95 y Windows 98 y su reproductor no puede conectarse a FreeDB o CDDB. Para que pueda mostrar el título de la canción y el nombre del artista, debe ingresar manualmente esta información en el archivo cdplayer.ini.

### Organización de un archivo CDA

La siguiente tabla muestra la información sobre compensaciones típicas:
| compensación | longitud | contenido |
---|---|---|
| 0x00 | 4 | los 4 caracteres ASCII "RIFF" |
| 0x04 | 4 | el tamaño del trozo siguiente: siempre 36 (44 - 8), en 4 bytes (orden de Intel) |
| 0x08 | 4 | identificador de fragmento: los 4 caracteres ASCII "CDDA" |
| 0x0C | 4 | los 3 caracteres ASCII "fmt" seguidos de un espacio |
| 0x10 | 4 | longitud del fragmento: siempre 24, en 4 bytes (orden de Intel) |
| 0x14 | 2 | versión del formato CD, en 2 bytes (orden Intel). En mayo de 2006, siempre igual a 1. |
| 0x016 | 2 | número del rango, en 2 bytes (orden Intel). La primera pista tiene el número 1. |
| 0x18 | 4 | identificador calculado por Windows para cdplayer.exe. |
| 0x1c | 4 | compensación de rango, en número de fotogramas (pedido de Intel) |
| 0x20 | 4 | duración de la pista, número total de fotogramas (pedido de Intel) |
| 0x24 | 1 | rango de posición: marcos |
| 0x25 | 1 | posición de rango: segundos |
| 0x26 | 1 | posición del rango: minutos |
| 0x27 | 1 | un byte nulo (valor binario 0) |
| 0x28 | 1 | duración de la pista: fotogramas |
| 0x29 | 1 | duración de la pista: segundos |
| 0x2a | 1 | duración de la pista: minutos |
| 0x2b | 1 | un byte nulo (valor binario 0) |

## Referencias

* [Archivo .cda - Por Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

