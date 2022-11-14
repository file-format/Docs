{
  "date" : "2019-10-11",
  "keywords" :[ "archivo xpm", "formato de archivo xpm", "qué es un archivo xpm", "archivo", "ejemplo de xpm", "extensión de archivo xpm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Formato de archivo X PixMap",
  "description":"Obtenga información sobre el formato de archivo XPM y las API que pueden crear y abrir archivos XPM",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo XPM?

Un archivo con extensión .xpm es un formato de archivo de imagen que fue utilizado por el sistema X Windows. Admite píxeles transparentes y, por lo general, tiene como objetivo la creación de mapas de píxeles de iconos. Admite datos de mapa de píxeles monocromáticos, a escala gra y en color. Estos fueron diseñados para ser editables a mano y pueden incluirse en el código [C](/es/programación/c/). Para este propósito, los archivos XPM están en formato de archivo de texto sin formato y siguen la sintaxis del lenguaje de programación C. Los archivos XPM se pueden abrir con una variedad de aplicaciones de visualización de imágenes, como
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView y Canvas X.

## Formato de archivo XPM

El formato de archivo XPM utiliza la sintaxis C para que estos se integren en los programas C y C++. Consta de las siguientes seis secciones diferentes.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Las secciones son en realidad una matriz de cadenas de la siguiente manera.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Los siguientes son los detalles de cada sección.

`<Values> ` - Esta sección es una cadena que contiene cuatro o seis enteros que están en base 10 y corresponden a:

* ancho y alto del mapa de píxeles
* número de colores
* número de caracteres por píxel
* coordenadas de puntos de acceso opcionales y etiqueta XPMEXT

`<Colors> ` - Esta sección contiene tantas cadenas como colores. Cada cadena es la siguiente:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Esta sección se compone de<height> cuerdas y<width> \*<chars_per_pixel> caracteres. Cada<chars_per_pixel> cadena de longitud debe ser uno de los grupos definidos previamente en el<Colors> sección.

`<Extension> ` - La sección de extensión debe estar etiquetada, si no está vacía, en el<Values> sección. Puede constar de varios<Extension> incisos que pueden ser de los dos tipos siguientes:

* una cadena independiente compuesta de la siguiente manera: XPMEXT<extension-name><extension-data>
* o un bloque compuesto por varias cadenas:XPMEXT<extension-name><related extension-data composed of several strings>

## Referencias

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Manual XPM] (http://www.xfree86.org/current/xpm.pdf)

