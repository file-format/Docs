{
"fecha": "2023-05-16",
  "keywords": [
"archivo sami",
"¿Qué es un archivo Sami?",
"ejemplo de archivo sami",
"archivo",
"extensión de archivo sami",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo SAMI - Archivo de intercambio de subtítulos y metadatos",
  "description":"Obtenga más información sobre el formato SAMI y las API que pueden crear y abrir archivos SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent": "vídeo"
}
},
"última modificación": "2023-05-16"
}

## ¿Qué es un archivo SAMI?

Un archivo con la extensión ".sami" normalmente se refiere a un archivo de intercambio de subtítulos y metadatos (SAMI). SAMI es un formato de subtítulos que se utiliza para mostrar subtítulos o subtítulos en videos. Fue desarrollado originalmente por Microsoft para su Windows Media Player.

Los archivos SAMI contienen información de tiempo y contenido de texto para subtítulos o subtítulos, lo que permite sincronizarlos con la reproducción de un video. El formato admite opciones de formato básicas, como estilo de fuente, color y posición de los subtítulos en la pantalla.

Los archivos SAMI suelen ser archivos de texto sin formato y se pueden abrir y editar con un editor de texto. El contenido de un archivo SAMI normalmente incluye una sección de encabezado que proporciona información sobre el archivo, seguida de entradas de subtítulos individuales con sus respectivos tiempos y texto.

A continuación se muestra un ejemplo de cómo podría verse un archivo SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Los archivos SAMI se usan comúnmente junto con reproductores de video o reproductores multimedia que admiten la visualización de subtítulos, como Windows Media Player o VLC Media Player. El reproductor lee el archivo SAMI y sincroniza los subtítulos con el contenido del video, lo que permite a los espectadores leer los subtítulos mientras miran el video.

## Etiquetas HTML soportadas

Los archivos SAMI (Subtitles And Metadata Interchange) admiten un conjunto limitado de etiquetas similares a HTML para formatear y diseñar los subtítulos. Estas son algunas de las etiquetas comúnmente utilizadas admitidas por SAMI:

- ``<SAMI> :`` El elemento raíz que encapsula todo el archivo SAMI.
- ``<HEAD> :`` Contiene información de encabezado para el archivo SAMI.
<html>- ``<TITLE> :`` Especifica el título del archivo SAMI. </html>
- ``<BODY> :`` Incluye las entradas de subtítulos y su información de tiempo.
- ``<SYNC> :`` Representa un punto de sincronización para una entrada de subtítulo. Especifica el momento en el que se debe mostrar el subtítulo.
- ``<P> :`` Encierra el contenido de texto real de un subtítulo. Generalmente se utiliza dentro de un<SYNC> bloquear.
<html>- `` <FONT>:`` Define las propiedades de fuente para el texto adjunto. Se pueden utilizar atributos como Color, Cara, Tamaño y Estilo para modificar la apariencia de la fuente.</font>
- ``<BR> :`` Inserta un salto de línea dentro de un subtítulo.
<html>- `` <B>:`` Muestra el texto adjunto en negrita.</b>
<html>- `` <I>:`` Representa el texto adjunto en cursiva.</i>
<html>- `` <U>:`` Hace que el texto adjunto esté subrayado.</u>
- ``<C> :`` Especifica la posición o alineación del texto del subtítulo en la pantalla. Admite atributos como Centro, Medio, Izquierda, Derecha, Arriba, Abajo y sus combinaciones.
- ``<LANG> :`` Especifica el código de idioma para el texto del subtítulo. Ayuda a identificar el idioma de los subtítulos.

Estas son algunas de las etiquetas básicas admitidas por los archivos SAMI. Es importante tener en cuenta que SAMI no admite toda la gama de etiquetas y atributos HTML. Las etiquetas admitidas se centran principalmente en diseñar y posicionar los subtítulos en lugar de proporcionar una estructuración o interactividad extensa del documento.

## Referencias
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

