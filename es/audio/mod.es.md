{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "archivo", "extensión", "formato", "qué es el formato de archivo mod", "música", "formato de archivo mod", "mod vs MP3", "especificación de formato de archivo mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MOD y las API que pueden crear, convertir y abrir archivos MOD",
  "title" :"MOD - Archivo de módulo de música",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## ¿Qué es un archivo MOD?
Un archivo con la extensión .mod es un archivo de módulo de música creado con el formato de módulo de música estándar, que se basa en el **formato de módulo de Amiga** desarrollado por Karsten Obarski y lanzado con el software **Ultimate Soundtracker** para Commodore Sistema amigo. Similar a un archivo [MIDI](/es/audio/mid/), consta de patrones de notas y muestras de sonido, que representan diferentes instrumentos que se reproducen según las notas. Los archivos MOD se utilizan especialmente en los videojuegos como música de fondo y en la subcultura del arte informático **demoscene**.

## Formato de archivo MOD

El MOD es un formato de archivo de computadora utilizado, su función básica es representar música, y fue el primer formato de archivo de módulo. Los archivos MOD usan la extensión de archivo .mod, excepto en **Amiga**, que lee el encabezado de un archivo para determinar el tipo de archivo, por lo que no depende de las extensiones de nombre de archivo. Un archivo MOD consta de un conjunto de varios instrumentos en forma de muestras, una serie de patrones que especifican cómo y cuándo se reproducirán las muestras, y una lista de qué patrones reproducir y en qué orden.

### Especificaciones del formato de archivo MOD

Un patrón de archivo MOD en realidad está diseñado en una interfaz de usuario de secuenciador como una tabla con una columna por canal, por lo que esta tabla tiene cuatro columnas (una para cada canal de hardware de Amiga. Cada columna tiene 64 filas).

Una celda de la tabla puede provocar que ocurra una de las siguientes acciones en el canal de su columna cuando se alcanza el tiempo de su fila:

- Iniciar un instrumento tocando una nota nueva en este canal a un volumen dado, posiblemente con un efecto especial aplicado
- Cambiar el volumen o el efecto especial que se aplica a la nota actual
- Cambio de patrón de flujo; saltar a una canción específica o posición de patrón o bucle dentro de un patrón
- Hacer nada; cualquier nota existente que se reproduzca en este canal continuará reproduciéndose

Un instrumento es una sola muestra junto con una especificación opcional de qué parte de la muestra se puede repetir para mantener una nota sólida.

### Momento
El marco de tiempo mínimo era de 0,02 segundos en el archivo MOD original, o un intervalo de "borrado vertical" (VSync), porque el software original usaba la sincronización VSync del monitor funcionando a 50 Hz (para PAL) o 60 Hz (para NTSC) por cronometraje

## Referencias

* [MOD (formato de archivo) - Por Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

