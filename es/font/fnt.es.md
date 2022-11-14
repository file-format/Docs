{
  "date" : "2020-08-20",
  "keywords" :[ "archivo fnt", "formato de archivo fnt", "qué es un archivo fnt", "archivo", "ejemplo fnt", "extensión de archivo fnt","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Archivo de fuentes de Windows",
  "description":"Obtenga información sobre el formato de archivo FNT y las API que pueden crear y abrir archivos FNT",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## ¿Qué es un archivo FNT?

Un archivo con la extensión .fnt es un archivo de fuentes que almacena información de fuentes genéricas en los sistemas operativos Windows. Los archivos FNT han sido reemplazados en su mayoría por formatos de archivo TrueType (.TTF) y OpenType (.OTF), y es un formato de archivo de fuente obsoleto a partir de ahora. Estos archivos pueden almacenar una sola fuente de evaluador o vector. Todos los controladores de dispositivos son compatibles con las fuentes de Windows 2.x. Sin embargo, no todos los controladores de dispositivos
Admite la versión de Windows 3.0.

## Formato de archivo FNT

Los archivos FNT son capaces de almacenar una sola fuente rasterizada o vectorial. GDI utiliza con mayor frecuencia los formatos vectoriales en comparación con el ráster, donde el glifo de cada carta se define mediante un pequeño mapa de bits. La razón obvia de la sustitución de .fnt por .ttf y .otf es su formato raster.

### Encabezado del archivo de fuente
El inicio de los archivos de fuentes tanto rasterizadas como vectoriales es común, seguido de información diferente para cada tipo de archivo. El encabezado del archivo de fuente incluido para Windows 3.0 incluye seis nuevos campos, como se muestra a continuación, que se establecen en cero para garantizar la compatibilidad con futuras versiones de Windows.

* dBanderas
* dfAespacio
* espacio dfB
* espacio dfC
* dfColorPointer
* dfReservado1

Para obtener información detallada sobre los encabezados para Windows 3.0 y 2.0, visite [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referencias
* [Formato de archivo de fuente](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Cómo instalar o eliminar una fuente en Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

