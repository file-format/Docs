{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo OSZ y las API que pueden crear y abrir archivos OSZ",
  "title" :"Archivo OSZ - osu! Formato de archivo Beatmap",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ¿Qué es un archivo OSZ?

Un archivo OSZ es un formato de archivo comprimido utilizado por el juego de ritmo osu. para almacenar datos de mapa de ritmos. Los mapas de ritmo son esencialmente niveles para el juego e incluyen información como la canción, el tiempo del ritmo y la ubicación de los objetos golpeados en la pantalla del juego. Los archivos OSZ permiten una fácil distribución de mapas de ritmos y, por lo general, se descargan de Internet y se importan al juego. ¡OSU! también tiene el formato de archivo [OSR](/es/game/osr/) que es un archivo de reproducción del juego y puede ser reproducido por los jugadores.

**Tipo MIME de formato de archivo OSR:** x-osu-replay

## Formato de archivo OSZ

Los detalles del formato de archivo interno de los tipos de archivo OSZ no están disponibles públicamente. Contiene datos comprimidos [ZIP](/es/compression/zip/) que tienen información para reproducir música, mostrar gráficos y mostrar a los jugadores los eventos en los que deben interactuar con el juego.

## ¿Cómo crear un archivo OSZ?

¡OSU! tiene instrucciones detalladas para [crear OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files
) y archivos OSK. Los siguientes pasos se pueden usar para crear un archivo OSZ usando OSU!.

1. Abra un mapa de ritmos a través del editor.
1. En el menú superior, seleccione Archivo > Exportar paquete....
1. El archivo .osz se colocará en la carpeta Exportaciones dentro del archivo osu! carpeta.

## Referencias

* [OSU! Juego de ritmo](https://osu.ppy.sh/home)
* [Formato de archivo OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats/Osz_%28file_format%29https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format %29#tipos de datos)

