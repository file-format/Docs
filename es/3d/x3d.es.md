{
  "date" : "2019-10-11",
  "keywords" :[ "archivo x3d", "formato de archivo x3d", "qué es un archivo x3d", "archivo", "ejemplo x3d", "extensión de archivo x3d","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Archivo de imagen 3D",
  "description":"Obtenga información sobre el formato de archivo X3D y las API que pueden abrir y crear archivos X3D",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo X3D?
X3D es un formato de archivo de gráficos 3D basado en [XML](/es/web/xml/) para la presentación de información 3D. Es un estándar modular y se define a través de varias especificaciones ISO. El formato admite gráficos vectoriales y de trama, transparencia, efectos de iluminación y configuraciones de animación, incluidas rotaciones, desvanecimientos y oscilaciones. Se convirtió en el sucesor del formato de archivo [VRML](/es/3d/vrml/) en 2001. X3D tiene la ventaja de codificar información de color (a diferencia de [STL](/es/cad/stl/)) que se usa durante la impresión del modelo en un color. impresora 3d. El formato incluye extensiones de VRML, lo que brinda la capacidad de codificar la escena utilizando una sintaxis XML, así como la sintaxis similar a Open Inventor de VRML97 o el formato binario.

La especificación abstracta para X3D (ISO/IEC 19775) fue aprobada por primera vez por ISO en 2004. Las codificaciones XML y ClassicVRML para X3D (ISO/IEC 19776) fueron aprobadas por primera vez en 2005.

## Formato de archivo X3D

Los archivos de escena X3D tienen una estructura de archivo común:

* Encabezado de archivo (ya sea XML, ClassicVRML o binario comprimido)
* Comienzo del nodo raíz X3D, incluidos los atributos de versión y perfil
* Una sección principal con Componente y Meta declaraciones (ambas opcionales)
* El gráfico de escena X3D y sus nodos secundarios
* Fin del nodo raíz X3D

## Ejemplo de formato de archivo X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## Referencias ##

* [X3D - Por Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Sitio web oficial del Consorcio Web3D](http://www.web3d.org/)
* [sitio web oficial de X3D](http://www.web3d.org/x3d/what-x3d)

