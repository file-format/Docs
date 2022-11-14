{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - Archivo NGS SP3",
  "description":"Obtenga información sobre el formato de archivo SP3 y las API que pueden crear y abrir archivos SP3",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## ¿Qué es un archivo SP3?

Un archivo con extensión .sp3 es un formato orbital del National Geodetic Survey (NGS) para almacenar información orbital. Esta es una extensión de los formatos SP1 y SP2 de NGS e incluye la información de corrección del reloj del satélite que se calcula simultáneamente con las órbitas. Se basa principalmente en la posición y el reloj, y no incluye las velocidades. El formato se propuso en Remondi, 1989 y se adoptó en 1991. Además de la información de corrección del reloj del satélite, incluye información como los exponentes de precisión de la órbita, las líneas de comentarios, la semana del GPS y los segundos de la semana asociados con la primera época. Los archivos SP3 se pueden abrir con Wolfram Research Mathematica.

## Formato de archivo SP3: más información

Los archivos SP3 se guardan en el disco en formato de archivo ASCII y su contenido se puede abrir en cualquier editor de texto para verlo. La estructura de un archivo SP3 se puede ver en la siguiente imagen.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referencias

* [El formato de órbita 3 del producto estándar extendido (SP3-c)] (http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,una estructura%20más%20flexible%20encabezado%20)
* [Ampliación de los formatos de órbita GPS estándar del Estudio Geodésico Nacional](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

