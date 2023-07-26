{
  "date" : "2019-10-11",
  "keywords" :[ "x3d fájl", "x3d fájlformátum", "mi az x3d fájl", "fájl", "x3d példa", "x3d fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D képfájl",
  "description":"További információ az X3D fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak X3D fájlokat.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az X3D fájl?
Az X3D egy [XML](/hu/web/xml/) alapú 3D grafikus fájlformátum 3D információk megjelenítésére. Ez egy moduláris szabvány, és számos ISO specifikáció határozza meg. A formátum támogatja a vektoros és rasztergrafikát, az átlátszóságot, a fényeffektusokat és az animációs beállításokat, beleértve az elforgatásokat, elhalványulásokat és kilengéseket. 2001-ben a [VRML](/hu/3d/vrml/) fájlformátum utódja lett. Az X3D előnye, hogy színinformációkat kódol (ellentétben az [STL](/hu/cad/stl/)-vel), amelyet a modell színre történő nyomtatása során használnak. 3d nyomtató. A formátum VRML-bővítményeket tartalmaz, amelyek lehetővé teszik a jelenet kódolását XML-szintaxis, valamint a VRML97 Open Inventor-szerű szintaxisa vagy bináris formázás használatával.

Az X3D absztrakt specifikációját (ISO/IEC 19775) az ISO először 2004-ben hagyta jóvá. Az X3D XML és ClassicVRML kódolásait (ISO/IEC 19776) először 2005-ben hagyták jóvá.

## X3D fájlformátum

Az X3D jelenetfájloknak közös fájlstruktúrájuk van:

* Fájlfejléc (XML, ClassicVRML vagy tömörített bináris)
* Az X3D gyökércsomópont kezdete, beleértve a verzió- és profilattribútumokat
* Egy fejrész komponens és meta utasításokkal (mindkettő opcionális)
* Az X3D Scene gráf és gyermekcsomópontjai
* Az X3D gyökércsomópont vége

## Példa X3D fájlformátumra

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

## Hivatkozások ##

* [X3D – a Wikipedia által](https://en.wikipedia.org/wiki/X3D)
* [Web3D Consortium hivatalos webhelye](https://www.web3d.org/)
* [X3D hivatalos webhely](https://www.web3d.org/x3d/what-x3d)

