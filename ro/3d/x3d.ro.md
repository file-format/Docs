{
  "date" : "2019-10-11",
  "keywords" :[ "fișier x3d", "format fișier x3d", "ce este un fișier x3d", "fișier", "exemplu x3d", "extensie fișier x3d", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Fișier imagine 3D",
  "description":"Aflați despre formatul de fișier X3D și despre API-urile care pot deschide și crea fișiere X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier X3D?
X3D este un format de fișier grafic 3D bazat pe [XML](/ro/web/xml/) pentru prezentarea informațiilor 3D. Este un standard modular și este definit prin mai multe specificații ISO. Formatul acceptă grafică vectorială și raster, transparență, efecte de iluminare și setări de animație, inclusiv rotații, estompări și balansări. A devenit succesorul formatului de fișier [VRML](/ro/3d/vrml/) în 2001. X3D are avantajul de a codifica informațiile de culoare (spre deosebire de [STL](/ro/cad/stl/)) care este utilizat în timpul imprimării modelului pe o culoare. imprimantă 3d. Formatul prezintă extensii pentru VRML, oferind capacitatea de a codifica scena folosind o sintaxă XML, precum și sintaxa de tip Open Inventor a VRML97 sau formatare binară.

Specificația abstractă pentru X3D (ISO/IEC 19775) a fost aprobată pentru prima dată de ISO în 2004. Codificările XML și ClassicVRML pentru X3D (ISO/IEC 19776) au fost aprobate pentru prima dată în 2005.

## Format de fișier X3D

Fișierele scenei X3D au o structură de fișiere comună:

* Antetul fișierului (fie XML, ClassicVRML sau Compressed Binary)
* Începutul nodului rădăcină X3D, inclusiv atributele versiunii și profilului
* O secțiune de cap cu instrucțiuni Component și Meta (ambele opționale)
* Graficul X3D Scene și nodurile sale secundare
* Sfârșitul nodului rădăcină X3D

## Exemplu de format de fișier X3D

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

## Referințe ##

* [X3D - După Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Web3D Consortium site-ul oficial](http://www.web3d.org/)
* [Site-ul web oficial X3D](http://www.web3d.org/x3d/what-x3d)

