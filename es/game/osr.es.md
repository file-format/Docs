{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo OSR y las API que pueden crear y abrir archivos OSR",
  "title" :"Archivo OSR - ¡osu! Formato de archivo de reproducción",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ¿Qué es un archivo OSR?

Un archivo OSR es un archivo de reproducción de juego creado por [osu! juego](https://osu.ppy.sh/home). ¡Osu! es un juego de ritmo donde los usuarios hacen coincidir los clics del mouse con la música. La canción reproducida por el usuario, los aciertos y errores, la hora y la fecha de reproducción de la canción y la clasificación general se registran en el archivo OSR. Este archivo OSR se puede compartir con otros para fines de reproducción. El archivo OSR requiere que el archivo de mapa de ritmos esté presente en la carpeta "Canciones".

**Tipo MIME de formato de archivo OSR:** x-osu-replay

## Formato de archivo OSR

Los archivos OSR se guardan como archivos binarios con campos de datos de longitud fija y variable.

|Tipo de datos| Formato|
---|---|
|Byte |Modo de juego de la repetición (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Entero |Versión del juego cuando se creó la repetición (ej. 20131216)|
|Cuerda |osu! mapa de ritmos MD5 hash|
|Cadena| Nombre del jugador|
|Cadena| osu! hash MD5 de reproducción (incluye ciertas propiedades de la reproducción)|
|Corto| Número de 300s|
|Corto| Número de 100s en estándar, 150s en Taiko, 100s en CTB, 100s en mania|
|Corto| Número de 50 en estándar, fruta pequeña en CTB, 50 en manía|
|Corto| Número de Gekis en estándar, Max 300s en mania|
|Corto| Número de Katus en estándar, 200s en manía|
|Corto| Número de fallos|
|Entero| Puntuación total que se muestra en el informe de puntuación|
|Corto| Mejor combinación mostrada en el informe de puntuación|
|Byte| Combo perfecto/completo (1 = sin fallas ni interrupciones del control deslizante ni controles deslizantes terminados antes de tiempo) |
|Entero| Modos usados. Consulte a continuación la lista de valores de modulación.|
|Cadena| Gráfico de barras de vida: pares separados por comas u/v, donde u es el tiempo en milisegundos en la canción y v es un valor de punto flotante de 0 - 1 que representa la cantidad de vida que tienes en el momento dado (0 = la barra de vida es vacío, 1= la barra de vida está llena)|
|Largo| Marca de tiempo (ticks de Windows) |
|Entero| Longitud en bytes de datos de reproducción comprimidos|
|Byte |Array Datos de reproducción comprimidos|
|Largo| ID de puntuación en línea|
|Doble| Información adicional sobre mods. Solo presente si Target Practice está habilitado.|

## Referencias

* [OSU! Juego de ritmo](https://osu.ppy.sh/home)
* [Formato de archivo OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

