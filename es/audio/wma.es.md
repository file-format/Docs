{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "archivo", "extensión", "formato", "formato de archivo de intercambio de audio", "música" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo WMA y las API que pueden crear y abrir archivos WMA",
  "title" :"WMA - Archivo de audio de Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## ¿Qué es un archivo WMA?

Un archivo con la extensión .wma representa un archivo de audio que se guarda en formato de sistemas avanzados (ASF). ASF es un formato propietario de Microsoft que contiene flujos de bits codificados por Windows Media Audio 9. Además del contenido de audio, un archivo WMA también contiene objetos de metadatos como el título, el álbum, el artista y el género de la pista. Los archivos WMA se utilizan principalmente para la transmisión por Internet de forma similar a los archivos [.mp3](/es/audio/mp3/).

## Formato de archivo WMA

Un archivo WMA es un formato de archivo binario y está contenido en el formato de archivo ASF. Especifica la codificación de metadatos sobre el archivo similar a las etiquetas ID3 utilizadas por los archivos MP3. Microsoft ha estado utilizando el códec WMA en su formato de archivo interoperable protegido (PIFF) desde 2008. Sin embargo, no ha sido declarado como códec de audio estandarizado por los estándares de la industria relacionados, como DECE UltraViolet y MPEG-DASH.

### Datos específicos del tipo de WMA

La información específica del tipo para el códec de audio de Windows Media se almacena en el siguiente formato como parte de los datos específicos del tipo del objeto de propiedades de transmisión.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referencias

* [Descripción general de ASF - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

