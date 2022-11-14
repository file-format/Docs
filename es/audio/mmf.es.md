{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "archivo", "extensión", "formato", "audio", "smaf", "extensión mmf", "archivos mmf", "archivo de música móvil", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MMF y las API que pueden crear y abrir archivos MMF",
  "title" :"MMF - Formato de archivo de música móvil",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## ¿Qué es un archivo MMF?

MMF es una extensión de archivo asociada con un archivo SMAF. MMF significa archivo de música móvil, mientras que SMAF significa formato de aplicación móvil de música sintética. Los archivos MMF dentro de un teléfono inteligente contienen tonos de llamada del sistema, sonido y también pueden contener gráficos y visualización de texto. El MMF contiene además tres tipos de parámetros de instrumentos, incluidos FM, PCM y Stream PCM. Estos formatos de archivo son compatibles con la plataforma del sistema Windows. Los archivos MMF se clasifican como archivos de datos. Por lo general, Microsoft Mail admite archivos MMF. El archivo que tiene el sufijo MMF se puede copiar a cualquier dispositivo móvil o plataforma de sistema.

Además, estos archivos tienen un tamaño mucho más pequeño en comparación con los archivos de formato MIDI estándar. Los archivos [WAV](/es/audio/wav/) y [MID](/es/audio/mid/) se pueden convertir a formato MMF que luego se pueden compartir y distribuir como contenido de audio. Estos archivos se pueden recibir por correo electrónico directamente a teléfonos y PC.


## Breve historia del formato de archivo MMF

Yamaha desarrolló herramientas SMAF como archivos de sonido para que los teléfonos inteligentes puedan almacenar una mayor cantidad de tonos de llamada únicos. Yamaha presentó SMAF con la producción de sus chips de sonido MA-1, MA-2, MA-3, MA-5 y MA-7 LSI. Todos estos formatos se volvieron bastante familiares entre los teléfonos móviles en el mercado de Asia oriental a principios de 2000.

A nivel internacional, el formato MMF fue autorizado por Samsung. Con la ayuda del formato MMF, Samsung pudo diseñar una amplia gama de tonos de llamada polifónicos para usar en los teléfonos inteligentes Samsung.

Yamaha quería que el formato fuera aún más popular y, en los archivos SMAF oficiales de Yamaha, publicó más herramientas compatibles con este formato. Con esto, los usuarios ahora pueden reproducir fácilmente archivos MMF en sus computadoras.


## Especificaciones del formato de archivo MMF ##

Los archivos MMF se clasifican en secciones de datos. Se utiliza una estructura prefijada alrededor de 8 bytes para describir cada segmento.
La etiqueta de 4 bytes incluye CNTI, OPDA, MSTR, MTR y ATR. El tamaño de los datos más 8 bytes es el tamaño del fragmento; el tamaño total del archivo se calcula sumando todos los tamaños de los fragmentos. Si un archivo no se ha dañado, el tamaño del archivo sumado debe ser el mismo que el tamaño del encabezado principal.

### Encabezado ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Aquí hay un ejemplo de archivo MMF:

![](../mmf.png)

## Referencias

* [MMF - Por Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

