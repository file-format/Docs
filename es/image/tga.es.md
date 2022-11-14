{
  "date" : "2019-10-11",
  "keywords" :[ "archivo tga", "formato de archivo tga", "qué es un archivo tga", "archivo", "ejemplo tga", "extensión de archivo tga","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo TGA: un archivo de imagen gráfica TARGA",
  "description":"Obtenga información sobre el formato de archivo TGA y las API que pueden crear y abrir archivos TGA",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo TGA?

Un archivo con la extensión .tga es un formato gráfico rasterizado y fue creado por Truevision Inc. Fue diseñado para las placas TARGA (Truevision Advanced Raster Adapter) y proporcionó soporte de visualización Highcolor/truecolor para PC compatibles con IBM. Admite 8, 16, 24 y 32 bits por píxel y canal alfa de 8 bits. También es compatible con la compresión RLE sin pérdidas que se puede aplicar para reducir el tamaño de la imagen. Las fotos y texturas digitales utilizan el formato de imagen TGA.

## Breve historia

La formación del formato de archivo TGA surgió en 1984 por AT&T EPICenter (más tarde extraído y formado como una entidad independiente conocida como Truevision) que estaba trabajando en la comercialización de nuevas tecnologías desarrolladas por AT&T para búferes de cuadros de color. EPICenter ya estaba trabajando en sus dos primeras tarjetas, la VDA (Adaptador de pantalla de video) y la ICB (placa de captura de imágenes), para las cuales ya se estaba trabajando en dos tipos de archivos, .vda e .icb. Estos formatos de archivo se codificaron y se introdujo el formato de archivo específico menos amplio TGA. TGA fue una extensión de lo que ya estaba en uso y proporcionó información como ancho, alto, profundidad de píxel, mapa de color asociado y origen de la imagen.

La versión 2.0 de TGA, publicada en 1989, incorporó varias funciones mejoradas, como:

* Miniaturas
* Canal alfa
* Valor gama
* Metadatos textuales

Los principales contribuyentes a la versión 2.0 de TGA incluyen a Shawn Steiner, Kevin Fiedly y David Spoelstra de Truevision.

## Especificaciones del formato de archivo TGA TARGA

Un archivo TGA consta de 2 partes principales:

* Encabezado
* Información de píxeles de color

Todos los valores en un archivo TGA están en littl-endian según las especificaciones de formato.

### Cabecera TGA

Un encabezado de archivo TGA consta de los siguientes 5 campos.

|N.º de campo|Longitud |Nombre de campo |Descripción|
---|---|---|---|
|1| 1 byte |longitud de ID| Longitud del campo de ID de imagen (0-255)|
|2| 1 byte |Tipo de mapa de colores| Si se incluye un mapa de color (0: indica que no se incluyen datos de mapa de color con esta imagen. 1: indica que se incluye un mapa de color con esta imagen).|
|3| 1 byte |Tipo de imagen| Compresión y tipos de color (0- No se incluyen datos de imagen. 1- Sin comprimir, imagen mapeada en color, 2- Sin comprimir, imagen en color verdadero, 9- Longitud de ejecución codificada, imagen mapeada en color, 11- Longitud de ejecución codificada, imagen en blanco y negro )|
|4| 5 bytes |Especificación del mapa de colores| Describe el mapa de colores|
|5| 10 bytes |Especificación de imagen| Dimensiones y formato de la imagen|

### Imagen y datos del mapa de color

|Número de campo |Longitud |Campo |Descripción|
---|---|---|---|
|6 |Del campo de longitud de ID de imagen| ID de imagen| Campo opcional que contiene información identificativa |
|7 |Desde el campo de especificación del mapa de colores| Datos del mapa de colores| Tabla de consulta que contiene datos de mapas de colores |
|8 |Del campo de especificación de imagen| Datos de imagen| Almacenado según el descriptor de la imagen|

### Área para desarrolladores (Opcional)

La versión 2.0 de TGA brinda soporte para mejoras/extras adicionales que muchos desarrolladores querían almacenar más información. La información es opcional por lo que si un decodificador TGA no es capaz de interpretarla, será ignorada.

### Área de extensión (opcional)

|Número de campo| Longitud| Campo |Descripción|
---|---|---|---|
|10| 2 bytes |Tamaño de extensión |Tamaño en bytes del área de extensión, siempre 495|
|11| 41 bytes| Nombre del autor |Nombre del autor. Si no se usa, los bytes deben establecerse en NULL (\0) o espacios |
|12| 324 bytes| Comentario del autor| Un comentario, organizado en cuatro líneas, cada una de 80 caracteres más un NULL|
|13| 12 bytes| Sello de fecha/hora |Fecha y hora en que se creó la imagen|
|14| 41 bytes| ID de trabajo||
|15| 6 bytes | tiempo de trabajo| Horas, minutos y segundos dedicados a crear el archivo (para facturación, etc.)|
|16| 41 bytes| ID de software |La aplicación que creó el archivo.|
|17| 3 bytes | Versión de software||
|18| 4 bytes | Color clave||
|19| 4 bytes | Relación de aspecto de píxeles||
|20| 4 bytes | Valor gama||
|21| 4 bytes | Compensación de corrección de color |Número de bytes desde el principio del archivo hasta la tabla de corrección de color, si está presente|
|22| 4 bytes | Sello postal | Número de bytes desde el principio del archivo hasta la imagen del sello postal, si está presente|
|23| 4 bytes | Compensación de línea de escaneo | Número de bytes desde el principio del archivo hasta la tabla de líneas de exploración, si está presente|
|24| 1 byte | Tipo de atributos| Especifica el canal alfa |

### Pie de página del archivo (opcional)

Los últimos 26 bytes del archivo representan el pie de página, que si está presente significa que es probable que sea un archivo TGA versión 2.

|Número de campo| Longitud| Campo| Descripción|
---|---|---|---|
|28| 4 bytes | Compensación de extensión | Desplazamiento en bytes desde el principio del archivo|
|29| 4 bytes | Compensación del área del desarrollador | Desplazamiento en bytes desde el principio del archivo|
|30| 16 bytes| Firma| Contiene "TRUEVISION-XFILE"|
|31| 1 byte | | Contiene "."|
|32| 1 byte | | Contiene NULL|


## Referencias

* [Especificaciones de formato de archivo TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA por Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

