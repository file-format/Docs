{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo OSU y las API que pueden crear y abrir archivos OSU",
  "title" :"Archivo OSU - Osu! Formato de archivo de script",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## ¿Qué es un archivo OSU?

¡Un archivo OSU es un guión de juego escrito para osu! juego de ritmo Contiene información sobre un mapa de ritmos utilizado en el juego, como el nivel de dificultad, la canción que se reproducirá y los tiempos de los objetos golpeados con los que el jugador debe sincronizarse con la música. Permite a los jugadores de juegos de ritmo desarrollar desafíos personalizados y compartirlos con la comunidad del juego.

**Tipo MIME de formato de archivo OSR:** x-osu-beatmap

## Formato de archivo OSU

Los archivos OSU se guardan como archivos de texto sin formato en el disco y su estructura está muy claramente definida en el [formato de archivo OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) por osu!.

### Secciones en el archivo OSU

Un archivo OSU típico tiene las siguientes secciones.

|Sección |Descripción |Tipo de contenido|
---|---|---|
|[Generalidades]| Información general sobre el beatmap| clave: pares de valores|
|[Editor]| Configuraciones guardadas para el editor de mapas de ritmos | clave: pares de valores|
|[Metadatos] |Información utilizada para identificar el beatmap| pares clave:valor|
|[Dificultad] |Configuración de dificultad| pares clave:valor|
|[Eventos]| Beatmap y storyboard eventos gráficos| Listas separadas por comas|
|[Puntos de tiempo]| Cronometraje y puntos de control| Listas separadas por comas|
|[Colores]| Combo y colores piel| clave : pares de valores|
|[ObjetosGolpeados]| Golpear objetos| Listas separadas por comas|

## Referencias

* [OSU! Juego de ritmo](https://osu.ppy.sh/home)
* [Formato de archivo OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

