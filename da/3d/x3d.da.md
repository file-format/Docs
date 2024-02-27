{
  "date": "2019-10-11",
  "keywords": [
"x3d fil",
"x3d filformat",
"hvad er en x3d-fil",
"fil",
"x3d eksempel",
"x3d filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X3D - 3D billedfil",
  "description": "Lær om X3D-filformater og API'er, der kan åbne og oprette X3D-filer.",
  "linktitle": "X3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-x3d"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en X3D fil?
X3D is an [XML](/web/xml/) based 3D graphics file format for presentation of 3D information. It is a modular standard and is defined through several ISO specifications. The format supports vector and raster graphics, transparency, lighting effects, and animation settings including rotations, fades, and swings. It became successor of [VRML](/3d/vrml/) file format in 2001. X3D har fordelen ved at kode farveoplysninger (i modsætning til [STL](/cad/stl/)), der bruges under udskrivning af modellen på en 3D-farveprinter. Formatet har udvidelser til VRML, der giver mulighed for at kode scenen ved hjælp af en XML-syntaks samt den Open Inventor-lignende syntaks af VRML97 eller binær formatering.

The abstract specification for X3D (ISO/IEC 19775) was first approved by the ISO in 2004. XML- og ClassicVRML-kodningerne til X3D (ISO/IEC 19776) blev først godkendt i 2005.

## X3D filformat

X3D-scenefiler har en fælles filstruktur:

* Filoverskrift (enten XML, ClassicVRML eller Compressed Binary)

* Start af X3D-rodnoden inklusive versions- og profilattributter

* En hovedsektion med komponent- og metaudsagn (begge valgfrit)

* X3D Scene-grafen og dens underordnede noder

* Slut på X3D-rodnoden


## Eksempel på X3D-filformat

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
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'-da/>
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

## Referencer ##

* [X3D - af Wikipedia](https://en.wikipedia.org/wiki/X3D)

* [Web3D Consortiums officielle hjemmeside](https://www.web3d.org/)

* [X3D officielle hjemmeside](https://www.web3d.org/x3d/what-x3d)


