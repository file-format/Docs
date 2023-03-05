{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MCR y las API que pueden crear y abrir archivos MCR",
  "title" :"MCR - Formato de archivo de región de Minecraft",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## ¿Qué es un archivo MCR?

El formato de archivo MCR de Minecraft es un formato de datos utilizado por Minecraft para almacenar fragmentos de terreno de un mundo de Minecraft. Se basa en el formato NBT (Etiqueta binaria con nombre), que fue desarrollado por los desarrolladores del popular motor de juegos de código abierto, Minecraft Forge. El tipo de archivo MCR se introdujo desde el principio y luego fue reemplazado por el [formato de archivo MCA](/es/juego/mca/).

## Formato de archivo MCR

El formato de archivo MCR está estructurado como una serie de etiquetas binarias con nombre, cada una de las cuales contiene un tipo específico de datos. La etiqueta de nivel superior es la etiqueta "Nivel", que contiene todos los datos para un solo nivel de juego. Dentro de la etiqueta Level, hay otras etiquetas con nombre que almacenan diferentes tipos de datos, como la etiqueta "Data", que almacena información sobre el mundo del juego, y las etiquetas "Entities" y "TileEntities", que almacenan datos sobre el objetos de juego y entidades de mosaico en el mundo, respectivamente.

## ¿Qué hay dentro del formato de archivo MCR?

En el formato de archivo MCR de Minecraft, una región es un área de bloques de 32x32 del mundo del juego. El formato MCR divide el mundo del juego en regiones para administrar los datos de manera más eficiente y permitir una carga y guardado más rápidos de los niveles del juego. Cada región se almacena en un archivo separado y el formato de archivo MCR utiliza un sistema de coordenadas para identificar la posición de cada región dentro del mundo del juego. Las coordenadas de una región están determinadas por las coordenadas de bloque de la esquina inferior izquierda de la región. Por ejemplo, una región con coordenadas (-1,0) estaría ubicada una región a la izquierda y cero regiones hacia abajo desde el origen del mundo del juego.

## Especificaciones del formato de archivo MCR

Las especificaciones del formato de archivo MCR están disponibles públicamente. Las especificaciones para el formato NBT, en las que se basa el formato MCR, están disponibles en el sitio web de Minecraft Forge. Además, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) también tiene información detallada sobre el formato de archivo MCR, incluida su estructura y los diversos tipos de datos que admite.

### Datos comprimidos en archivos MCR

El formato de archivo MCR de Minecraft admite la compresión. El formato de archivo MCR se basa en el [formato NBT](https://minecraft.fandom.com/wiki/NBT_format) que permite que los datos se almacenen en forma comprimida. Esto ayuda a reducir el tamaño de los archivos MCR y hacerlos más eficientes para transferir y almacenar. Esta es una característica importante del formato de archivo MCR, ya que permite a los jugadores compartir grandes datos de terreno de Minecraft World con otros.

## Referencias

* [Editor mundial para Minecraft](https://www.mcedit.net/)
* [Acerca de Minecraft](https://www.minecraft.net/en-us)
* [Formato de archivo de región](https://minecraft.fandom.com/wiki/Region_file_format)
* [Formato NBT](https://minecraft.fandom.com/wiki/NBT_format)

