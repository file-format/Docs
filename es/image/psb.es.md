{
  "date" : "2019-10-11",
  "keywords" :[ "archivo psb", "formato de archivo psb", "qué es un archivo psb", "archivo", "ejemplo de psb", "extensión de archivo psb","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Formato de archivo de imagen grande de Photoshop",
  "description":"Obtenga información sobre el formato de archivo PSB y las API que pueden crear y abrir archivos PSB",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PSB?
Adobe Photoshop guarda los archivos en dos formatos. Los archivos que tienen un tamaño de 30 000 x 30 000 píxeles se guardan con la extensión PSD y los archivos más grandes que PSD hasta 300 000 x 300 000 píxeles se guardan con la extensión PSB conocida como “Photoshop Big”. Más específicamente, los archivos PSB pueden tener un tamaño de hasta 4 EB (más de 4200 millones de GB) con imágenes que tienen una altura y un ancho de hasta 300 000 píxeles. Los PSD, por otro lado, pueden tener un máximo de 2 GB y dimensiones de imagen de 30,000 píxeles.

PSB también se conoce como tamaño de formato grande para Photoshop y es compatible con todas las funciones de Photoshop, como capas, efectos y filtros. Photoshop puede convertir archivos PSB a [PSD](/es/image/psd/), [JPG](/es/image/jpeg/) , [PNG](/es/image/png/), [EPS](/es/page-description-language/eps/), [GIF](/es/image/gif/) y otros formatos también. El formato de documento grande de Photoshop está disponible una vez que se habilita la función del panel de manejo de archivos del cuadro de diálogo de preferencias de Photoshop.

## Información de formato de archivo ##

El formato de archivo de Photoshop se divide en cinco partes principales con muchos marcadores de longitud para moverse entre las secciones.

|Formato de archivo
---|
|Encabezado de archivo
|Datos del modo de color
| Recursos de imágenes
|Información de capa y máscara
|(((
Datos de imagen
)))

### Encabezado del archivo ###

El encabezado del archivo tiene una longitud fija de 26 bytes y contiene las propiedades básicas de la imagen.

BYTE Firma [4] – Igual a '8BPS'.

WORD Versión [2] – Número de versión, PSD # 1, PSB # 2.

BYTE Reservado [6] – Reservado y siempre cero.

WORD Channels [2]: número de canales de color en la imagen, incluidos los canales alfa. Su valor oscila entre 1 y 56.

LONG Rows [4]: altura de la imagen en píxeles, PSD 1-30 000, PSB 1-300 000.

Columnas LARGAS [4]: ancho de la imagen en píxeles, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] – Número de bits por canal. Los valores admitidos son 1,8,16 y 32.

Modo WORD [2] – Modo de color del archivo.

#### Modo Descripción ####


|Modo|Descripción
---|---|
|0|Mapa de bits (monocromo)
|1|Escala de grises
|2|Indizado
|3|RGB
|4|CMYK
|7|Multicanal
|8|Duotono (medio tono)
|9|Laboratorio

### Datos del modo de color ###

Después de la sección del encabezado del archivo, sigue la sección de datos del modo de color. El bloque comienza con un número LARGO que da la longitud del bloque en bytes. La estructura de los datos del modo de color es la siguiente:

4 bytes: la longitud de los siguientes datos de color.

Variable – Datos de color

Si el valor del campo de modo en la sección del encabezado no es Color indexado o duotono, la longitud del bloque será 0 y no habrá datos después del campo de longitud.

Para las imágenes en color indexadas, la longitud será de 768 bytes que contendrán una paleta de 256 colores. Para duotono, los datos contendrán parámetros de pantalla y otra información relacionada.

### Recursos de imágenes ###

Después de la sección de datos del modo de color, el tercer bloque es la sección de recursos de imagen. Los primeros cuatro bytes son un número LARGO que especifica la longitud del bloque seguido de una serie de bloques de recursos. La estructura del bloque de recursos de imagen es la siguiente:

BYTE Tipo [4] – Firma '8BIM'

ID DE PALABRA [2]: ID de recurso de imagen. Hay una lista de ID de recursos que se puede ver en el enlace de referencia.

BYTE Nombre [Variable] – Nombre: Cadena Pascal con longitud par. ** **

Tamaño LARGO [4]: tamaño real de los datos de recursos que siguen.

Datos BYTE [Variable}: datos de recursos. Está acolchado para hacer el tamaño uniforme.

Algunos de los formatos de recursos se explican brevemente a continuación:

**Formato de recursos de cuadrículas y guías:** La información de cuadrículas y guías se almacena en el bloque de recursos. Estos bloques de recursos contienen una cuadrícula de 16 bytes y un encabezado de guía seguido de bloques de 5 bytes de información de guía.

**Formato de recursos de miniaturas:** La información de miniaturas se almacena en un bloque de recursos de imagen para la visualización de vista previa que consta de un encabezado de 28 bytes y una miniatura JFIF en RGB.

**Formato de recursos de muestras de color:** La información de muestras de color se almacena en un bloque de recursos de imagen con un encabezado de 8 bytes seguido de un bloque de longitud variable de información de muestras de color.

### Información de capa y máscara ###

El cuarto bloque es un bloque de información de capa y máscara y contiene información sobre las capas y máscaras. La información de la capa se almacena primero y luego la información de la máscara.

**Información de la capa:** La información de la capa comienza con un valor LARGO que muestra la longitud de la información de la capa. Después de eso, hay un recuento de valores de PALABRA que muestra el número de registros de capa a seguir.

[8] – longitud de las capas

[2] – Recuento de capas

[Variable] – Información sobre cada capa.

[Variable] – Datos de imagen del canal.** **

**Información de la máscara:** La estructura de la máscara tiene el siguiente formato:


|Estructura de datos|Nombre de campo| Descripción
---|---|---|
|PALABRA| Espacio de color superpuesto | (No documentado)
|BYTE[8]| Componentes de color| componentes de color de 4x2 bytes
|PALABRA| Opacidad| 0#transparente, 1#opaco
|BYTE| Amable| 0#invertido, 1#protegido, 128#usar valor almacenado
|BYTE| relleno | poner a cero

### Datos de imagen ###

La última sección contiene los datos de píxeles de la imagen. Los datos de la imagen se almacenan como una serie de secuencias en planos, es decir, primero todos los datos rojos, luego todos los datos verdes, etc. WORD al comienzo de cada línea muestra el tamaño en bytes relacionado con cada línea de exploración.

[2] – Método de compresión:

[Variable]: datos de imagen en orden plano, es decir, RRRR, GGGG, BBBB, etc.

Métodos de compresión:

0 – Raw Datos de imagen

1 – RLE comprimido

2 – Zip sin predicción

3 – Zip con predicción

## Referencia ##

* [Formato de archivo PSB - Por Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

