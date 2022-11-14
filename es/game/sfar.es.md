{
  "date" : "2021-10-20",
  "keywords" :[ "archivo sfar", "formato de archivo sfar", "qué es un archivo sfar", "archivo", "ejemplo de sfar", "extensión de archivo DLC de Mass Effect 3", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo SFAR de Mass Effect 3 y las API que pueden crear y abrir archivos SFAR",
  "title" :"SFAR - Archivo DLC de Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## ¿Qué es un archivo SFAR?

Un archivo con la extensión .sfar es un archivo de datos del juego utilizado por Mass Effect 3 para almacenar su DLC (contenido descargable) en un archivo propietario comprimido. Mass Effect 3 es un juego creado por Electronic Arts, una importante empresa de desarrollo de juegos. El contenido DLC almacenado en un archivo SFAR se usa para ampliar el juego con contenido y funciones adicionales.

## Formato de archivo SFAR - Más información

Los archivos SFAR se almacenan/guardan como archivos comprimidos en formato de archivo binario. Estos utilizan algoritmos de compresión LZX y LZMA para comprimir los contenidos. Los archivos SFAR se pueden abrir con el Editor DLC que viene incluido con ME3 Explorer. Además de SFAR, DLC Editor puede extraer otros archivos de juegos como [PCC](/es/game/pcc/).

## Especificaciones del formato de archivo SFAR

Un archivo SFAR se divide en los siguientes cuatro fragmentos principales.

### Encabezado SFAR

El encabezado SFF contiene información sobre los diversos fragmentos que componen el archivo.

### Tabla de archivos SFAR

La tabla de archivos SFAR contiene una lista de entradas de archivos donde cada entrada tiene una longitud de 30 bytes.

### Tabla de tamaño de bloque

Block-Size contiene múltiples entradas, donde cada entrada tiene 2 byes de largo. Este valor especifica el tamaño de bloque correspondiente a una entrada en la tabla de archivos.

### Bloques

Los fragmentos de bloque en un archivo SFAR contienen los datos dentro del archivo SFAR.

## Referencias

* [Formato de archivo DLC SFAR - Investigación](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

