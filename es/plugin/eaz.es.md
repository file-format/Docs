{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo EAZ: ¿Qué es un archivo EAZ y cómo abrirlo?",
  "description":"Obtenga información sobre el formato de archivo EAZ y las API que pueden crear y abrir archivos EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-es-eaz"
}
},
  "lastmod" : "2023-12-23"
}

## ¿Qué es un archivo EAZ?

El archivo EAZ es un archivo complementario utilizado por ArcGIS Explorer, una aplicación gratuita desarrollada por ESRI para explorar, visualizar y compartir mapas. Contiene un archivo comprimido que incluye un [XML file](/web/xml/), código compilado y archivos de soporte necesarios para el complemento. Estos archivos se emplean para ampliar la funcionalidad básica del software incorporando nuevos botones, ventanas acoplables y otras extensiones.

## Formato de archivo EAZ - Más información

Los archivos EAZ se crean mediante la utilización del SDK de ArcGIS Explorer, un kit de desarrollo diseñado para crear funcionalidades personalizadas dentro de ArcGIS Explorer. Estos archivos utilizan compresión [ZIP](/compression/zip/) para empaquetar eficientemente su contenido. En el centro del archivo, el archivo **Addins.xml** reside en el directorio raíz y sirve como un componente vital que describe y detalla las diversas personalizaciones integradas en el archivo EAZ.

El archivo Addins.xml actúa esencialmente como una hoja de ruta, ofreciendo información sobre las mejoras, modificaciones y extensiones específicas que el archivo EAZ introduce en ArcGIS Explorer. A través de esta estructura integral, los desarrolladores pueden encapsular e integrar sin problemas nuevas funciones, botones y ventanas acoplables, mejorando la funcionalidad general y la experiencia del usuario de la aplicación ArcGIS Explorer.

## Referencias

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
