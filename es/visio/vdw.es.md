{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","archivo vdw", "formato de archivo vdw", "tipo de archivo vdw", "archivo", "tipo", "qué es un archivo vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW: formato de archivo del servicio de gráficos de Visio",
  "description":"Obtenga información sobre el formato de archivo VDW y las API que pueden crear y abrir archivos VDW",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## ¿Qué es un archivo VDW?

VDW es el formato de archivo del Servicio de gráficos de Visio que especifica las secuencias y los almacenamientos necesarios para representar un dibujo web. Un dibujo web es una colección de páginas de dibujo, formas, fuentes, imágenes, conexiones de datos e información de actualización de diagramas que se puede representar como un dibujo vectorial o rasterizado. Los archivos VDW también se pueden abrir en Microsoft Visio, pero se guardan principalmente para su uso en la web. Microsoft Visio ofrece la capacidad de convertir archivos de Visio a varios formatos de archivo diferentes, incluidos [PNG](/es/Imagen/PNG/), [BMP](/es/Imagen/BMP/), [PDF](/es/pdf/) y otros.

## **VDW** Formato de archivo

Las especificaciones técnicas del formato de archivo VDW están disponibles en línea en [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) y los desarrolladores pueden consultarlas para crear aplicaciones El documento técnico describe los datos contenidos en un archivo compuesto que contiene almacenamientos y flujos. La representación de un dibujo web se hace posible a través de una secuencia, denominada VisioServerData, a través de un archivo ZIP. Una parte XML de ShapGraphic en el archivo describe los elementos gráficos que se muestran en el dibujo web y se expresan en lenguaje de marcado de aplicación extensible (XAML). Una colección de partes XML en el archivo ZIP describe la conexión de datos del dibujo web, información sobre su forma y la lógica de actualización del diagrama. Estas partes se expresan como XML. La parte XML de DataGraphic describe las propiedades recalculadas que se evaluarán después de que los datos del dibujo web se hayan actualizado desde el origen de datos. Los elementos adicionales del archivo ZIP contienen información sobre las fuentes e imágenes utilizadas en el dibujo web.

|![Posible Implementación de un Archivo](/es/web/vdw.png "Posible Implementación de un Archivo")

## Referencias

* [[MS-VGSFF]: formato de archivo del servicio de gráficos de Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

