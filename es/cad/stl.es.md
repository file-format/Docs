{
  "date" : "2020-03-16",
  "keywords" :[ "Archivo STL", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo STL y las API que pueden crear y abrir archivos STL",
  "title" :"Formato de archivo STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo STL?

STL, abreviatura de estereolitrografía, es un formato de archivo intercambiable que representa geometría de superficie tridimensional. El formato de archivo encuentra su uso en varios campos, como la creación rápida de prototipos, la impresión 3D y la fabricación asistida por computadora. Representa una superficie como una serie de pequeños triángulos, conocidos como facetas, donde cada faceta está descrita por una dirección perpendicular y tres puntos que representan los vértices del triángulo. Las aplicaciones utilizan los datos resultantes para determinar la sección transversal de la forma 3D que construirá el fabricante. No hay información disponible en el formato de archivo STL para la representación de color, textura u otros atributos comunes del modelo [CAD](/es/cad/).

## Breve historia ##

El desarrollo del formato de archivo STL se remonta a 1987. Fue desarrollado por 3D Systems para su uso en impresoras 3D comerciales. En 2009 se propuso una versión revisada del formato de archivo STL, conocida como STL 2.0, con actualizaciones del formato de archivo.

## Especificaciones de formato de archivo ##

Un archivo STL representa una geometría de superficie usando facetas. Las facetas definen la superficie de un objeto 3D y se identifican únicamente por una unidad normal, que es una línea perpendicular al triángulo con una longitud de 1,0, y por tres vértices. Hay un total de 12 números almacenados para cada faceta como Normal y cada vértice se especifica mediante tres coordenadas cada uno. El archivo StL no contiene ninguna información de escala; las coordenadas están en unidades arbitrarias.

Las especificaciones del formato de archivo STL se pueden examinar a partir de los siguientes dos aspectos.

### Orientación de facetas ###

La orientación de una faceta está determinada por la dirección de la unidad normal y el orden en que se enumeran los vértices. La orientación de las facetas se especifica de dos maneras como sigue:

* La dirección de la normal es hacia afuera
* Los vértices se ordenan en sentido antihorario desde fuera, obedeciendo la regla de la mano derecha.

### Regla de vértice a vértice ###

Según esta regla, cada triángulo comparte dos vértices con cada uno de sus triángulos adyacentes. Por lo tanto, un vértice de un triángulo no puede estar en el lado de otro triángulo.

## Formatos de archivo ##

STL está disponible en ASCII, así como representaciones binarias para formato de archivo compacto.

### Formato STL ASCII ###

La versión ASCII del formato de archivo STL está escrita en ASCII simple. Sin embargo, debido a su gran tamaño, el formato de archivo no se selecciona como formato preferible para su uso. La sintaxis de un archivo ASCII STL es la siguiente:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Las palabras en negrita representan palabras clave que siempre deben estar en minúsculas. Los símbolos en cursiva son variables que deben reemplazarse con valores especificados por el usuario. Los datos numéricos en las líneas **faceta normal** y **vértice** son flotantes de precisión simple, por ejemplo, 1.23456E+789. Una coordenada **normal de faceta** puede tener un signo menos inicial; una coordenada de **vértice** puede no hacerlo.

### Formato binario STL ###

El formato binario utiliza la representación numérica de punto flotante y entero IEEE. El formato de archivo se representa de la siguiente manera:

|Campo|Información|
---|---|
|Encabezado|80 caracteres|
|Número de triángulos|Entero sin signo little endian de 4 bytes|
|Datos para cada triángulo|12 números de coma flotante de 32 bits|

A continuación se muestra una vista más elaborada del formato de archivo.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referencias ##

* [El formato STL](http://www.fabbers.com/tech/STL_Format)
* [STL - por Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

