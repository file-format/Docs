{
  "date" : "2020-03-16",
  "keywords" :[ "Archivo PAT", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo PAT y las API que pueden crear y abrir archivos PAT",
  "title" :"Formato de archivo PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## ¿Qué es un archivo PAT?

Un archivo con extensión .pat es un archivo CAD que utiliza el software AutoCAD. Las aplicaciones que pueden abrir archivos PAT usan el patrón de sombreado almacenado en estos archivos para obtener información sobre la textura/relleno de un área. Los patrones contenidos dan información sobre la apariencia del material a los objetos dibujados. Los archivos PAT se pueden abrir en aplicaciones como Autodesk AutoCAD, CorelDRAW Graphics Suite y Ketron Software. Los archivos PAT se pueden convertir a diferentes formatos de imagen, como JPG, PNG, BMP, etc.

## Formato de archivo PAT

Los archivos PAT están escritos en formato de texto sin formato y se pueden abrir en cualquier editor de texto. Los patrones de sombreado de estos archivos están basados en vectores y siguen la sintaxis descrita en la documentación de AutoCAD.

Todos los patrones comienzan en el punto 0,0, el patrón se calcula para cubrir el límite de sombreado.

### Definición de patrón

Todas las definiciones de patrones constan de los siguientes campos:
* Un liderazgo '\*'
* Un nombre: el nombre no puede tener espacios, signos de puntuación, paréntesis ni barras.
* Una descripcion

El formato estándar para los patrones de sombreado es `<\*><name> <, descripción>`. El nombre y la descripción están separados por una coma y las descripciones no pueden exceder la longitud de línea de ochenta caracteres. Los patrones de sombreado se definen después de esta información.

### Ejemplos de patrones de sombreado
El siguiente es un ejemplo de patrón cuadrado
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Otro ejemplo que muestra un patrón de paralelogramo es el siguiente.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referencias ##

* [Patrones hash de Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

