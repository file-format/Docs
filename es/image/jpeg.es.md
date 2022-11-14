{
  "date" : "2019-11-25",
  "keywords" :[ "archivo jpeg", "formato de archivo jpeg", "qué es un archivo jpeg", "archivo", "ejemplo de jpeg", "extensión de archivo jpeg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Formato de archivo de imagen",
  "description":"Obtenga más información sobre el formato de archivo JPEG y las API que pueden crear y abrir archivos JPEG",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## ¿Qué es un archivo JPEG? ##

Un JPEG es un tipo de formato de imagen que se guarda mediante el método de compresión con pérdida. La imagen de salida, como resultado de la compresión, es un equilibrio entre el tamaño de almacenamiento y la calidad de la imagen. Los usuarios pueden ajustar el nivel de compresión para lograr el nivel de calidad deseado y al mismo tiempo reducir el tamaño de almacenamiento. La calidad de la imagen se ve afectada de manera insignificante si se aplica una compresión de 10:1 a la imagen. Cuanto mayor sea el valor de compresión, mayor será la degradación de la calidad de la imagen.

## Especificaciones de formato de archivo ##

El formato de archivo de imagen JPEG fue estandarizado por el Grupo Conjunto de Expertos Fotográficos y, de ahí, el nombre JPEG. El formato ha sido el elegido para almacenar y transmitir imágenes fotográficas en la web. Casi todos los sistemas operativos ahora tienen visores que admiten la visualización de imágenes JPEG, que a menudo también se almacenan con la extensión JPG. Incluso los navegadores web admiten la visualización de imágenes JPEG. Antes de entrar en las especificaciones del formato de archivo JPEG, es necesario mencionar el proceso general de pasos involucrados en la creación de JPEG.

### Pasos de compresión JPEG ###

**Transformación:** Las imágenes en color se transforman de RGB a una imagen de luminancia/crominancia (el ojo es sensible a la luminancia, no a la crominancia, por lo que la parte de crominancia puede perder muchos datos y, por lo tanto, puede comprimirse mucho.

**Muestreo descendente:** El muestreo descendente se realiza para el componente de color y no para el componente de luminancia. El muestreo descendente se realiza en una proporción de 2:1 horizontalmente y 1:1 verticalmente (2h 1 V). Por lo tanto, la imagen se reduce de tamaño ya que el componente 'y' no se toca, no hay una pérdida notable de calidad de imagen.

**Organización en grupos:** Los píxeles de cada componente de color se organizan en grupos de 8 × 2 píxeles llamados "unidades de datos" si el número de filas o columnas no es un múltiplo de 8, la fila inferior y las columnas de la derecha se duplican.

**Transformación discreta del coseno:** Luego se aplica la Transformación discreta del coseno (DCT) a cada unidad de datos para crear un mapa de 8×8 de los componentes transformados. La DCT implica cierta pérdida de información debido a la precisión limitada de la aritmética informática. Esto significa que incluso sin el mapa habrá alguna pérdida de calidad de imagen, pero normalmente es pequeña.

**Cuantificación:** cada uno de los 64 componentes transformados en la unidad de datos se divide por un número separado llamado "coeficiente de cuantificación (QC)" y luego se redondea a un número entero. Aquí es donde la información se pierde de forma irrecuperable, los grandes controles de calidad causan más pérdidas. En general, la mayoría de los implementos de JPEG permiten utilizar las tablas de control de calidad recomendadas por el estándar JPEG.

**Codificación:** Los 64 coeficientes transformados cuantificados (que ahora son números enteros) de cada unidad de datos se codifican mediante una combinación de codificación RLE y Huffman.

**Agregar encabezado:** El último paso agrega el encabezado y todos los parámetros JPEG utilizados y genera el resultado.

El decodificador JPEG utiliza los pasos a la inversa para generar la imagen original a partir de la comprimida.

### Estructura del archivo ###

Una imagen JPEG se representa como una secuencia de segmentos donde cada segmento comienza con un marcador. Cada marcador comienza con el byte 0xFF seguido de una bandera de marcador para representar el tipo de marcador. La carga útil seguida por el marcador es diferente según el tipo de marcador. Los tipos de marcadores JPEG comunes se enumeran a continuación:

|Nombre abreviado|Bytes|Carga útil|Nombre|Comentarios
---|---|---|---|---|
|SOI|0xFF, 0xD8|ninguno|Inicio de imagen|
|S0F0|0xFF, 0xC0|tamaño variable|Inicio de trama|
|S0F2|0xFF, 0xC2|tamaño variable|Inicio del cuadro|
|DHT|0xFF, 0xC4|tamaño variable|Definir tablas de Huffman|
|DQT|0xFF, 0xDB|tamaño variable|Definir tabla(s) de cuantificación|
|DRI|0xFF, 0xDD|4 bytes|Definir intervalo de reinicio|
|SOS|0xFF, 0xDA|tamaño variable|Inicio de escaneo|
|RSTn|0xFF, 0xD//n//(/es//n//#0..7)|ninguno|Reiniciar|
|APPn|0xFF, 0xE//n//|tamaño variable|Específico de la aplicación|
|COM|0xFF, 0xFE|tamaño variable|Comentario|
|EOI|0xFF, 0xD9|ninguno|Fin de la imagen|

Dentro de los datos codificados por entropía, después de cualquier byte 0xFF, el codificador inserta un byte 0x00 antes del siguiente byte, de modo que no parece haber un marcador donde no se pretende, lo que evita errores de trama. Los decodificadores deben omitir este byte 0x00. Esta técnica, llamada [relleno de bytes] (https://en.wikipedia.org/wiki/Byte_stuffing) (consulte la sección F.1.2.3 de la especificación JPEG), solo se aplica a los datos codificados en entropía, no a los datos de carga útil de marcadores. . Sin embargo, tenga en cuenta que los datos codificados por entropía tienen algunos marcadores propios; específicamente los marcadores de reinicio (0xD0 a 0xD7), que se utilizan para aislar fragmentos independientes de datos codificados en entropía para permitir la decodificación paralela, y los codificadores pueden insertar estos marcadores de reinicio a intervalos regulares (aunque no todos los codificadores hacen esto).

