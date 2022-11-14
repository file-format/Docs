{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "archivo", "extensión", "formato", "formato de video","Qué es un archivo SWF", "formato de archivo swf", "reproductor de archivos swf","cómo abrir un archivo swf"] ,
  "title" :"Archivo SWF - Formato de archivo de película Shockwave Flash",
  "description":"Obtenga información sobre qué es un archivo SWF y las API que pueden crear y muestre cómo abrir el archivo SWF",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo SWF?

Un archivo SWF es un archivo de animación que se crea con Adobe Flash. Puede contener diferentes tipos de elementos como texto, imágenes vectoriales, imágenes rasterizadas, scripts de acción, objetos como círculos, líneas, cuadrados y rectángulos para crear la animación. Los archivos SWF organizan estos elementos multimedia en fotogramas que se pueden reproducir en diferentes fotogramas por segundo (fps). SWF significa archivo web corto, pero también se conoce como formato Shockwave.

Las aplicaciones que podían *abrir archivos SWF** incluían Adobe Flash Player (ahora descontinuado) y Eltima Elmedia Player.

## Formato de archivo SWF: más información

Los archivos SWF se solían almacenar como archivos binarios en el disco. El formato de archivo SWF se usó para desarrollar animaciones y juegos que se podían incrustar en sitios web y jugar de forma independiente también. También admitía videos y sonidos que brindaban a los desarrolladores muchas opciones para crear aplicaciones multimedia interactivas. Los archivos SWF pueden reproducirse en navegadores web que tengan instalado Adobe Shockwave. Adobe Flash se suspendió en diciembre de 2020 debido a sus deficiencias y problemas de seguridad.

## Breve historia del formato de archivo SWF

El formato de archivo SWF fue diseñado originalmente por FutureWave Software, para mostrar animaciones con la intención de ejecutarse en un software de reproducción en cualquier sistema con conexiones de red más lentas, manteniendo el tamaño del archivo pequeño. En diciembre de 1996, Macromedia adquirió FutureWave y se convirtió a Macromedia Flash 1.0.

En 2005, Macromedia fue adquirida por Adobe, quien anunció SWF como parte de su proyecto de código abierto en 2008. Durante el mismo año, Adobe lanzó código a los motores web más populares del mundo para permitirles rastrear e indexar archivos SWF. Sin embargo, dado que los archivos SWF parecen convertirse en un formato estándar para publicar contenido Flash en Internet, SWF se ha revisado para que signifique formato web pequeño.

## Estructura del archivo SWF

Path es el elemento gráfico básico en SWF, que es una secuencia de segmentos de elementos básicos, que van desde líneas simples hasta curvas Bezier. Estos elementos simples también ayudan a crear otras primitivas adicionales como cubos, elipses e incluso textos. Las primitivas gráficas en SWF tienen similitud con los elementos gráficos de otros formatos como SVG y MPEG-4 BIFS.

El formato también permite mostrar listas y reutilizar/renombrar elementos ya definidos. El formato de flujo binario de SWF se puede comparar con los átomos de QuickTime, que es similar en términos de etiqueta, tamaño y carga útil. El formato de transmisión binaria permite a los reproductores más antiguos omitir contenidos no compatibles. Aunque las versiones originales de SWF estaban limitadas a ofrecer imágenes y gráficos vectoriales, las nuevas versiones también permiten contenidos de audio y video.

En la versión 11 se introdujo una nueva API 3D de bajo nivel de Flash Player llamada "Stage3D". Esta API fue concebida para ser la contraparte de OpenGL o Direct3D. Stage3D define los colores en un lenguaje de bajo nivel llamado Adobe Graphics Assembly Language (AGAL). A continuación, se muestran algunos tipos de datos básicos del formato de archivo SWF.

### Coordenadas

Las coordenadas XY en formato de archivo SWF se almacenan como números enteros y se miden en una unidad llamada twip. Un twip consta de 1/20 de un píxel lógico. El píxel lógico y el píxel de la pantalla son los mismos cuando el archivo se reproduce sin escalar al 100 %.

### Tipos de enteros y orden de bytes

Los tipos enteros con y sin signo de 8, 16, 32 y 64 bits están permitidos en el formato de archivo SWF. El orden de bytes little-endian se utiliza para almacenar valores enteros. Aunque dentro de los bytes, el orden de bits se almacena en big-endian. Todos los valores enteros deben estar alineados con bytes. Los enteros con signo se representan mediante patrones de bits de complemento a 2 tradicionales.

### Números de punto fijo

El formato de archivo SWF admite dos tipos de números de punto fijo, es decir, 32 y 16 bits.

### Números de punto flotante

SWF 8 y versiones posteriores utilizan tres tipos de números de punto flotante (FLOAT, FLOAT 16, DOUBLE) que son compatibles con el estándar IEEE 754 de tipos de punto flotante.

### Enteros codificados

SWF 9 y versiones posteriores admiten un tipo de entero codificado con un número variable de bytes.

## Referencias

* [formato de archivo SWF] (https://en.wikipedia.org/wiki/Swf)

