{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Video de audio comprimido", "Archivo", "Extensión", "Formato de archivo", "Contenedor multimedia", "XVid", "DivX", "Códecs", "Formato de archivo de intercambio de recursos", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo AVI: un archivo intercalado de audio y video",
  "description":"Obtenga información sobre el formato de archivo AVI y las API que pueden crear y abrir archivos AVI",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo AVI? ##

El formato de archivo **AVI** es un formato de archivo contenedor multimedia de audio y video que introdujo Microsoft. Contiene los datos de audio y video creados y comprimidos usando varios códecs (Codificadores/Decodificadores) como **XVid** y **DivX**. Dado que se pueden usar diferentes códecs para codificar los contenidos AVI, las aplicaciones de recuperación, es decir, los reproductores AVI, deberían poder abrirlos solo si tienen instalados los códecs necesarios con los que se crearon los contenidos AVI. El formato es compatible de forma predeterminada en todas las plataformas de **Microsoft Windows**, así como en casi todas las demás plataformas principales. Varias aplicaciones y API brindan la capacidad de crear/guardar, leer y convertir AVI a otros formatos populares como MP4, MOV, WMV, etc.

## Formato de archivo AVI ##

Un archivo que tiene una extensión .avi es un archivo AVI. Es un subformato del formato de archivo de intercambio de recursos (RIFF). RIFF organiza los datos en bloques, o "fragmentos", que se identifican con una etiqueta FourCC. Un archivo AVI es simplemente un "fragmento" en un archivo con formato RIFF.

En el primer subfragmento, el encabezado del archivo se identifica con la etiqueta "hdrl"; su contenido incluye el ancho, la altura y la velocidad de fotogramas del video. En el segundo subfragmento, la etiqueta de movimiento representa la velocidad de fotogramas del video. El video AVI se compone de los datos de audio/visuales reales en este fragmento. También hay un tercer subfragmento opcional con la etiqueta "idx1", que indica la posición dentro del archivo de los fragmentos de datos individuales que pertenecen al archivo.

### Limitaciones ###

* La información de relación de aspecto no se puede codificar en la especificación AVI original, aunque la especificación OpenDML posterior (AVI 2.0) ofrece un método estandarizado
* Aunque los archivos AVI se utilizan ampliamente en la postproducción de películas y televisión, varios enfoques para agregarles un código de tiempo compiten, lo que afecta la usabilidad del formato.
* Un archivo de video codificado en AVI no puede usar una técnica de compresión que requiera datos de fotogramas futuros más allá del fotograma que se está codificando (fotograma B)
* Es problemático usar archivos AVI con tasas de bits variables (VBR) (como audio MP3 a frecuencias de muestreo inferiores a 32 kHz)
* Es probable que un archivo AVI que codifica largometrajes de definición estándar como se usa normalmente genere una sobrecarga de aproximadamente 5 MB por hora, dependiendo de cómo se use el archivo
* Los subtítulos deben estar codificados en la transmisión de video o distribuirse en un archivo separado en caso de que los archivos AVI no puedan acomodar archivos adjuntos como fuentes y subtítulos.

## Breve historia ##

AVI fue presentado por Microsoft en 1992 con el objetivo de proporcionar un formato de archivo de audio y video más sólido y avanzado. El formato rápidamente se hizo popular con el uso de Internet, lo que permite a las personas compartir archivos de video directa e indirectamente a través del almacenamiento de medios basado en la nube.

## Referencias ##

* [AVI - Por Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

