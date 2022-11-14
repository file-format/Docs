{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Archivo", "Formato", "Abrir", "Leer", "API", "MicroStation", "Sistema de diseño de gráficos interactivos de Intergraph" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Formato de archivo de diseño CAD de MicroStation",
  "description" :"Obtenga más información sobre el formato de archivo DGN y las API que pueden crear y abrir archivos DGN",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## ¿Qué es un archivo DGN?

Un archivo con extensión .dgn (diseño) es un archivo de dibujo creado y compatible con aplicaciones CAD como MicroStation e Intergraph Interactive Graphics Design System. Se utiliza para crear y guardar diseños para proyectos de construcción como carreteras, puentes y edificios. El formato es similar al formato de archivo [DWG](/es/cad/dwg/) de Autodesk y se considera su competidor. Los archivos DNG se pueden guardar como formato de archivo estándar de Intergraph o V8 DGN. DGN se puede convertir a otros formatos como DWG, [BMP](/es/image/bmp/), [JPEG](/es/image/jpeg/), [PDF](/es/pdf/), [GIF](/es/image/ gif/) y otros. Se puede abrir con Autodesk AutoCAD, Bentley View y Bentley Systems MicroStation además de otras aplicaciones de software como las versiones Corel PaintShop Photo Pro e IMSI TurboCAD Deluxe.

## Formato de archivo V8 DGN

Un archivo DGN de MicroStation V8 se compone de uno o más modelos. Un modelo es un contenedor de elementos. El DGN V8 elimina todas las restricciones basadas en el formato de archivo que estaban presentes en versiones anteriores de MicroStation. A continuación se muestra una lista de mejoras en el formato de archivo DGN.

* Se eliminó el límite en la cantidad de niveles en un archivo DGN, y cada nivel se nombra y almacena como un elemento.
* El tamaño físico máximo del archivo DGN no tiene ninguna limitación y solo está limitado por el sistema operativo (por ejemplo, el límite de NT es de 4 GB)
* El tamaño máximo de un solo elemento es de 128 KB.
* No hay límite en el tamaño máximo de una celda.
* Los nombres de celda están limitados a aproximadamente 500 caracteres.
* No hay límite en el número de referencias que se pueden adjuntar a un archivo DGN.
* Una cadena de líneas, una forma o una curva de puntos pueden tener hasta 5000 vértices.
* No hay límite para el número de componentes en una cadena compleja o forma compleja.
* No hay límite para el número de grupos de gráficos en un archivo DGN.
* La cerca es paralela a la vista en la que se coloca.
* Una sola línea de texto puede contener 65.535 caracteres.
* No hay límite en el tamaño máximo de un nodo de texto.
* No hay límite para el número de nodos de texto en un archivo DGN.
* Cada elemento tiene un identificador único de 64 bits que no cambia durante el ciclo de vida del elemento.
* Cada elemento tiene una marca de tiempo que indica la hora del cambio más reciente.

## Referencias

* [DNG - Por Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [Formato de archivo DGN de MicroStation V8](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

