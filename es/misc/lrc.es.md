{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo LRC - ¿Qué es un archivo LRC?",
  "description":"Obtenga más información sobre el archivo LRC Lyric y las API que pueden crear y abrir archivos LRC",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## ¿Qué es un archivo LRC?

Un archivo LRC es un archivo de letras basado en texto que contiene las letras de una canción de audio. Cuando la canción de audio se reproduce con un reproductor de música o software de reproductor de audio en una computadora, el archivo LRC se lee en paralelo y se muestra con el tiempo. Los archivos LRC contienen puntos de referencia para mostrar la letra cuando se reproduce la canción. En general, los archivos LRC tienen el mismo nombre que el archivo de audio correspondiente, como audio.mp3 y audio.lrc. Los archivos LRC son similares a los archivos de subtítulos como [SRT](/es/video/srt/).

## Formato de archivo LRC - Más información

Los archivos de formato de letra LRC se guardan como archivos de texto sin formato y se pueden abrir y editar en un archivo de texto. El contenido de un archivo LRC contiene información de color para mostrar el texto de la letra.

## Formatos LRC

Hay múltiples formatos de archivos LRC que se han desarrollado con el tiempo. Estas

### Formato LRC simple

Las etiquetas de tiempo de línea tienen el formato `[mm:ss.xx]` donde mm son minutos, ss son segundos y xx son centésimas de segundo.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Formato simple extendido

Incluye la capacidad de cambiar y especificar el género de las letras usando M: masculino, F: femenino, D: dúo.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Formato LRC mejorado

El formato LRC mejorado es una versión extendida del formato LRC simple. Agrega una etiqueta de tiempo de palabra en el formato`<mm:ss.xx>` al final de la palabra anterior.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referencias

* [Formato de archivo de letras LRC - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

