{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Códec de video de alta eficiencia",
  "description":"Obtenga información sobre el formato de archivo IDX y las API que pueden crear y abrir archivos IDX",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## ¿Qué es un archivo IDX?

Un archivo IDX es un archivo de índice de subtítulos que apunta a la lista de información de metadatos para subtítulos dentro de un archivo .sub (Subtítulos VobSub). Es creado y utilizado por la aplicación de software VobSub que permite a los usuarios extraer subtítulos de DVD y volcarlos en un archivo SUB. Los archivos IDX contienen marcas de tiempo y compensaciones de bytes que se utilizan para apuntar a cada uno de los subtítulos. VobSub siempre crea un archivo IDX junto con el archivo SUB correspondiente.

## Formato de archivo IDX - Más información

Los archivos IDX se generan y guardan como archivos de texto sin formato que se pueden abrir en cualquier editor de texto. Un archivo IDX contiene información que los reproductores multimedia leen para leer parámetros como el color del texto de los subtítulos para mostrar en la pantalla, la posición del texto de los subtítulos en la pantalla.

### Configuración de subtítulos IDX

Un archivo IDX típico almacena esta información de metadatos al comienzo del archivo. La configuración de los subtítulos comienza con **#**. Las marcas de tiempo y las referencias de imágenes se agregan después de todas estas configuraciones de subtítulos y comienzan con **marca de tiempo:**.

## Ejemplo de formato de archivo IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## ¿Cómo usar el archivo IDX?

Si tiene los archivos Sub e IDX para una película, puede reproducir estos subtítulos junto con la película para la que se crearon. Muchas aplicaciones como VLC, GOM Player, PotPlayer o PowerDVD tienen la capacidad de cargar estos archivos SUB e IDX y reproducirlos junto con la película. Las aplicaciones de software también pueden incrustar archivos de subtítulos SUB e IDX en archivos [.mkv](/es/video/mkv/).

## Convertir IDX a SRT

El [SRT](/es/video/srt/) (formato de archivo SubRip) es un archivo de subtítulos simple guardado en el formato de archivo SubRip. Se usa más comúnmente en comparación con el formato de archivo VobSub. Por lo tanto, si desea convertir archivos SUB/IDX a formato de archivo SRT, hay herramientas de terceros disponibles que pueden usarse para lograrlo. El convertidor SUB/IDX a SRT, disponible en SubtitleTools.com, es una de esas herramientas que toma archivos SUB e IDX como entrada y convierte estos subtítulos VobSub en archivos SRT.

## Referencias

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

