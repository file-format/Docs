{
  "date" : "2019-10-11",
  "keywords" :[ "archivo psd", "formato de archivo psd", "qué es un archivo psd", "archivo", "ejemplo psd", "extensión de archivo psd", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Formato de archivo de imagen de Photoshop",
  "description":"Obtenga información sobre el formato de archivo PSD y las API que pueden crear y abrir archivos PSD",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PSD?

PSD, documento de Photoshop, representa el formato de archivo nativo de Adobe Photoshop utilizado para el diseño y desarrollo de gráficos. Los archivos PSD pueden incluir capas de imagen, capas de ajuste, máscaras de capa, anotaciones, información de archivo, palabras clave y otros elementos específicos de Photoshop. Los archivos de Photoshop tienen una extensión predeterminada como .PSD y tienen una altura y un ancho máximos de 30 000 píxeles y un límite de longitud de dos gigabytes.

## Especificaciones del formato de archivo PSD ##

Los datos en un archivo PSD se almacenan en orden de bytes big endian. Esto implica intercambiar los enteros cortos y largos al leer o escribir en la plataforma Windows. El formato de archivo de Photoshop se divide en cinco partes principales. Tiene muchos marcadores de longitud que se pueden usar para pasar de una sección a la siguiente. Los marcadores de longitud generalmente se rellenan con bytes para redondear al intervalo de 2 o 4 bytes más cercano. Las cinco partes principales son:

* Encabezado de archivo
* Datos del modo de color
* Recursos de imagen
* Información de capa y máscara
* Datos de imagen

Para la conformidad, los datos deben escribirse en todos estos campos de la sección, ya que Photoshop puede intentar leer la sección completa. También implica que se escriban ceros en los campos omitidos mientras se escribe en un archivo. El campo de longitud en las secciones delimitadas por longitud debe usarse para decidir cuándo detener la lectura. En la mayoría de los casos, el campo de longitud indica el número de bytes, no de registros, que siguen. Los siguientes puntos deben recordarse al leer un archivo.

* Los valores en la columna "Longitud" en todas las tablas están en bytes.
* Todos los valores definidos como cadena Unicode constan de:
* Un campo de longitud de 4 bytes, que representa el número de caracteres en la cadena (no bytes).
* La cadena de valores Unicode, dos bytes por carácter.

### Encabezado del archivo ###

El encabezado del archivo contiene las propiedades básicas de la imagen.

|Longitud|Descripción
---|---|
|4|Firma: siempre igual a '8BPS' . No intente leer el archivo si la firma no coincide con este valor.
|2|Versión: siempre igual a 1. No intente leer el archivo si la versión no coincide con este valor. (~*~*PSB~*~* la versión es 2.)
|6|Reservado: debe ser cero.
|2|El número de canales en la imagen, incluidos los canales alfa. El rango admitido es de 1 a 56.
|4|La altura de la imagen en píxeles. El rango admitido es de 1 a 30.000.
|4|El ancho de la imagen en píxeles. El rango admitido es de 1 a 30.000.
|2|Profundidad: el número de bits por canal. Los valores admitidos son 1, 8, 16 y 32.
|2|El modo de color del archivo. Los valores admitidos son: Mapa de bits # 0; Escala de grises # 1; indexado # 2; RGB #3; CMYK #4; Multicanal # 7; Duotono # 8; Laboratorio # 9.

### Sección de datos del modo de color ###

La sección de datos del modo de color está estructurada de la siguiente manera:


|Longitud|Descripción
---|---|
|4|La longitud de los siguientes datos de color
|variable|Los datos de color

Los datos del modo de color están disponibles solo para el color indexado y el duotono según lo definido por el campo de modo en la sección Encabezado del archivo. Para todos los demás modos, esta sección está representada por valores puestos a cero de 4 bytes. Para imágenes en color indexadas, la longitud es 768 y los datos de color contienen la tabla de colores para la imagen, en orden no intercalado. Para las imágenes de duotono, los datos de color contienen la especificación de duotono (cuyo formato no está documentado). Otras aplicaciones que leen archivos de Photoshop pueden tratar una imagen de duotono como una imagen gris y simplemente conservar el contenido de la información de duotono al leer y escribir el archivo.

### Sección de recursos de imágenes ###

La tercera sección del archivo contiene recursos de imagen. Comienza con un campo de longitud, seguido de una serie de bloques de recursos.


|Longitud|Descripción
---|---|
|4|Longitud de la sección de recursos de imágenes. La longitud puede ser cero.
|Variable|Recursos de imagen (Bloques de recursos de imagen)

Los recursos de imagen se utilizan para almacenar datos que no son píxeles asociados con imágenes, como las rutas de herramientas de lápiz. Se denominan bloques de recursos porque contienen datos que se almacenaron en el recurso de Macintosh en las primeras versiones de Photoshop. La estructura básica de los bloques de recursos de imágenes es la siguiente:


|Longitud|Descripción
---|---|
|4|Firma: '8BIM'
|2|Identificador único del recurso. Los ID de recursos de imagen contienen una lista de los ID de recursos utilizados por Photoshop.
|Variable|Nombre: cadena Pascal, rellenada para que el tamaño sea uniforme (un nombre nulo consiste en dos bytes de 0)
|4|Tamaño real de los datos de recursos que siguen
|Variable|Los datos del recurso, descritos en las secciones sobre los tipos de recursos individuales. Está acolchado para que el tamaño sea uniforme.

Los recursos de imagen utilizan varios números de identificación estándar.

### Información de capa y máscara ###

La cuarta sección de un archivo de Photoshop contiene información sobre capas y máscaras, como el número de capas, los canales en las capas, los rangos de fusión, las claves de capa de ajuste, las capas de efectos y los parámetros de máscara. Si no hay capas ni máscaras, esta sección se representa mediante un campo de 4 bytes puesto a cero. Se debe prestar especial atención a la longitud de las secciones al leer esta sección debido a los valores puestos a cero. La disposición de la sección Capa y Máscara es la siguiente:


|Longitud|Descripción
---|---|
|4|Longitud de la sección de información de capa y máscara. (La longitud de PSB es de 8 bytes).
|Variable|Información de capa
|Variable|Información de máscara de capa global
|Variable|Serie de bloques etiquetados que contienen varios tipos de datos.

#### Información de la capa ####

La siguiente tabla muestra la organización de alto nivel de la información de la capa.


|Longitud|Descripción
---|---|
|4|Longitud de la sección de información de capas, redondeada a un múltiplo de 2. (La longitud de PSB es de 8 bytes).
|2|Recuento de capas. Si es un número negativo, su valor absoluto es el número de capas y el primer canal alfa contiene los datos de transparencia para el resultado combinado.
|Variable|Información sobre cada capa. Ver Registros de capas describe la estructura de esta información para cada capa.
|Variable|Datos de imagen del canal. Contiene uno o más registros de datos de imagen para cada capa. Las capas están en el mismo orden que en la información de la capa

### Datos de imagen ###

Los datos de píxeles de la imagen se encuentran en la sección Datos de la imagen del archivo. La disposición de los datos en la sección Datos de imagen está en orden plano, es decir, primero todos los datos rojos, luego todos los datos verdes, etc. Cada plano se almacena en orden de línea de exploración, sin bytes de relleno. como se muestra en la siguiente tabla.

|Longitud|Descripción
---|---|
|2|Método de compresión: *0 = Datos de imagen sin procesar * 1 = RLE comprimido Los datos de imagen comienzan con los recuentos de bytes para todas las líneas de exploración (filas * canales), con cada recuento almacenado como un valor de dos bytes. Siguen los datos comprimidos RLE, con cada línea de exploración comprimida por separado. La compresión RLE es el mismo algoritmo de compresión utilizado por la rutina PackBits de ROM de Macintosh y el estándar TIFF. *2 = ZIP sin predicción *3 = ZIP con predicción.
|Variable|Los datos de la imagen. Orden planar = RRR GGG BBB, etc.

## Referencias ##

* [Especificaciones del formato de archivo PSD - Por Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Formato de archivo de Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

