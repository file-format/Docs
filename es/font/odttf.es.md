{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo ODTTF - Formato de archivo de fuente OpenType ofuscado",
  "description":"Obtenga información sobre el formato de archivo ODTTF y las API que pueden crear y abrir archivos ODTTF",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## ¿Qué es un archivo ODTTF?

Un archivo ODTTF es un formato de archivo de fuente que utilizan los formatos de archivo [.XPS](/es/page-description-language/xps/) y Microsoft Office 2007. Contiene una fuente OpenType ofuscada que se ha modificado para dificultar la extracción de la información de diseño de la fuente o la ingeniería inversa del código fuente de la fuente. ODTTF se basa en las fuentes utilizadas en los documentos originales, pero no están en un formato simple y es posible que el software de terceros no las lea para extraer datos de fuentes.

Puede abrir archivos ODTTF usando Pagemark XpsViewer, Apple Safari con Pagemark XpsPlugin, Mozilla Firefox con Pagemark XpsPlugin,
NiXPS Ver y NiXPS Editar.

## Formato de archivo ODTTF

La estructura de formato de archivo interno del formato de archivo ODTTF no se conoce, ya que se almacenan como formato ofuscado incrustado. Estos se pueden incrustar en documentos digitales como .PDF o .DOCX.

## Referencias
* [Especificaciones de fuentes OpenType de Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Descripción general de TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

