{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "archivo", "extensión", "formato", "formato de archivo 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo PLY y las API que pueden crear y abrir archivos PLY",
  "title" :"PLY - Formato de archivo 3D de polígono",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PLY?

PLY, Polygon File Format, representa un formato de archivo 3D que almacena objetos gráficos descritos como una colección de polígonos. El propósito de este formato de archivo era establecer un tipo de archivo simple y fácil que fuera lo suficientemente general como para ser útil para una amplia gama de modelos. El formato de archivo PLY viene en formato ASCII y binario para un almacenamiento compacto y para guardar y cargar rápidamente. El formato de archivo es utilizado por diferentes aplicaciones que brindan soporte para la lectura de archivos 3D.

Los objetos en formato PLY se describen mediante una colección de vértices, caras y otros elementos, junto con propiedades como el color y la dirección normal que se pueden adjuntar a estos elementos. Otras propiedades que también se pueden almacenar con el objeto incluyen:

* Normales de superficie
* coordenadas de textura
* transparencia
* intervalo de confianza de los datos
* propiedades para el anverso y reverso de un polígono

Un objeto representado por el formato PLY puede ser el resultado de varias fuentes, como objetos digitalizados a mano, objetos poligonales de aplicaciones de modelado, datos de rango, triángulos de cubos en marcha, datos de terreno y modelos de radiosidad.

## Breve historia

El formato PLY fue desarrollado en la década de 1990 por Greg Turk y otros en el laboratorio de gráficos de Stanford y es por eso que también se conoce como formato de triángulo de Stanford. El formato de archivo tiene la versión 1.0 desde entonces y no se realizaron más modificaciones.

## Formato de archivo PLY

Un objeto PLY simple consiste en una colección de elementos para la representación del objeto. Consiste en una lista de (x,y,z) triples de vértices y una lista de caras que en realidad son índices en la lista de vértices. Los vértices y las caras son dos ejemplos de elementos y la mayoría del archivo PLY consta de estos dos elementos. También se pueden crear y adjuntar nuevas propiedades a los elementos de un objeto, pero deben agregarse de tal manera que los programas antiguos no se rompan cuando se encuentran estas nuevas propiedades. Estas propiedades también se pueden descartar mediante la lectura de aplicaciones. Además, se pueden crear nuevos elementos y también se pueden definir propiedades con este elemento.

### Estructura del archivo

La estructura de archivos de un formato de archivo PLY es la siguiente:

|Campo
---|
|Encabezado de archivo
|Lista de vértices
|Lista de rostros
|Lista de otros elementos

#### Estructura de ejemplo

Usaremos el siguiente ejemplo a continuación en nuestra discusión posterior para varias partes de un formato de archivo PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Encabezado de archivo

El encabezado del formato de archivo PLY consta de texto ASCII tanto para el formato ASCII como para el formato binario. El inicio y el final de la sección del encabezado se identifican mediante palabras clave de capa y encabezado final. El comienzo del encabezado tiene la palabra mágica ply, que se utiliza para que los lectores reconozcan el formato de archivo PLY. La siguiente línea muestra el número de versión de este archivo. Los comentarios en un formato de archivo PLY comienzan con la palabra clave de comentario al comienzo de cada línea de comentario.

#### Palabra clave del elemento

La palabra clave del elemento luego dice qué hay dentro del archivo. Le siguen las propiedades para ese tipo de elemento específico donde cada propiedad tiene su tipo de propiedad y orden especificado como se muestra a continuación:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

En este ejemplo particular, el elemento de vértice específico tiene 3 propiedades de tipo flotante con su orden especificado.

#### Tipos de tipos de datos

Hay dos tipos de tipos de datos que puede tener una propiedad.

`Scalar`: los tipos de datos escalares son los que se muestran a continuación:

|#Nombre|#Tipo|#Número de bytes
|carácter|carácter|1
|uchar|personaje sin firmar|1
|corto|entero corto|2
|ushort|entero corto sin signo|2
|int|Entero|4
|uint|Entero sin signo|4
|flotador|flotador de precisión simple|4
|doble|flotador de precisión doble|8

`Lista`: Hay una forma especial de definiciones de propiedad que utiliza el tipo de datos de lista. Un ejemplo de esto es del archivo de cubo anterior:

`lista de propiedades uchar int vertex_index`

Esto significa que la propiedad "vertex_index" contiene primero un carácter sin signo que indica cuántos índices contiene la propiedad, seguido de una lista que contiene tantos enteros. Cada entero en esta lista de longitud variable es un índice de un vértice.

## Referencias ##

* [Formato de archivo PLY] (http://paulbourke.net/dataformats/ply/)
* [PLY - Por Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

