{
  "date" : "2019-10-11",
  "keywords" :[ "archivo png", "formato de archivo png", "qué es un archivo png", "archivo", "ejemplo png", "extensión de archivo png","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PNG - Archivo de imagen ráster",
  "description":"Obtenga información sobre el formato de archivo PNG y las API que pueden crear y abrir archivos PNG",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PNG?

Un archivo **PNG** (Portable Network Graphics) es un formato de archivo de imagen de trama que utiliza compresión sin pérdidas. Este formato de archivo se creó como reemplazo del formato de intercambio de gráficos ([GIF](/es/image/gif/)) y no tiene limitaciones de derechos de autor. Sin embargo, el formato de archivo PNG no admite animaciones. El formato de archivo PNG admite la compresión de imágenes sin pérdidas, lo que lo hace popular entre sus usuarios. Con el paso del tiempo, PNG se ha convertido en uno de los formatos de archivo de imagen más utilizados.

## Breve historia del formato de archivo PNG

La razón principal detrás de la creación del formato de archivo PNG fue el algoritmo de compresión patentado, Lempel-Ziv-Welch, utilizado en el formato de archivo GIF. Esto, junto con otras limitaciones de GIF, creó la necesidad de reemplazar el formato de archivo [**GIF**](/es/image/gif/). La primera propuesta y nombre para el formato de archivo PNG se produjo en enero de 1995. Los eventos clave con respecto a los formatos de archivo PNG se enumeran a continuación:

* Octubre de 1996: se publicaron las especificaciones PNG, versión 1.0, que luego aparecieron como [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Se convirtió en una recomendación del W3C en octubre de 1996.
* Diciembre de 1998: se lanzó la versión 1.1, con algunos pequeños cambios y la adición de tres nuevos fragmentos.
* Agosto de 1999: se lanzó la versión 1.2, que agrega una parte adicional.
* Noviembre de 2003: PNG se convirtió en un estándar internacional (ISO/IEC 15948:2003). Esta versión de PNG difiere solo ligeramente de la versión 1.2 y no agrega nuevos fragmentos.
* Marzo de 2004: ISO/IEC 15948:2004

## Comparación funcional de GIF y PNG

El formato de archivo PNG fue diseñado para ser simple y portátil, legalmente libre de trabas, intercambiable, flexible y robusto. En la siguiente tabla, se enumeran las funciones de GIF heredadas por el formato de archivo PNG, además de las funciones nuevas.

|Característica|GIF|PNG|
---|---|---|
|Imágenes de índice de color de hasta 256 colores|Sí|Sí|
|Soporte para transmisión|Sí|Sí|
|Transparencia|Sí|Sí|
|Información complementaria|Sí|Sí|
|Independencia de hardware y plataforma|Sí|Sí|
|Efectivo|Sí|Sí|
|Imágenes en color verdadero de hasta 48 bits por píxel|No|Sí|
|Imágenes en escala de grises de hasta 16 bits por píxel|No|Sí|
|Canal alfa completo (máscaras de transparencia general)|No|Sí|
|Información gamma de la imagen|No|Sí|
|Confiabilidad|No|Sí|
|Presentación inicial más rápida|No|Sí|

## Estructura del archivo PNG

Casi todos los sistemas operativos tienen soporte para abrir archivos PNG. Por ejemplo, el visor de Microsoft Windows tiene la capacidad de abrir archivos PNG ya que el sistema operativo tiene soporte disponible de manera predeterminada como parte de la instalación. Un archivo PNG consta de una "firma" PNG seguida de una serie de //fragmentos//.

### Encabezado de archivo PNG

Los primeros ocho bytes de un archivo PNG siempre contienen los siguientes valores (decimales):

{{{137 80 78 71 13 10 26 10 }}}

Esta firma indica que el resto del archivo contiene una sola imagen PNG, que consta de una serie de fragmentos que comienzan con un fragmento IHDR y terminan con un fragmento IEND.

### Trozos ###

Cada fragmento consta de cuatro partes:

**Longitud:** Un número entero sin signo de 4 bytes que proporciona el número de bytes en el campo de datos del fragmento. La longitud cuenta solo el campo de datos, no en sí mismo, el código de tipo de fragmento o el CRC. Cero es una longitud válida. Aunque los codificadores y decodificadores deberían tratar la longitud como sin signo, su valor no debe exceder los 231 bytes.

**Tipo de fragmento:** Un código de tipo de fragmento de 4 bytes. Para facilitar la descripción y el examen de los archivos PNG, los códigos de tipo están restringidos a letras ASCII en mayúsculas y minúsculas (AZ y az, o 65-90 y 97-122 decimal). Sin embargo, los codificadores y decodificadores deben tratar los códigos como valores binarios fijos, no como cadenas de caracteres. Por ejemplo, no sería correcto representar el código de tipo IDAT por los equivalentes EBCDIC de esas letras. Las convenciones de nomenclatura adicionales para los tipos de fragmentos se analizan en la siguiente sección.

**Datos de fragmento:** Los bytes de datos apropiados para el tipo de fragmento, si corresponde. Este campo puede ser de longitud cero.

**CRC:** un CRC (comprobación de redundancia cíclica) de 4 bytes calculado en los bytes anteriores del fragmento, incluido el código de tipo de fragmento y los campos de datos del fragmento, pero sin incluir el campo de longitud. El CRC siempre está presente, incluso para fragmentos que no contienen datos.

La longitud de los datos del fragmento puede ser cualquier número de bytes hasta el máximo; por lo tanto, los implementadores no pueden asumir que los fragmentos están alineados en límites mayores que los bytes.

Los fragmentos pueden aparecer en cualquier orden, sujeto a las restricciones impuestas a cada tipo de fragmento. (Una restricción notable es que IHDR debe aparecer primero e IEND debe aparecer al final; por lo tanto, el fragmento IEND sirve como marcador de fin de archivo). Pueden aparecer varios fragmentos del mismo tipo, pero solo si se permite específicamente para ese tipo.

#### Tipos de fragmentos

Los tipos de fragmentos se clasifican en fragmentos **Críticos** y **Auxiliares** según el valor ASCII de 4 bytes que distingue entre mayúsculas y minúsculas asignado al tipo de fragmento. Todas las implementaciones deben comprender y representar con éxito los fragmentos críticos estándar. Una imagen PNG válida debe contener un fragmento IHDR, uno o más fragmentos IDAT y un fragmento IEND.

### Compresión

El método de compresión PNG 0 (el único método de compresión actualmente definido para PNG) especifica la compresión desinflar/inflar con una ventana deslizante de 32768 bytes como máximo. La compresión Deflate es un derivado de LZ77 utilizado en zip, gzip, pkzip y programas relacionados. Se ha realizado una amplia investigación que respalda su estado libre de patentes. Los datos comprimidos dentro del flujo de datos zlib se almacenan como una serie de bloques, cada uno de los cuales puede representar datos sin procesar (sin comprimir), datos comprimidos LZ77 codificados con códigos Huffman fijos o datos comprimidos LZ77 codificados con códigos Huffman personalizados. Un bit marcador en el bloque final lo identifica como el último bloque, lo que permite que el decodificador reconozca el final del flujo de datos comprimido.

#### Filtrado de precompresión

Se aplican filtros de precompresión para preparar los datos de imagen para una compresión óptima. El método de filtro PNG define cinco tipos de filtro básicos de la siguiente manera:

|Tipo de filtro|Nombre|Valor previsto|
---|---|---|
|0|Ninguno|La línea de exploración se transmite sin modificar|
|1|Sub|Transmite la diferencia entre cada byte y el valor del byte correspondiente del píxel anterior.|
|2|Arriba|El filtro Arriba() es igual que el filtro Sub() excepto que el píxel inmediatamente encima del píxel actual, en lugar de solo a su izquierda, se usa como predictor.|
|3|Promedio|El filtro Promedio() usa el promedio de los dos píxeles vecinos (izquierda y arriba) para predecir el valor de un píxel.|
|4|Paeth|El filtro Paeth() calcula una función lineal simple de los tres píxeles vecinos (izquierda, arriba, arriba a la izquierda), luego elige como predictor el píxel vecino más cercano al valor calculado.|

Los algoritmos de filtrado se aplican a "bytes", no a píxeles, independientemente de la profundidad de bits o el tipo de color de la imagen. Los algoritmos de filtrado funcionan sobre la secuencia de bytes formada por una línea de exploración. Si la imagen incluye un canal alfa, los datos alfa se filtran de la misma forma que los datos de la imagen.

Cuando la imagen está entrelazada, cada paso del patrón de entrelazado se trata como una imagen independiente para fines de filtrado. Los filtros funcionan sobre las secuencias de bytes formadas por los píxeles realmente transmitidos durante un pase, y la "línea de exploración anterior" es la que se transmitió previamente en el mismo pase, no la adyacente en la imagen completa. Tenga en cuenta que la subimagen transmitida en cualquier paso siempre es rectangular, pero tiene un ancho y/o alto más pequeño que la imagen completa. El filtrado no se aplica cuando esta subimagen está vacía.

## Referencias ##

* [PNG - Página de inicio](http://www.libpng.org/pub/png/)

