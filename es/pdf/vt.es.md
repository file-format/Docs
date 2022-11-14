{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PDF/VT",
  "description":"Obtenga información sobre el formato de archivo PDF/VT y las API que pueden crear y abrir archivos PDF/VT",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# ¿Qué es PDF/VT? #

PDF/VT, publicado como [ISO 16612-2](https://www.iso.org/standard/46428.html) en agosto de 2010 como estándar, está diseñado para permitir la impresión variable de documentos (VDP) en una variedad de entornos. El estándar hace que la información variable y la impresión transaccional sean su base para el estándar. La impresión de datos variables se utiliza cuando parte de la información es diferente para cada destinatario del contenido. La impresión transaccional incluye facturas, extractos y otros documentos que combinan información de facturación con información de marketing. Esto da como resultado una combinación de procesamiento mejorado de imágenes, texto y otros tipos de contenido. PDF/VT permite una gestión fiable y dinámica de páginas para datos de impresión de salida transaccional de gran volumen (HVTO) mediante el uso del concepto de metadatos de partes del documento (DPM). Los archivos PDF/VT se pueden abrir en el visor de Adobe Acrobat sin necesidad de agregar ningún otro componente.

## Jerarquía de partes del documento ##

La jerarquía de la parte del documento (DPart) es como una estructura de árbol de nodos de parte del documento que se basa en todas las páginas del documento. Los elementos de este árbol se denominan nodos DPart. Cada nodo interno contiene otros nodos DPart y cada nodo hoja especifica una o más páginas para un destinatario. Básicamente, la jerarquía DPart especifica la secuencia y la relación de los documentos o partes de los documentos en un archivo PDF/VT. La estructura de árbol de los nodos DPart representa fácilmente el contenido interno de un documento PDF/VT, ya que puede contener subdocumentos para muchos destinatarios y cada parte del documento corresponde a las páginas de un solo destinatario. La jerarquía DPart es necesaria en los archivos PDF/VT.

## Metadatos de la parte del documento (DPM) ##

Los metadatos de la parte del documento (DPM) están asociados con cada nodo en la jerarquía de la parte del documento y se pueden usar para comunicar información sobre el subdocumento de un destinatario en particular y sus partes. En particular, el DPM puede contener información sobre las propiedades o información sobre los destinatarios en forma codificada.

## Niveles de conformidad ##

PDF/VT se confiere a los siguientes tres niveles de conformidad. Todos están basados en [PDF](/es/pdf/) 1.6.

* `PDF/VT-1`: se basa en PDF/X-4 y contiene todos los recursos necesarios para generar un documento PDF.
* `PDF/VT-2`: diseñado para el intercambio de múltiples archivos, los documentos PDF/VT-2 pueden hacer referencia a intenciones de salida externas, contenidos externos o ambos. Un documento PDF/VT y todos sus archivos PDF a los que se hace referencia y las intenciones de salida externa se denominan colectivamente conjunto de archivos PDF/VT-2. Acrobat 9 y admiten esta función.
* `PDF/VT-2s`: admite transmisión en vivo de PDF/VT-2. Esto permite procesar secciones segmentadas de datos.

## Referencias ##

* [PDF/VT - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [Tecnología gráfica ISO 16612-2](https://www.iso.org/standard/46428.html)

