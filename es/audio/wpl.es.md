{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "archivo wpl", "extensión", "formato", "qué es un archivo wpl", "música", "formato de archivo wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo WPL y las API que pueden crear, convertir y abrir archivos WPL",
  "title" :"WPL - Archivo de lista de reproducción del Reproductor de Windows Media",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## ¿Qué es un archivo WPL?

Un archivo con extensión .wpl contiene la lista de reproducción de canciones que se ejecutarán en Microsoft Windows Media Player. Estos archivos generalmente los crean los usuarios para sus colecciones de video y audio. El contenido escrito en un archivo WPL es solo rutas de directorio o ubicaciones para los archivos multimedia seleccionados por el creador del archivo .wpl, de modo que la aplicación del reproductor multimedia pueda encontrar y reproducir rápidamente el contenido multimedia desde sus ubicaciones de directorio.

## Formato de archivo WPL

WPL (lista de reproducción de Windows Media Player) es un formato de archivo patentado que se utiliza en las versiones 9 o posteriores de Microsoft Windows Media Player. Es un formato de archivo de computadora que almacena listas de reproducción multimedia. De manera predeterminada, la lista de reproducción se guarda con una extensión .wpl (Lista de reproducción del Reproductor de Windows Media). En su lugar, puede utilizar la extensión [.m3u](/es/audio/m3u/), si desea reproducir sus discos de datos en un dispositivo que no admita esta extensión. Los elementos de un archivo WPL se representan en formato XML.

El elemento de nivel superior "smil" especifica que los elementos del archivo siguen la estructura del lenguaje de integración multimedia sincronizada (SMIL). El archivo se crea y guarda con la extensión .wpl y su tipo MIME es application/vnd.ms-wpl.

### ejemplo WPL

Aquí hay un ejemplo de un archivo wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Referencias ##

* [MPEG-1 Audio Layer II - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

