{
  "date" : "2021-09-08",
  "keywords" :[ "archivo mgx", "formato de archivo mgx", "qué es un archivo mgx", "archivo", "ejemplo mgx", "extensión de archivo mgx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MGX de reproducción de expansión de Age of Empires 2 y las API que pueden crear y abrir archivos MGX",
  "title" :"MGX - Repetición de expansión de Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ¿Qué es un archivo MGX?

Un archivo con la extensión .mgx es un archivo grabado para el juego Age of Empires II: The Conquerors que se puede reproducir dentro del programa Age of Empires II. Contiene grabación completa de la campaña jugada por el usuario. Se puede cargar y reproducir dentro del programa Age of Empires II. Una vez reproducido, el juego muestra todos los eventos y escenarios que el usuario planeó para la campaña y jugó.

## Formato de archivo MGX - Más información

El formato de archivo interno del archivo MGX se elaboró y está disponible como información parcialmente validada en [Age of Empires 2: The Conquerors — Especificación de formato de archivo de guardado](https://github.com/stefan-kolb/aoc-mgx- formato). Las especificaciones describen los detalles en las siguientes secciones.

### Definiciones de estructura

Se cree que las definiciones de estructura del formato de archivo GPX se basan en las [declaraciones de BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) que proporcionan una forma de leer y escribir datos binarios estructurados. Esto le permite al programador especificar el formato de los datos binarios que luego BinData lee y escribe.

### Mensajería MGX

La mensajería MGX se basa en dos tipos de mensajes.

* GAMESTART: especifica los comandos de inicio del juego y no está validado hasta la fecha
* CHAT: describe los mensajes de chat del juego. Tanto los jugadores como el propio juego (Gaia) pueden emitir mensajes dentro del juego.

### ACCIONES DE JUEGO

Hay varias [Acciones de JUEGO](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) que se han recuperado y cuyos detalles están disponibles.

## Referencias

* [Age of Empires 2: The Conquerors — Especificación de formato de archivo de guardado](https://github.com/stefan-kolb/aoc-mgx-format)

