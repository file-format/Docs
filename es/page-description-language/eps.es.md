{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "archivo", "extensión", "formato de archivo", "Diseño de página", "PostScript encapsulado" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo EPS y las API que pueden crear y abrir archivos EPS",
  "title" :"Formato de archivo EPS: archivo PostScript encapsulado",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo EPS?

Un archivo .eps es un archivo de imagen que se guarda en un disco en formato de archivo Postscript encapsulado. Puede contener cualquier combinación de texto, gráficos e imágenes. Los archivos EPS también pueden incluir una imagen de vista previa de mapa de bits encapsulada en el interior para que la muestren las aplicaciones que pueden abrir dichos archivos.

## Breve historia del formato de archivo EPS

Una mirada rápida al formato de archivo EPS desde la perspectiva del historial revela la siguiente información:

* Adobe lanzó la primera versión de EPS en algún momento entre 1985 y 1988
* La versión 2.0 de la especificación EPS se publicó en enero de 1989
* La especificación para la versión 3.0 de EPS se publicó como documento separado en 1992; esta es la última versión publicada.

EPS, en combinación con el mecanismo de extensión Open Structuring Conventions descrito en la cláusula 9 de Adobe's PostScript Language Document Structuring Conventions Specification, formó la base de las primeras versiones del formato de archivo Adobe Illustrator Artwork.

## Formato de archivo EPS

EPS es un formato patentado pero documentado públicamente y las especificaciones del formato de archivo EPS están disponibles públicamente para referencia del desarrollador. EPS es un formato de archivo conforme a [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Convención de Estructuración de Documentos) y se adhiere a todas las reglas establecidas por DSC. El DSC es un formato de archivo especial para documentos PostScript de Adobe. Cualquier aplicación que afirme poder leer archivos EPS debe ser compatible con DSC.

Un archivo EPS consta de dos secciones principales, como se explica a continuación.

### Imagen de vista previa ###

Un archivo EPS típico contiene una imagen de vista previa en un formato diseñado para un uso conveniente en un flujo de trabajo que involucra varios sistemas o aplicaciones. La intención de una vista previa es tener una imagen en un formato que la mayoría de las aplicaciones de gráficos puedan representar; una vista previa suele tener una resolución más baja, en dimensiones de píxeles y/o en profundidad de bits. El archivo de vista previa puede estar en uno de varios formatos. La especificación para EPS_3 enumera tres formatos de vista previa "específicos del dispositivo":

* para Apple Macintosh, una imagen PICT utilizada por la aplicación QuickDraw
* para computadoras DOS, un mapa de bits TIFF
* Metarchivo de Windows.

PICT y Metarchivo de Windows pueden incorporar datos de mapa de bits y gráficos vectoriales. Además, la especificación define una representación independiente del dispositivo muy simple para una imagen de vista previa de mapa de bits incrustada. Esta representación se conoce como formato de intercambio de PostScript encapsulado (EPSI).

Una vista previa de EPSI es un mapa de bits representado como hexadecimal ASCII, envuelto entre algunos comentarios de PostScript para su identificación y destinado a ser simple y fácilmente transportable. Para distinguir los archivos EPS con los diferentes formatos de vista previa, se recomendaron diferentes extensiones de archivo DOS y tipos de archivo Macintosh en la especificación EPS.

### Código PostScript

Como mínimo, el formato de archivo EPS debe incluir lo siguiente:

* un comentario de encabezado, %!PS-Adobe-3.0 EPSF-3.0
* y un comentario de cuadro delimitador, %%BoundingBox: llx lly urx ury, que describe los límites de la ilustración. Estos cuatro argumentos corresponden a las esquinas inferior izquierda (llx, lly) y superior derecha (urx, ury) del cuadro delimitador.

Un archivo EPS no puede utilizar ninguno de los siguientes operadores:

* dispositivo de banda,
* cleardictstack
* copia
* borrar página
* servidor de salida
* dispositivo de marco
* grestoreall
* clip de inicio
* iniciales
* matriz inicial
* abandonar
* bandas de renderizado
* setglobal
* dispositivo de configuración
* conjunto compartido
* iniciar trabajo.

## Conversión de EPS a otros formatos de archivo

Los archivos EPS se pueden convertir a formatos de imagen estándar como [JPG](/es/image/jpeg/), [PNG](/es/image/png/), [TIFF](/es/image/tiff/) y [PDF](/es/pdf/) usando diferentes aplicaciones, por ejemplo, Adobe Illustrator, Photoshop y PaintShop Pro.

Debido a una [vulnerabilidad de seguridad](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) en archivos EPS, Office 2016, Office 2013, Office 2010 y Office 365 han desactivado la capacidad de insertar archivos EPS en documentos de Office.

## Referencias

* [PostScript encapsulado - Por Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

