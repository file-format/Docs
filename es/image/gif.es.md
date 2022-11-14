{
  "date" : "2019-10-11",
  "keywords" :[ "archivo gif", "formato de archivo gif", "qué es un archivo gif", "archivo", "ejemplo gif", "extensión de archivo gif","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Formato de archivo de imagen",
  "description":"Obtenga información sobre el formato de archivo GIF y las API que pueden crear y abrir archivos GIF",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GIF? ##

Un GIF o formato de intercambio gráfico es un tipo de imagen altamente comprimida. GIF, propiedad de Unisys, utiliza el algoritmo de compresión LZW que no degrada la calidad de la imagen. Para cada imagen, el GIF generalmente permite hasta 8 bits por píxel y hasta 256 colores en la imagen. A diferencia de una imagen [JPEG](/es/image/jpeg/), que puede mostrar hasta 16 millones de colores y alcanza los límites del ojo humano. Cuando surgió Internet, los GIF seguían siendo la mejor opción porque requerían un ancho de banda bajo y eran compatibles con los gráficos que consumen áreas sólidas de color. Un GIF animado combina numerosas imágenes o marcos en un solo archivo y los muestra en una secuencia para generar un clip animado o un video corto. Las limitaciones de color son de hasta 256 para cada cuadro y es probable que sean las menos adecuadas para reproducir otras imágenes y fotografías con degradado de color.

## Formato de archivo GIF ##

Conceptualmente, los archivos GIF tienen un área gráfica de tamaño fijo llena de cero o más imágenes. Algunos archivos GIF dividen el área gráfica de tamaño fijo o los bloques en subimágenes capaces de funcionar como marcos animados en el caso de un GIF animado. El formato GIF utiliza profundidades de píxel de 1 a 8 bits para almacenar los datos de mapa de bits. El modelo de color RGB y los datos de la paleta siempre se utilizan para almacenar las imágenes. Según la versión, un encabezado de longitud fija ("GIF87a" o "GIF89a") define el inicio de un archivo GIF típico.

Actualmente, están disponibles dos versiones de GIF: 87a y 89a. El primero es el formato GIF original, mientras que el segundo es el nuevo formato GIF. En este formato de archivo, las características de los bloques y las dimensiones de los píxeles se mencionan en un descriptor de pantalla lógica de longitud fija. La existencia y el tamaño de una tabla de colores global pueden especificarse mediante el descriptor de pantalla, que rastrea más detalles si están presentes. El tráiler es el último byte del archivo que contiene un solo byte de un punto y coma ASCII. Un diseño de archivo GIF87a típico es el siguiente:

### Encabezado ###

El encabezado contiene seis bytes y se usa para especificar el tipo de archivo como GIF. Aunque el descriptor de pantalla lógica está separado del encabezado real, a veces se considera como el segundo encabezado. La misma estructura que se utiliza para almacenar el encabezado puede almacenar el descriptor de pantalla lógica. Todos los archivos GIF comienzan con la firma de 3 bytes y utilizan los caracteres "GIF" como identificador. La versión también tiene un tamaño de tres bytes y declara la versión del archivo GIF.

### Descriptor de pantalla lógica ###

Un descriptor de imagen de longitud fija especifica la pantalla y la información de color necesaria para crear la imagen GIF. Los campos Alto y Ancho encierran el menor valor de resolución de pantalla, obligatorio para mostrar los datos de la imagen. Si el dispositivo de visualización no puede mostrar la resolución especificada, será necesario escalar para mostrar adecuadamente la imagen. La información de la pantalla y el mapa de colores se muestra en los cuatro subcampos de la siguiente tabla (mientras que el bit 0 es el bit menos significativo):


|Bits|Subcampos
---|---|
|0-2|Tamaño de la tabla de colores global
|3|Bandera de clasificación de tabla de colores
|4-6|Resolución de color
|7|Bandera de tabla de colores global

#### Tabla de colores globales ####

Una tabla de color global opcional se coloca justo después del descriptor de pantalla lógica. Esta tabla mapeada para indexar los datos de color de los píxeles dentro de los datos de la imagen. En ausencia de una tabla de colores global, cada imagen del archivo GIF utiliza su color local. Es mejor proporcionar una tabla de colores predeterminada si falta la tabla de colores global y local. Una serie de triples de tres bytes compone los elementos de la tabla de colores. Cada byte caracteriza un valor de color RGB. Los colores rojo, verde y azul se utilizan como valores de cada elemento de la tabla de colores. Las entradas en la Tabla de colores global alcanzan un máximo de 256 entradas y siempre se representan en una potencia de dos.

#### Datos de imagen ####

Los datos de la imagen almacenan un byte de símbolos no codificados seguidos de una lista enlazada de sub- junto con los datos codificados en LZW.

#### Remolque ####

El tráiler representa un solo byte de datos que es el último carácter del archivo. El valor de este byte es permanentemente 3Bh y especifica el final del flujo de datos. Cada archivo GIF debe tener el tráiler en el último de cada archivo.

## Referencias ##

* [formato de archivo GIF](https://en.wikipedia.org/wiki/GIF)

