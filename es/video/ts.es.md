{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo TS - Archivo de flujo de transporte de video",
  "keywords" :[ "ts", "volar", "extensión", "extensión", ".ts", "formato" ],
  "description":"Obtenga información sobre qué es un archivo TS y las API que pueden crear y abrir archivos TS",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## ¿Qué es un archivo TS?

Un archivo con extensión .ts es una transmisión de video que almacena los datos en DVD. Utiliza el algoritmo de compresión MPEG-2 ([.mpeg](/es/video/mpg/)) para lograr la máxima eficiencia y compatibilidad entre diferentes tipos de medios, como transmisión por Internet y transmisión. El formato de archivo TS se creó para que se pueda reproducir en dispositivos con malas conexiones a Internet, como Smart TV.

## Formato de archivo TS: más información

Los datos en un archivo TS son similares al archivo [MP4](/es/video/mp4/), pero están divididos en pequeños fragmentos. Cada fragmento consta de una pequeña pieza de video, seguida de un poco de audio y una leyenda opcional. Un solo archivo TS consta de muchos fragmentos de este tipo. Además del video, el audio y los subtítulos, cada fragmento también incluye algunos datos adicionales para detectar errores en el fragmento. Debido a esto, los archivos TS son algo más grandes.

### ¿Por qué usar el formato de archivo TS?

Entonces, si los archivos TS tienen un tamaño algo grande, ¿qué ventaja ofrece usarlos en lugar de otros formatos de archivo? Bueno, en la transmisión, los pequeños fragmentos de video y audio se pueden enviar a través de los medios de comunicación (alámbricos o por radio) en tiempo real. El receptor utiliza los datos adicionales en los fragmentos para omitir los fragmentos propensos a errores.

Además, los archivos TS se utilizan porque el sistema de transmisión no necesita todo el flujo para reproducirlo. La transmisión se puede recoger y se puede usar en tiempo real ensamblando audio y video.

## ¿Cómo reproducir archivos TS?

Bueno, los archivos TS se pueden abrir y reproducir en el popular [reproductor multimedia VideoLAN VLC](https://www.videolan.org/vlc/features.html), que está disponible para descargar de forma gratuita.

## Referencias ##

* [Flujo de transporte MPEG - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

