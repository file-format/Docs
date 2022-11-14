{
  "date" : "2019-10-11",
  "keywords" :[ "archivo tiff", "formato de archivo tiff", "qué es un archivo tiff", "archivo", "ejemplo de tiff", "extensión de archivo tiff","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Formato de archivo de imagen",
  "description":"Obtenga información sobre el formato de archivo TIFF y las API que pueden crear y abrir archivos TIFF",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo TIFF?

TIFF o TIF, formato de archivo de imagen etiquetada, representa imágenes de trama diseñadas para su uso en una variedad de dispositivos que cumplen con este estándar de formato de archivo. Es capaz de describir datos de imagen de dos niveles, escala de grises, colores de paleta y a todo color en varios espacios de color. Admite esquemas de compresión con pérdida y sin pérdida para elegir entre el espacio y el tiempo para las aplicaciones que utilizan el formato. El formato no depende de la máquina y está libre de límites como el procesador, el sistema operativo o los sistemas de archivos.

## Breve historia del formato de archivo TIFF

El formato de archivo TIFF fue creado inicialmente por Aldus Corporation en el otoño de 1986, después de una serie de reuniones con varios fabricantes de escáneres y desarrolladores de software. El objetivo principal del formato de archivo TIFF era proporcionar un formato de archivo de imagen escaneado común para todos los proveedores de escáneres de escritorio. Comenzando con soporte solo para formato de imagen binaria, el formato evolucionó a soporte de imágenes en color y en escala de grises con el paso del tiempo. La versión inicial de las especificaciones del formato de archivo TIFF se puede etiquetar como Reivision 3.0, ya que hubo dos versiones preliminares anteriores. En 1988 se publicó una revisión importante 5.0 que agregó soporte para imágenes de paleta de colores y compresión LZW. La revisión 6.0 de los formatos de archivo TIFF se publicó en 1992 después de eso. En 1994, Adobe Systems adquirió Aldus y las especificaciones ahora están disponibles y son mantenidas por Adobe Systems.

## Especificaciones del formato de archivo TIFF

El formato de archivo TIFF es extensible y ha sufrido varias revisiones que permiten la inclusión de una cantidad ilimitada de información privada o de propósito especial. Un archivo TIFF comienza con un encabezado de 8 bytes donde los bytes son números de 0 a N. El archivo TIFF más grande posible tiene una longitud de 2**32 bytes. El archivo comienza con un encabezado de archivo de imagen de 8 bytes que apunta directamente a un archivo de imagen (IFD). Un IFD contiene información sobre la imagen, así como punteros a los datos de la imagen real.

### Encabezado del archivo TIFF

El encabezado del archivo TIFF de 8 bytes contiene la siguiente información:

**Bytes 0-1:** El orden de bytes utilizado dentro del archivo. Los valores legales son: “II” (4949.H) “MM” (4D4D.H).

En el formato "II", el orden de los bytes es siempre del byte menos significativo al byte más significativo, tanto para enteros de 16 bits como de 32 bits. Esto se denomina orden de bytes little-endian. En el formato "MM", el orden de los bytes siempre es del más significativo al menos significativo, tanto para enteros de 16 bits como de 32 bits. Esto se denomina orden de bytes big-endian.

**Bytes 2-3:** Un número arbitrario pero cuidadosamente elegido (42) que identifica aún más el archivo como un archivo TIFF. El orden de los bytes depende del valor de los bytes 0-1.

**Bytes 4-7:** El desplazamiento (en bytes) del primer IFD. El directorio puede estar en cualquier ubicación del archivo después del encabezado, pero debe comenzar en un límite de palabra. En particular, un directorio de archivos de imagen puede seguir los datos de imagen que describe. Los lectores deben seguir los punteros donde sea que los lleven. El término desplazamiento de bytes siempre se usa en este documento para referirse a una ubicación con respecto al comienzo del archivo TIFF. El primer byte del archivo tiene un desplazamiento de 0.

### Directorio de archivos de imagen

Un IFD contiene información sobre la imagen, así como punteros a los datos reales de la imagen. Consiste en un recuento de 2 bytes del número de entradas del directorio (es decir, el número de campos), seguido de una secuencia de entradas de campo de 12 bytes. , seguido de un desplazamiento de 4 bytes del siguiente IFD (o 0 si no hay ninguno). Debe haber al menos 1 IFD en un archivo TIFF y cada IFD debe tener al menos una entrada.

#### Entrada IFD

Cada entrada IFD de 12 bytes tiene el siguiente formato.


|Bytes|Descripción
---|---|
|0-1|La etiqueta que identifica el campo
|2-3|El tipo de campo
|4-7|Recuento del tipo indicado
|8-11|La compensación de valor, la compensación de archivo (en bytes) del valor para el campo. Se espera que el valor comience en un límite de palabra; la compensación de valor correspondiente será, por lo tanto, un número par. Este desplazamiento de archivo puede apuntar a cualquier parte del archivo, incluso después de que los datos de la imagen

Un campo TIFF es una entidad lógica que consta de una etiqueta TIFF y su valor. Este concepto lógico se implementa como una Entrada IFD, más el valor real si no encaja en la parte de valor/compensación, los últimos 4 bytes de la Entrada IFD. Los términos campo TIFF y entrada IFD son intercambiables en la mayoría de los contextos.

### TIFF de referencia ###

Baseline TIFF es el núcleo de TIFF, los elementos esenciales que todos los principales desarrolladores de TIFF deben admitir en sus productos. La conformidad con el formato TIFF está sujeta al cumplimiento de los requisitos de TIFF de referencia. Estos requisitos están bien documentados en el documento de especificaciones 6.0.

#### Varias imágenes por archivo ####

Puede haber más de un IFD en un archivo TIFF. Cada IFD define un subfile. Un uso potencial de los subarchivos es describir imágenes relacionadas, como las páginas de una transmisión de fax. No se requiere un lector TIFF de línea base para leer ningún IFD más allá del primero.

#### Tipos de imágenes ####

La imagen TIFF de línea de base tiene los siguientes tipos:

**Binivel:** Una imagen de dos niveles contiene dos colores: blanco y negro. TIFF permite que una aplicación escriba datos de dos niveles en formato blanco es cero o negro es cero. El campo que registra esta información se llama **Interpretación Fotométrica**.

* RGB a todo color

La información de interpretación fotométrica para imágenes binivel es la siguiente:

Etiqueta = 262 (106.H)
Tipo = CORTO
**Valores**

|Valor|Descripción|
---|---|
|0|Para imágenes binivel y en escala de grises: 0 se representa en blanco. El valor máximo se representa en negro. Este es el valor normal para Compresión#2|
|1|El negro es cero. Para imágenes de dos niveles y en escala de grises: 0 se representa en negro. El valor máximo se representa en blanco. Si se especifica este valor para Compresión n.º 2, la imagen debería mostrarse e imprimirse al revés.|

**GrayScale:** Las imágenes en escala de grises son una generalización de las imágenes binivel. Las imágenes de dos niveles solo pueden almacenar datos de imágenes en blanco y negro, pero las imágenes en escala de grises también pueden almacenar tonos de gris. Para describir tales imágenes, debe agregar o cambiar los siguientes campos. Los demás campos obligatorios son los mismos que los necesarios para las imágenes de dos niveles. Para imágenes en escala de grises, Compresión # 1 o 32773 (PackBits). En Baseline TIFF, las imágenes en escala de grises pueden almacenarse como datos sin comprimir o comprimirse con el algoritmo PackBits.

La información de **BitsPerSample** para imágenes en escala de grises es la siguiente:

Etiqueta = 258 (102.H)
Tipo = CORTO

El número de bits por componente. Los valores permitidos para las imágenes en escala de grises TIFF de línea base son 4 y 8, lo que permite 16 o 256 tonos distintos de gris.

**Palette-Color:** Las imágenes de paleta de colores son similares a las imágenes en escala de grises. Todavía tienen un componente por píxel, pero el valor del componente se usa como índice en una tabla de búsqueda RGB completa. Para describir dichas imágenes, debe agregar o cambiar los siguientes campos. Los demás campos obligatorios son los mismos que para las imágenes en escala de grises.
La información de interpretación fotométrica para la imagen de paleta de colores es la siguiente:

Interpretación Fotométrica = 3 (Paleta de Colores).
ColorMapTag = 320 (140.H)
Tipo = CORTO
N = 3 * (2 bits por muestra)

Este campo define un mapa de color Rojo-Verde-Azul (a menudo llamado tabla de búsqueda) para imágenes de colores de paleta. En una imagen de paleta de colores, se usa un valor de píxel para indexar en una tabla de búsqueda RGB. Por ejemplo, un píxel de color de paleta que tenga un valor de 0 se mostraría de acuerdo con el triplete rojo, verde y azul 0. En un mapa de colores TIFF, todos los valores rojos aparecen primero, seguidos de los valores verdes y luego los valores azules. En ColorMap, el negro está representado por 0,0,0 y el blanco está representado por 65535, 65535, 65535.

**RGB a todo color:** en una imagen RGB, cada píxel se compone de tres componentes: rojo, verde y azul. No hay ColorMap. Para describir una imagen RGB, debe agregar o cambiar los siguientes campos y valores. Los demás campos obligatorios son los mismos que los necesarios para las imágenes de paleta de colores.

Bits por muestra = 8,8,8. Cada componente tiene una profundidad de 8 bits en una imagen TIFF RGB de línea base.

PhotometricInterpretation = 2 (RGB) y no hay ColorMap.

Etiqueta = 277 (115.H)
Tipo = CORTO
El número de componentes por píxel. Este número es 3 para imágenes RGB, a menos que haya muestras adicionales.

## Referencias ##

* [Formato de archivo TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

