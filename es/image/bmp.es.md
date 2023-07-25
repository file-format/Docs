{
  "date" : "2019-10-11",
  "keywords" :[ "archivo bmp", "formato de archivo bmp", "qué es un archivo bmp", "archivo", "ejemplo de bmp", "extensión de archivo bmp","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Formato de archivo de imagen",
  "description":"Obtenga más información sobre el formato de archivo BMP y las API que pueden crear y abrir archivos BMP",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# ¿Qué es un archivo BMP? #

Los archivos que tienen la extensión .BMP representan archivos de imagen de mapa de bits que se utilizan para almacenar imágenes digitales de mapa de bits. Estas imágenes son independientes del adaptador de gráficos y también se denominan formato de archivo de mapa de bits independiente del dispositivo (DIB). Esta independencia sirve para abrir el archivo en múltiples plataformas, como Microsoft Windows y Mac. El formato de archivo BMP puede almacenar datos como imágenes digitales bidimensionales tanto en formato monocromático como en color con varias profundidades de color.

## Especificaciones del formato de archivo BMP ##

Los mapas de bits independientes del dispositivo actúan como una ayuda para intercambiar mapas de bits entre dispositivos y aplicaciones. Debido a la continua evolución de este formato de archivo, la información contenida en los encabezados puede ser diferente según la versión de Bitmap. Un único archivo de mapa de bits consta de estructuras de tamaño fijo y variable en una secuencia específica.

Las estructuras de un archivo de mapa de bits se organizan en el siguiente orden:


|Estructura|Opcional|Tamaño|Propósito
---|---|---|---|
|File Header|No|14|Para almacenar información general sobre el archivo de imagen de mapa de bits
|Encabezado DIB|No|Tamaño fijo|Para almacenar información detallada sobre la imagen de mapa de bits y definir el formato de píxel
|Máscaras de bits adicionales|Sí|12 o 16 bytes|Para definir el formato de píxel
|Paleta de colores|Semi-opcional|Tamaño variable|Para definir los colores utilizados por los datos de imagen de mapa de bits
|Brecha1|Sí|Tamaño variable|Alineación de estructura
|Matriz de píxeles|No|Tamaño variable|El formato de píxeles se define mediante el encabezado DIB o las máscaras de bits adicionales.
|Brecha2|Sí|Tamaño variable|Alineación de estructura
|Perfil de color ICC|Sí|Tamaño variable|Para definir el perfil de color para la gestión del color

Cuando una imagen de mapa de bits se carga en la memoria, se convierte en una estructura DIB, utilizada por Windows a través de su API GDI. El encabezado del archivo no forma parte de esta estructura de datos. El color también puede consistir en entradas de 16 bits que constituyen índices de la paleta a la que se hace referencia actualmente en lugar de definiciones de color RGB explícitas. Echemos un vistazo a algunos de estos en detalle, especialmente los encabezados.

### Encabezado del archivo de mapa de bits ###

Un encabezado de archivo de mapa de bits es similar a otros encabezados de archivo utilizados para identificar el archivo. Dado que existen diferentes variantes del formato de archivo BMP, los primeros 2 bytes del formato de archivo BMP son el carácter "B" y luego el carácter "M" en codificación ASCII. Todos los valores enteros se almacenan en formato little-endian.

|Desplazamiento hexadecimal|Desplazamiento dec|Tamaño|Propósito
---|---|---|---|
|00|0|2 bytes|El campo de encabezado utilizado para identificar el archivo BMP y DIB es 0x42 0x4D en hexadecimal, igual que BM en ASCII. Puede seguir los valores posibles.* **BM**: Windows 3.1x, 95, NT, ... etc. * **BA**: matriz de mapa de bits de estructura OS/2 * **CI**: estructura OS/2 icono de color * **CP**: puntero de color constante OS/2 * **IC**: icono de estructura OS/2 * **PT**: puntero OS/2
|02|2|4 bytes|El tamaño del archivo BMP en bytes
|06|6|2 bytes|Reservado; el valor real depende de la aplicación que crea la imagen
|08|8|2 bytes|Reservado; el valor real depende de la aplicación que crea la imagen
|0A|10|4 bytes|El desplazamiento, es decir, la dirección inicial, del byte en el que se pueden encontrar los datos de la imagen de mapa de bits (matriz de píxeles).

#### Encabezado DIB (encabezado de información de mapa de bits) ####

La información detallada sobre la imagen está representada por este encabezado. Con base en esta información, se determinará la aplicación que se utilizará para mostrar la imagen en la pantalla. Todos estos encabezados contienen un campo DWORD (32 bits), que especifica su tamaño, para que una aplicación pueda determinar fácilmente el encabezado utilizado en la imagen. Esto se debe básicamente a que el formato DIB sufrió varias ampliaciones. A continuación se muestra el encabezado DIB con los campos enumerados.

#### Paleta de color ####

Una paleta de colores BMP es una matriz de estructuras que especifican los valores de intensidad RGB de cada color en la paleta de colores de un dispositivo de visualización. Cada píxel de los datos de mapa de bits almacena un único valor que se utiliza como índice en la paleta de colores. La información de color almacenada en el elemento en ese índice especifica el color de ese píxel. La disponibilidad de color en un archivo de mapa de bits varía de la siguiente manera:

* Uno, 4 y 8 bits: se espera que siempre contenga una paleta de colores
* Dieciséis, 24 y 32 bits: nunca contienen paletas de colores
* Archivos BMP de dieciséis y 32 bits: contienen valores de máscara de campos de bits en lugar de la paleta de colores

#### Almacenamiento de píxeles ####

Los píxeles de mapa de bits se almacenan como bits empaquetados en filas donde el tamaño de cada fila se redondea a un múltiplo de 4 bytes (un DWORD de 32 bits) mediante relleno. La cantidad total de bytes necesarios para almacenar los píxeles de una imagen no se puede calcular directamente simplemente contando los bits. Dado que hay relleno involucrado, se requiere el efecto de redondear el tamaño de cada fila a un múltiplo de 4 bytes. Los bytes de relleno (no necesariamente 0) deben agregarse al final de las filas para aumentar la longitud de las filas a un múltiplo de cuatro bytes. Cuando la matriz de píxeles se carga en la memoria, cada fila debe comenzar en una dirección de memoria que sea un múltiplo de 4.

En realidad, la imagen se describe mediante la representación DWORD de 32 bits de la matriz de píxeles. Por lo general, los píxeles se almacenan "de abajo hacia arriba", comenzando en la esquina inferior izquierda, yendo de izquierda a derecha y luego fila por fila desde la parte inferior hasta la parte superior de la imagen. Los formatos de píxeles y sus implicaciones se enumeran a continuación:

* El formato de 1 bit por píxel (1bpp) admite 2 colores distintos (por ejemplo, blanco y negro).
* El formato de 2 bits por píxel (2bpp) admite 4 colores distintos y almacena 4 píxeles por 1 byte; el píxel más a la izquierda se encuentra en los dos bits más significativos. Cada valor de píxel es un índice de 2 bits en una tabla de hasta 4 colores.
* El formato de 4 bits por píxel (4bpp) admite 16 colores distintos y almacena 2 píxeles por 1 byte; el píxel más a la izquierda se encuentra en el nibble más significativo. Cada valor de píxel es un índice de 4 bits en una tabla de hasta 16 colores.
* El formato de 8 bits por píxel (8bpp) admite 256 colores distintos y almacena 1 píxel por 1 byte. Cada byte es un índice en una tabla de hasta 256 colores.
* El formato de 16 bits por píxel (16bpp) admite 65536 colores distintos y almacena 1 píxel por PALABRA de 2 bytes. Cada PALABRA puede definir las muestras alfa, roja, verde y azul del píxel.
* El formato de píxel de 24 bits (24bpp) admite 16 777 216 colores distintos y almacena un valor de 1 píxel por 3 bytes. Cada valor de píxel define las muestras de rojo, verde y azul del píxel (8.8.8.0.0 en notación RGBAX). En concreto, en el orden: azul, verde y rojo (8 bits por cada muestra).
* El formato de 32 bits por píxel (32bpp) admite 4 294 967 296 colores distintos y almacena 1 píxel por DWORD de 4 bytes. Cada DWORD puede definir las muestras alfa, roja, verde y azul del píxel.

## Referencias ##

* [Formato de metaarchivo de Windows](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Formato de archivo BMP](https://en.wikipedia.org/wiki/BMP_file_format)

