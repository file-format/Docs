{
  "date" : "2021-02-25",
  "keywords" :[ "archivo bdf", "formato de archivo bdf", "qué es un archivo bdf", "archivo", "ejemplo de bdf", "extensión de archivo bdf","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Formato de distribución de mapa de bits de glifo",
  "description":"Obtenga información sobre el formato de archivo BDF y las API que pueden crear y abrir archivos BDF",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## ¿Qué es un archivo BDF?
Los archivos BDF son legibles por humanos y generalmente se distribuyen en una codificación ASCII. El archivo comienza con información global relevante para la fuente completa, seguida de información y mapas de bits para los glifos individuales. Los datos que contiene muestran la fuente para una orientación de tamaño único. Las métricas a utilizar en más de una dirección pueden estar comprendidas en un único archivo. En el archivo BDF, cada elemento está contenido en una línea de texto separada en el archivo. Los espacios se utilizan para separar los elementos en una línea.

## formato de archivo bdf
Las abreviaturas BDF de Glyph Bitmap Distribution Format; propiedad de Adobe es un formato de archivo para guardar fuentes de tipo mapa de bits. El contenido toma la forma de un archivo de texto destinado a ser legible tanto por computadora como por humanos. El BDF se usa particularmente en entornos Unix X Window. Ha sido reemplazado ampliamente por el formato de fuente PCF, que se supone que es más eficiente, y por fuentes OpenType y TrueType.
### Estructura del archivo BDF
Un archivo de fuente BDF consta de tres secciones:

- una sección global que se aplica a todos los glifos de una fuente.
- una sección con una entrada separada para cada glifo.
- la sentencia ENDFONT.

## Ejemplo
Aquí hay una fuente de ejemplo que contiene un glifo, para ASCII mayúscula 'A'. Sus declaraciones globales comienzan con la línea "STARTFONT" y terminan con la línea "CHARS".
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Referencias
* [Formato de distribución de mapa de bits de glifo](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Especificación del formato de distribución de mapa de bits (BDF) de glifo](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

