{
  "date" : "2019-10-11",
  "keywords" :[ "archivo djvu", "formato de archivo djvu", "qué es un archivo djvu", "archivo", "ejemplo de djvu", "extensión de archivo djvu","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo DJVU",
  "description":"Obtenga información sobre el formato de archivo DJVU y las API que pueden crear y abrir archivos DJVU",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DJVU?

DjVu, pronunciado como "déjà vu", es un formato de archivo de gráficos destinado a documentos escaneados y libros, especialmente aquellos que contienen una combinación de texto, dibujos, imágenes y fotografías. Fue desarrollado por AT&T Labs. Utiliza múltiples técnicas como la separación de capas de imágenes de texto e imágenes de fondo, carga progresiva, codificación aritmética y compresión con pérdida para imágenes bitonales. Dado que el archivo DJVU puede contener imágenes en color, fotografías, texto y dibujos comprimidos pero de alta calidad y se puede guardar en menos espacio, por lo tanto, se usa en la web como libros electrónicos, manuales, periódicos, documentos antiguos, etc.

DjVu puede calificarse como una alternativa superior a [PDF](/es/pdf/). Las extensiones de archivo asociadas a DjVu son .DJVU o .DJV. DjVu puede lograr relaciones de compresión entre 5 y 10 mejores que los métodos existentes como [JPEG](/es/image/jpeg/) y [GIF](/es/image/gif/) para documentos en color y entre 3 y 8 veces mejor que [TIFF]( /image/tiff/) en documentos en blanco y negro. Los documentos escaneados a 300 DPI a todo color de hasta 25 MB se pueden comprimir hasta 30 a 100 KB. Del mismo modo, los documentos en blanco y negro se pueden comprimir de 5 a 30 KB. La página HTML promedio puede tener hasta 50 KB, por lo tanto, estos documentos se pueden cargar en la red sin ningún problema.

## Breve historia ##

La tecnología DjVu fue desarrollada en los laboratorios de AT&T por [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner y Paul G de 1996 a 2001. El formato de archivo DjVu ha pasado por varias revisiones, la más reciente de 2005.


|Versión|Fecha de lanzamiento|Notas
---|---|---|
|1–19|1996–1999|Estas son las versiones de desarrollo.
|20|abril de 1999|La página única se cambió al formato de varias páginas.
|23|julio 2002|fragmento CID
|24|febrero 2003|LTAnno trozo
|21|Septiembre 1999|Reemplazo del formato de almacenamiento indirecto. Se agregó la capa de búsqueda de texto.
|22|abril 2001|Orientación de página, color JB2
|25|Mayo 2003|Trozo NAVM. Se agregó soporte para marcadores DjVu.
|26|abril de 2005|Anotaciones de texto/línea

## Formato de archivo DjVu ##

Los documentos DjVu son archivos IFF85. La estructura proporciona una jerarquía de contenedores que contiene información en un archivo DjVu. Estos contenedores también se denominan "Chunks". El tipo de fragmento y el ID de fragmento describen cómo se utiliza el fragmento. Hay un encabezado de 4 bytes seguido de una estructura IFF. Los primeros cuatro bytes de un archivo DjVu son 0x41 0x54 0x26 0x54. Esta sección analiza los diversos tipos de documentos DjVu y los fragmentos correspondientes de los que consisten.


|Id. de fragmento|Uso
---|---|
|FORMULARIO|La porción compuesta que tiene los primeros cuatro bytes de datos de la porción FORM que son identificadores secundarios.
|FORM:DJVM|Un documento DjVu de varias páginas. Fragmento compuesto que contiene el fragmento DIRM.
|FORM:DJVU|Documento DjVu de una sola página. Fragmento compuesto que contiene los fragmentos que forman una página en un documento djvu.
|FORM:DJVI|Un archivo DjVu "compartido" que se incluye a través del fragmento INCL. Anotaciones compartidas y diccionario de formas.
|FORM:THUM|Trozo compuesto que contiene los fragmentos TH44 que son las miniaturas incrustadas.
|DIRM|Información de nombre de página para documentos de varias páginas.
|NAVM|Información de marcadores
|ANTa, ANTz|Anotaciones que incluyen la configuración de la vista inicial y los hipervínculos superpuestos, cuadros de texto, etc.
|TXTa, TXTz|Unicode Texto e información de diseño.
|Djbz|Tabla de forma compartida.
|Sjbz|BZZ comprimió los datos bitonales de JB2 utilizados para almacenar la máscara.
|FG44|IW44 datos utilizados para almacenar en primer plano
|BG44|IW44 datos utilizados para almacenar antecedentes
|TH44|Datos IW44 utilizados para almacenar imágenes en miniatura incrustadas
|WMRM|Se requieren datos JB2 para eliminar una marca de agua
|FGbz|Color JB2 datos. Proporciona un color para cada (¿blit o forma?) en el fragmento Sjbz correspondiente.
|INFO|Información sobre la página DjVu
|INCL|El ID de un fragmento FORM:DJVI incluido.
|BGjp|Fondo codificado en JPEG
|FGjp|Primer plano codificado en JPEG
|Smmr|Máscara codificada G4

### Compresión DJVU

Una sola imagen se divide en muchas imágenes diferentes y luego cada imagen se comprime por separado. Para la creación de un archivo DjVu, la imagen se separa primero en tres imágenes, una imagen de fondo, un primer plano y una máscara. Por lo general, las imágenes de fondo y de primer plano son imágenes en color de menor resolución; pero la imagen de la máscara es una imagen de mayor resolución y, por lo general, el texto se almacena allí. Después de la separación, las imágenes de primer plano y de fondo se comprimen mediante un algoritmo de compresión basado en wavelet IW44, mientras que la imagen de la máscara se comprime mediante otro método llamado JB2.

El método de codificación JB2 elimina gran parte de la redundancia en la imagen de texto al identificar formas idénticas en la página, como múltiples apariciones de un carácter en una fuente en particular. JB2 primero codifica el mapa de bits de cada forma única aprovechando la redundancia entre formas similares. Luego codifica las ubicaciones en las que aparece cada forma en la página. Tanto JB2 como IW44 se basan en un nuevo tipo de codificador aritmético binario adaptativo llamado codificador ZP que elimina cualquier redundancia restante dentro de un pequeño porcentaje del límite de Shannon. El codificador ZP es adaptativo y más rápido que otros codificadores aritméticos binarios aproximados.

## Referencias ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Formato de archivo DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

