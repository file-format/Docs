{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "archivo", "extensión", "formato", "Codificación de audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo AAC y las API que pueden crear y abrir archivos AAC",
  "title" :"AAC - Archivo de codificación de audio avanzado",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## ¿Qué es un archivo AAC?

AAC (Codificación de audio avanzada) se refiere al estándar de codificación de audio digital que representa archivos de audio basados en compresión de audio con pérdida. Se lanzó como sucesor del formato de archivo **[MP3](/es/audio/mp3/)** teniendo en cuenta que el lateral enfrentaba problemas para la implementación de nuevas ideas en el proceso de codificación basado en el desarrollo de métodos para la compresión de datos. AAC logra una mejor calidad de sonido en comparación con MP3 a la misma tasa de bits. Se definió en MPEG-2 Parte 7 (ISO/IEC 13818-7), y en forma actualizada en MPEG-4 Parte 3 (ISO/IEC 14496-3).

El formato AAC fue adoptado como formato multimedia predeterminado por YouTube, iPhone, iPod, iPad, Apple iTunes y varias otras plataformas. Varias aplicaciones y API están disponibles para la conversión del formato de archivo AAC a otros formatos como MP3, WMA, M4A, **[WAV](/es/audio/wav/)** y otros.

### Breve historia del archivo AAC

El formato de archivo AAC es una versión mejorada de MP3 con algunas mejoras. Contribuido por varias empresas, incluido el Instituto Fraunhofer (Fraunhofer IIS, desarrolladores de MP3), Nokia, Dolby, AT&T y Sony, el formato fue declarado como estándar internacional por Moving Picture Experts Group (MPEG) en abril de 1997. Posteriormente, en 1999, el MPEG-2 Parte 7 se actualizó y se incluyó en la familia de estándares MPEG-4. Era conocido como MPEG-4 Parte 3, identificado como ISO/IEC 14496-3: 1999 o MPEG-4 Audio.

## Especificaciones del formato de archivo AAC

Las especificaciones del formato de archivo AAC permiten una mayor flexibilidad para diseñar el códec que el MP3, lo que da como resultado estrategias de codificación más simultáneas y una compresión eficiente. El formato ha sido elegido por varias plataformas de hardware por sus mejoras sobre MP3 en términos de brindar soporte para más opciones incluso a menos tasas de bits. Las especificaciones del formato de archivo AAC están disponibles como [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) y [MPEG-4 Part 3](https://www.iso.org /standard/53943.html) (la descarga no es gratuita). El formato utiliza los siguientes tipos de medios:

* audio/ac
*audio/aacp
* audio/3gpp
* audio/3gpp2
* sonido/mp4
* audio/mp4a-latm
* audio/mpeg4-genérico

## AAC vs MP3 - Mejoras ##

Las principales diferencias entre AAC y MP3 en términos de mejoras son las siguientes:

* AAC admite una gama más amplia de canales (hasta 48) y frecuencias de muestreo (de 8 kHz a 96 kHz)
* AAC tiene mejores frecuencias de codificación por encima de 16 kHz
* AAC tiene límites de variación más amplios en la resolución de frecuencia-tiempo de un banco de filtros que han llevado a una codificación mejorada de transitorios y partes estacionarias de la señal de audio
* Banco de filtros más eficiente y simple: un banco de filtros híbrido ha sido reemplazado por el estándar MDCT (transformada de coseno discreta modificada)
* Admite una mayor eficacia de la compresión mediante el modelado de ruido temporal (TNS), los coeficientes de predicción de tiempo MDCT (predicción a largo plazo), estéreo paramétrico, sustitución de ruido perceptual, replicación de banda espectral (SBR).
* estéreo conjunto más flexible (se pueden usar diferentes métodos en diferentes rangos de frecuencia);

## Referencias ##

* [AAC - Por Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

